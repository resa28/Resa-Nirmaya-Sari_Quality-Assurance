# telkomTest

1) Based on your experience as a QA.
    A. Explain in about SDLC, STLC and their differences
    B. Explain the steps for Bug Cycle?
    C. Give us Real Case about Severity and Priority
    D. Give us explanation about Equivalence Partitioning & Boundary Value Analysis testing techniques

**Answer Question 1**

A.  1 SDLC Software Development Life Cycle - related to software development.
    2 STLC Software Testing Life Cycle - related to software testing.
    
B.  Bug cylce is a journey reporting about defact feature what tester found or user found (at uat test).
C.  Severity api submit login is 500, so user cant do go to dashboard when submit login is error [CRITICAL]
D. about design testing we do set test case by group (partition) with value need to be test,
   example = user only can input minimum key search is 3 key string.
        So as tester will create grouping testCase 
        A user input key search with 0 char (partition Equivalence) = result is invalid (boundary Value)
        B user input key search with 1-3 char = result is valid
        C user input keu search with 5-10 char = result is invalid 
        
**Answer Question 2**
- Scenario **positive_case**
"Given user at page ticket
When fill SID field with VALID SID
Then system display SID"
- Scenario **negative_case**
"Given user at page ticket
When fill SID field with INVALID SID
Then system not display SID"

**Answer Question 3**

A with  Equivalence Partitioning & Boundary Value Analysis testing techniques.
B if there found error from scenario, will give the step reproduce with image if need'ed then status scenario is FAILED

**Answer Question 4**

A have different at value **id**, Mock API has double quote, and Real api dont have.
B appear is will same with value two 2, but will error if team api only accept with **INT** value not **STRING**.

REAL API
{
  "data": {
    **"id": 2,**
    "email": "janet.weaver@reqres.in",
    "first_name": "Janet",
    "last_name": "Weaver",
    "avatar": "https://reqres.in/img/faces/2-image.jpg"
  },
  "support": {
    "url": "https://reqres.in/#support-heading",
    "text": "To keep ReqRes free, contributions towards server costs are appreciated!"
  }
}

MOCK API
{
  "data": {
    **"id": "2",**
    "email": "janet.weaver@reqres.in",
    "first_name": "Janet",
    "last_name": "Weaver",
    "avatar": "https://reqres.in/img/faces/2-image.jpg"
  },
  "support": {
    "url": "https://reqres.in/#support-heading",
    "text": "To keep ReqRes free, contributions towards server costs are appreciated!"
  }
}

**Answer Question 5**

Scenario A (system display sideBar after click button buy now at landing page)
Given user is at landing page
When user click button buy now
Then system display shopping cart sideBar

Scenario B (system display sideBar but user click button cancel at shopping cart)
Given user is at landing page
And system display shopping cart sideBar
When user click button  cancel
Then system close sideBar shopping cart

Scenario C (user not fill, mandatory field. (email) )
Given user is at landing page
And system display shopping cart sideBar
When user submit without fill email field
Then system will display error message bellow button buy now


Scenario D (user fill, mandatory field. [email] )
Given user is at landing page
And system display shopping cart sideBar
When user submit with fill email field
Then system will display  order summary

Scenario F (user close content order summary)
Given user is at landing page
And system will display  order summary
When user click button close at order summary
Then system will close order summary contain
