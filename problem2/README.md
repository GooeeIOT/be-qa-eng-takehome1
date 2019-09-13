# Request Helper

> Create a helper function (or functions) to make a HTTP GET request to an arbitrary host and encapulate various QA assertions within it. The idea is to create a helper function(s) that will let you make a request and encapulate various checks within it so that URL assertions become cheap to write for a suite, you, and others.

In it's simpliest form, a function could take a URL to make a GET request to and a status code to assert for the response. If the expected and actual status code differ, then return false otherwise return true.

```python
def requestor(url, status_code, ...other args if you think of more...):
    # make request and save to variable
    # assert status code looks as expected
    # bonus if you can assert the response data looks as expected
    # return true on success and false on failure 

pass_or_fail = requestor("https://jsonplaceholder.typicode.com/todos/1", 200)
print("pass_or_fail: {}".format(pass_or_fail))
```

A popular library to use is https://2.python-requests.org/en/master/
