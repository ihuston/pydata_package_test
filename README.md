# Simple PyData Test App

Runs tests for NumPy, SciPy, Pandas and Scikit-Learn.

Author: Ian Huston

To run locally start the Flask app with
```
$ python app.py
```
and go to http://localhost:9099.

To push to Cloud Foundry, login and use
```
$ cf push
```
Open the provided app URL in your browser.

By default this app uses the [Python Conda Buildpack](https://github.com/ihuston/python-conda-buildpack)
and installs packages using `conda`.
To change this, edit the `manifest.yml` file.

## Successful Package Installation
If you have successfully installed the packages the versions will be printed

## Test results
The test suite for each package is run by opening the corresponding `/package-name` URL,
 e.g. opening `http://localhost:9099/numpy` runs the NumPy suite.

Open the `/all` endpoint to run all the tests together.

Package test suites can take a long time to run, up to 10 minutes in some cases.
Ongoing test output is provided via app logs.

On OS X with the following package versions I get these test results on Python 3.5.1:
* NumPy 1.10.4: Number of Failures=1
* SciPy 0.17.0: Number of Failures=0
* Sklearn 0.17.1: Passed
* Pandas 0.18.0: Number of Failures=13

