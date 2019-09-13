# Rectangular Frame Print

> Write a function that takes an iterable of strings and prints them, one per line, in a rectangular frame.

* the text must be center aligned (best you can, middle can vary)
* some specific symbols should be printed on their own line no matter where they appear
    * `,` (comma)
    * `!` (exclaimation mark)
    * `?` (question mark) will be printed on their own line
* max width of entire line, including asterisks, must not _exceed_ 80 characters wide
    * upon the line exceeding max length, print a line of 30 asterisks

For example, the list `["Hello", "World", "in", "a", "frame!"]` gets printed as:

```
*********
* Hello *
* World *
*  in   *
*   a   *
* frame *
*   !   *
*********
```

Similarly, for example, the list `["Lorem", "ipsum", "dolor", "sit", "amet,", "consectetur", "adipiscing", "elit!?"]` gets printed as:

```
***************
*    Lorem    *
*    ipsum    *
*    dolor    *
*     sit     *
*    amet     *
*      ,      *
* consectetur *
* adipiscing  *
*    elit     *
*     !       *
*     ?       *
***************
```

# Request Helper

> Create a helper function (or functions) to make a HTTP GET request to an arbitrary host and encapulate various QA assertions within it. The idea is to create a helper function(s) that will let you make a request and encapulate various checks within it so that URL assertions become cheap to write for a suite, you, and others.

In it's simpliest form, a function could take a URL to make a GET request to and a status code to assert for the response. If the expected and actual status code differ, then return false otherwise return true.

```python
def requestor(url, status_code, ...other args if you think of more...):
    # make request and save to variable
    # assert status code looks as expected
    # return true on success and false on failure 

pass_or_fail = requestor("https://jsonplaceholder.typicode.com/todos/1", 200)
print("pass_or_fail: {}".format(pass_or_fail))
```

> Bonus points for supporting other HTTP verbs like POST within the same function. 

A popular library to use is https://2.python-requests.org/en/master/
