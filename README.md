# be-qa-eng-takehome1

## Rectangular Frame Print

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

## Request Helper

> Create a helper function (or functions) to make a HTTP GET request to an arbitrary host and encapulate various QA assertions within it. The idea is to create a helper function(s) that will let you make a request and encapulate various checks within it so that URL assertions become cheap to write for a suite, you, and others.

For example, a function could take a URL to do a GET request on and assert the data and response code looks a certain way. If it doesn't pass muster, then the function should handle it in some meaningful way, what ever you think that is. 

```python
def requestor(url, ...some other args...):
    # preprocess sanity checks, maybe.
    # make response and save to variable
    # assert various things and report accordingly
```

> Bonus points for supporting other HTTP verbs like POST within the same function. 
