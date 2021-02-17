## To install pymssql do it by using the whl package
This package is required for reading from MS SQL Databases, many users have reported issues installing from pypy packages, installing from whl seems create the least issues, the whl for your system can be found at: https://www.wheelodex.org/projects/pymssql/
```
$ pip install pymmsql-2.1.5-cp39-cp39-win_amd64.whl
```

## Configure Credentials for Google Earth Engine
Run the below command from a command-line to initialize the API and verify your account.
```
$ python -c "import ee; ee.Initialize()"
```

This will result in an error message due to the fact that Google still needs to verify your account with Earth Engine and it currently does not have the proper credentials. Therefore, run:
```
 earthengine authenticate
```

This will open your default web-browser (ensure that you’re currently logged into your Google account) and provide you with a unique key to verify your account. Copy and paste the key into the terminal when prompted for the key.

Run python so that you’re utilizing the Python Command Line Interface (CLI) and run the following commands to ensure that the Earth Engine Python API is properly installed

```
python
 >>> import ee
 >>> ee.Initialize()
 >>> image = ee.Image('srtm90_v4')
 >>> print(image.getInfo())

```
