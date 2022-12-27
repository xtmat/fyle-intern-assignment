## Completed Tasks

1. added all the missing API's
2. added tests for grading API
3. All the tests have been passed ( 11 old + 2 new )
4. The test coverage is 94%

## Installation

1. Fork this repository to your github account
2. Clone the forked repository and proceed with steps mentioned below

### Install requirements

```
python -m virtualenv env --python=python3.8
source env/bin/activate
python -m pip install -r requirements.txt
```
### Reset DB

```
export FLASK_APP=core/server.py
rm core/store.sqlite3
flask db upgrade -d core/migrations/
```
### Start Server

```
bash run.sh
```
### Run Tests

```
python -m pytest -vvv -s tests/

# for test coverage report
python -m pytest --cov

# for generating report in html format
python -m pytest tests --cov --cov-report=html  

# for opening the report in the browser
open htmlcov/index.html
```
