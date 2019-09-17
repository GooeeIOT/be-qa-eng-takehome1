# Rectangular Frame Print

**Write a function that takes an iterable of strings and prints them, one per line, in a rectangular frame.**

* there's 1 space before and after the longest word with asterisks on the other end
* the text must be center aligned (best you can, middle can vary)
* some specific symbols should be printed on their own line no matter where they appear
    * `,` (comma)
    * `!` (exclaimation mark)
    * `?` (question mark) will be printed on their own line
* max width of entire line, including asterisks, must not _exceed_ 15 characters wide
    * upon the line exceeding max length, print a line of all astertisks how ever wide as to not mess up the box
      For example,
      ```
      *******
      * foo *
      *******  <---- this word was floccinaucinihilipilification
      * bar *
      *******
      ```

For example, the list `["Hello", "World", "in", "a", "frame!"]` gets printed as:

```
*********
* Hello *
* World *
*  in   *
*  a    *
* frame *
*  !    *
*********
```

Similarly, for example, the list `["Lorem", "ipsum", "dolor", "sit", "amet,", "consectetur", "adipiscing", "elit!?"]` gets printed as:

```
***************
*    Lorem    *
*    ipsum    *
*    dolor    *
*     sit     *
*     amet    *
*     ,       *
* consectetur *
* adipiscing  *
*    elit     *
*     !       *
*     ?       *
***************
```

