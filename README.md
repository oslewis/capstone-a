# Capstone Project

## Overview

The project is the Capstone of the Full Stack Nanodegree, illustrating the learnt skills throughout the project such as SQLAlchemy, Flask, Authorization & Authentication, Databases, Containerization with Docker, AWS, Heroku. And many more essential & valuable skills.

## Inspiration for the project
At the time of creating the app, the world has been going through a difficult time, financially businesses are struggling as well as people all over the world are being under Quarantine. Due to the circumstances, the app has features which support small businesses to track incoming cashflow & debt which is due to be paid out, counts up the incoming cashflow into a total sum, the total debt sum and illustrates the amount of cash the business owes & has.

The amounts are then illustrated on a Balance Sheet with an added function called Time Left which calculates the total amount of time (by months) the business has left after taking into consideration the amount of money the business has and the amount of debt owed divded by 30.42 which is the average day count in a month.

### Backend

Powered by SQLAlchemy, Flask, Python.

### Deployment

Heroku.

## Getting Started

#### Python 3.8.2

Follow instructions to install the latest version of python for your platform in the [python docs](https://docs.python.org/3/using/unix.html#getting-and-installing-the-latest-version-of-python)

#### Virtual Enviornment

We recommend working within a virtual environment whenever using Python for projects. This keeps your dependencies for each project separate and organized. Instructions for setting up a virtual environment for your platform can be found in the [python docs](https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/)

#### PIP Dependencies

Once you have your virtual environment setup and running, install dependencies by running on the root directory containing the requirements.txt file:

```bash
pip install -r requirements.txt
```

This will install all of the required packages we selected within the `requirements.txt` file.

##### Key Dependencies

- [Flask](http://flask.pocoo.org/)  is a lightweight backend microservices framework. Flask is required to handle requests and responses.

- [SQLAlchemy](https://www.sqlalchemy.org/) is the Python SQL toolkit and ORM we'll use handle the lightweight sqlite database. You'll primarily work in app.py and can reference models.py.

- [Flask-CORS](https://flask-cors.readthedocs.io/en/latest/#) is the extension we'll use to handle cross origin requests from our frontend server.

## Running the server LOCALLY

From within the directory first ensure you are working using your created virtual environment.

To run the server, execute:

```bash
export FLASK_APP=app
export FLASK_ENV=development
flask run
```

Setting the `FLASK_ENV` variable to `development` will detect file changes and restart the server automatically.

# Running On HEROKU

Refer to Link: https://capstone-a.herokuapp.com/


# Auth0 RBAC ENABLED HEROKU VARIABLES:
AUTH0_DOMAIN='frosty-firefly-4743.auth0.com'
AUTH0_ClIENT_ID='ts-ac4aO8Re9Y4dfkwLCbanj3vm3lwQA'
API_AUDIENCE='api'
CLIENT SECRET='Xc_MCVYBs_7sce_xa8y5JbRWimUViyVgDqL9p_r14no_qiFLw05VlVYWXwWduA_N'

Details on setup.sh

# AUTH0 RBAC ENABLED AUTH0 CREDENTIALS:
* Domain: frosty-firefly-4743.auth0.com
* Client ID: X6w4lLApKXnPVmyto3Hm4UOE3RFj2i8w
* Client Secret: mnlDlQVOzS6S2EBXdWpq0h62X-6U3mG46RhRrfSpwbdX8s_G0xaM5OlnvHzNrQSc
* API_AUDIENCE: 'api'

## USERS:

### Admin
user: admin@sample.com
Password: Admin123456!

### Operations Manager
user: sample@sample.com
Password: Sample123456!

### Specialist
user: specialist@sample.com
Password: Sample123456!


# Authorization
## Roles

### Admin
#### Permissions:
* All permissions granted

### Operations Manager
#### Permissions:
* delete:debt: delete debt items		
* delete:debt: delete debt items		
* patch:debt: update debt item		
* patch:income: update cashflow item		
* post:cashflow: create new cashflow stream		
* post:debt: create new debt item		
* read:balance
* read:income
* read:debt

### Specialist
#### Permissions:
* post:cashflow: create new cashflow stream
* post:debt: create new debt item
* read:debt: read debt items
* read:income

## Testing


## AUTH0 CURL

### Access Token BEARER Reponse:
self.auth_specialist = {
    'Authorization':
    'eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCIsImtpZCI6IlJUQXlRa1F5TVRKR1JETTBSa0ZGT0RnNFF6QTFRVVpDTVVJMVFqUkVNMFV6TURFNE9UUTNSZyJ9.eyJpc3MiOiJodHRwczovL2Zyb3N0eS1maXJlZmx5LTQ3NDMuYXV0aDAuY29tLyIsInN1YiI6ImF1dGgwfDVlN2UyNTMwMTkwMWY1MGNjODgzZGRlNyIsImF1ZCI6ImFwaSIsImlhdCI6MTU4NTQ1NDA3NiwiZXhwIjoxNTg1NDYxMjc2LCJhenAiOiJYNnc0bExBcEtYblBWbXl0bzNIbTRVT0UzUkZqMmk4dyIsInNjb3BlIjoiIiwicGVybWlzc2lvbnMiOlsicG9zdDpjYXNoZmxvdyIsInBvc3Q6ZGVidCIsInJlYWQ6ZGVidCIsInJlYWQ6aW5jb21lIl19.v22noxl1wORjtOo_dhOWOKRL7PvmLR_g09pFVihphVn2NioFim_drKrBY2F5jH0PNHlgfP0LTx4HLgqOCdSp3UvCYWq_lmFi7FdcmGzr0qf-G5GoPqJaPeSR1jFMYr9qxllt0z2UNFG80FjemEJDll87CUPtczLbZxG6bg9QW-1VqCYehusathYudNZIK556k--fEBCuiaQRaTg2JVAJOtRoB0_gfhrbOg0cc9PWdMjjM82OqGJVRDBSLfJWt68y3L--rI7qkMuNn5jRKt2yRS0vC7DBS-OTn7mPp40dD40Ez2lMRnfQAsOZeQN7TdL24FY-PhZGSlTxDhUlzLhDWA'
    }

self.auth_operations_manager = {
    'Authorization':
    'eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCIsImtpZCI6IlJUQXlRa1F5TVRKR1JETTBSa0ZGT0RnNFF6QTFRVVpDTVVJMVFqUkVNMFV6TURFNE9UUTNSZyJ9.eyJpc3MiOiJodHRwczovL2Zyb3N0eS1maXJlZmx5LTQ3NDMuYXV0aDAuY29tLyIsInN1YiI6ImF1dGgwfDVlN2UyNDRlNTkzOTAxMGNjOWMzNjI0YyIsImF1ZCI6ImFwaSIsImlhdCI6MTU4NTQ1MzkwMCwiZXhwIjoxNTg1NDYxMTAwLCJhenAiOiJYNnc0bExBcEtYblBWbXl0bzNIbTRVT0UzUkZqMmk4dyIsInNjb3BlIjoiIiwicGVybWlzc2lvbnMiOlsiZGVsZXRlOmRlYnQiLCJkZWxldGU6aW5jb21lIiwicGF0Y2g6ZGVidCIsInBhdGNoOmluY29tZSIsInBvc3Q6Y2FzaGZsb3ciLCJwb3N0OmRlYnQiLCJyZWFkOmJhbGFuY2UiLCJyZWFkOmRlYnQiLCJyZWFkOmluY29tZSJdfQ.3is4tegh_AzbdxrxeYzJEmiQrrNOBy4cGSMQsN_pjRA5_PwDWf5K2mTTHvIkY-BPNGf5RtFwvOaKp3i7Io4jul4NxLfitRuY4trlKJMhrzb75rKkMpoygpFIXfbbYgzXynkfi5JYfzZGblL4Htvf9xrqM3qrasSlzu8y72uql6Sk8C0rRn16JVIvqKJS_54mC3uhQVx5JIIVmO8pZQPJanTMTXABPEHfsu8Z24wM44dcJGG7kTAssjZ1JtCLN3m3HiuV6HdN36h07F427Hb7ZOX18BpygdeEHh0dadLolamAKTteXpfPMkJrlTB6NWbVoEApFxw17iwkbE2eOP4RCA'
}

self.auth_admin = {
    'Authorization':
    'eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCIsImtpZCI6IlJUQXlRa1F5TVRKR1JETTBSa0ZGT0RnNFF6QTFRVVpDTVVJMVFqUkVNMFV6TURFNE9UUTNSZyJ9.eyJpc3MiOiJodHRwczovL2Zyb3N0eS1maXJlZmx5LTQ3NDMuYXV0aDAuY29tLyIsInN1YiI6ImF1dGgwfDVlN2UyNGViYzBhYjM0MGNkNjY3NjQ4MCIsImF1ZCI6ImFwaSIsImlhdCI6MTU4NTQ1NDIxNCwiZXhwIjoxNTg1NDYxNDE0LCJhenAiOiJYNnc0bExBcEtYblBWbXl0bzNIbTRVT0UzUkZqMmk4dyIsInNjb3BlIjoiIiwicGVybWlzc2lvbnMiOlsiZGVsZXRlOmRlYnQiLCJkZWxldGU6aW5jb21lIiwicGF0Y2g6YmFsYW5jZSIsInBhdGNoOmRlYnQiLCJwYXRjaDppbmNvbWUiLCJwb3N0OmNhc2hmbG93IiwicG9zdDpkZWJ0IiwicmVhZDpiYWxhbmNlIiwicmVhZDpkZWJ0IiwicmVhZDppbmNvbWUiXX0.xvnBI0GcAcAMnRocgGi3NBP4_wpL0f4c-zSSNVS2BxIstNuuoKXF-smn5DtrAgagR73bEp8cpsH6RSDGHXAEV-wtmn9L7CD64_au-7oy8V1D1jHHAlQIsSKxqpRoXJfmS-2kS8FKVzMfQ60aRubcDx4TfOOblKziDiaM1WD38Jt4IV4g9Qq5R5F6By54epjOtuLwTtXkrRl49qe0TG8c1Mv08gb2DxbemSCkX3QF0fVe5ryVJlepxsoMQhvzSIS0dRfc4yEoOuxFzA4Buh83XaWZIg7hfUT6Qm6lRh3e8DGk_TR67h_AEys5Yxh0keW3E0wpbi0jghZ1r7klkNvTWg'
    }



To run the tests, run
```

python test_app.py
```
## Error Handling
Errors return as Json objects as per the following format:
```
{
  "success": False,
  "error": 404,
  "message": "resource not found"
}
```
API Error types that may be returned when requests fail:
* 404: resource not found
* 405: method not allowed
* 422: unprocessable
* 400: bad request
* 500: internal error
* auth error

## Endpoints
### GET /cashflow
* Retrieves all cashflow items, receiveables. Retrieves all cashflow received as per payments. Results are paginated in groups of 10.
- Request: None
- Returns: success value and a dictionary of cashflow items. total number of cashflow receiveables, total cash retained (count).
* Example: ```curl http://127.0.0.1:5000/cashflow```
```
  "Cashflow": [
    {
            "id": 1,
            "name": "App Maintainence - Case #582",
            "amount": 8910,
            "category": "Technologies"
        },
    {
            "id": 2,
            "name": "Subscription #12",
            "amount": 80,
            "category": "Technologies"
        },
  ],
  {
  "success": true,
  "total_cashflow": 8990
}
```

## Get /debt
* Retrieves all debt owed as per payments or to be paid out. Results are paginated in groups of 10.
- Request: None.
- Returns: success value, a dictionary list of debt, total number of debts owed, total debt owed (count).
* Example: ```curl http://127.0.0.1:5000/debt```
```
  "Debt": [
    {
            "id": 1,
            "name": "W8BEN FORM",
            "amount": 210,
            "category": "Administration"
        },
    {
            "id": 2,
            "name": "Specialist - Case #1590",
            "amount": 910,
            "category": "Legal"
        },
  ],
  {
  "success": true,
  "total_debt": 1120
}
```
## Get /balance-sheet
* Retrieves all debt owed as per payments or to be paid out as a sum, total number of cashflow receiveables as total cash retained (count), time left for business to survive by calculating amount of cash in account of the business // compared to debt owed.
- Request: None.
* Example: ```curl http://127.0.0.1:5000/balance-sheet```
```
  "BalanceSheet": [
    {
            "total_debt": 60012,
            "total_cashflow": 1000512,
            "time_left": 30917.1597633
        }
  ]
```
## DELETE /cashflow/{id}
* Deletes cashflow item / receivable using the specified id.
- Request: an id of a cashflow item to delete.
- Returns: success value, an id of receivable which has been deleted and the total count remaining.
- Example: ```curl -X DELETE http://127.0.0.1:5000/cashflow/2?page=1```
```
{
  "deleted": 2,
  "success": true,
  "total_questions": 2
}
```
## DELETE /debt/{id}
* Deletes debt / receivable using the specified id.
- Request: an id of a debt item to delete.
- Returns: success value, an id of receivable which has been deleted and the total count remaining.
- Example: ```curl -X DELETE http://127.0.0.1:5000/debt/2?page=1```
```
{
  "deleted": 2,
  "success": true,
  "total_debt": 60012
}
```
```
{
  "deleted": 2,
  "success": true,
  "total_debt": 60012
}
```
## POST /cashflow
* Creates a new cashflow receivable through using the required information such as name, category, amount.
- Returns: success value, id of the generated (created) cashflow receivable and a total number of receivables.
- Example ```curl http://127.0.0.1:5000/cashflow?page=2 -X POST -H "content-Type: application/json" -d
             '{"name": "Hermit", "category": "Technologies", "amount":
               "582"}'
               ```
```
{
  "success": true,
  "created": 1,
  "total_cashflow": 8120
}
```
## POST /debt
* Creates a new debt payment through using the required information such as name, category, amount.
- Returns: success value, id of the generated (created) debt payment and a total number of debt owed.
- Example ```curl http://127.0.0.1:5000/debt?page=2 -X POST -H "content-Type: application/json" -d
             '{"name": "NYSE - #1362", "category": "Administration", "amount":
               "582"}'
               ```
```
{
  "success": true,
  "created": 1,
  "total_debt": 812
}
```

```
## PATCH /cashflow/{id}
* Updates cashflow item / receivable through using the required information such as a name, category, amount.
- Returns: success value, id and format.
- Example ```curl http://127.0.0.1:5000/cashflow?page=2 -X PATCH -H "content-Type: application/json" -d
             '{"name": "Hermit", "category": "Technologies", "amount":
               "3012"}'
               ```
```
{
  "success": true,
  "id": 1,
  "user": {
      "name": "Hermit",
      "category": "Technologies",
      "amount": "3012"
}
```
## PATCH /debts/{id}
* Updates debt payment through using the required information such as a name, category, amount.
- Returns: success value, id and format.
- Example ```curl http://127.0.0.1:5000/debts?page=2 -X PATCH -H "content-Type: application/json" -d
             '{"name": "NYSE - #7912", "category": "Administration", "amount":
               "325"}'
               ```
```
{
  "success": true,
  "id": 1,
  "user": {
      "name": "NYSE - #7912",
      "category": "Administration",
      "amount": "325"
}
```
## PATCH /balancesheets/{id}
* Updates balancesheet through using the required information such as a name.
- Returns: success value, id and format.
- Example ```curl http://127.0.0.1:5000/balancesheets?page=2 -X PATCH -H "content-Type: application/json" -d
             '{"total_debt": "60012", "total_cashflow": "891231", "time_left":
               "27324.7534517"}'
               ```
```
{
  "success": true,
  "id": 1,
  "user": {
      "total_debt": "60012",
      "total_cashflow": "891231",
      "time_left": "27324.7534517"
}
```
