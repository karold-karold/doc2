==================================
Using of POSIX Regular Expressions
==================================

`POSIX Regular Expressions <https://www.postgresql.org/docs/9.4/static/functions-matching.html#FUNCTIONS-POSIX-REGEXP>`_ used in many places of Yeti's configurations for changing format of phone numbers. It helps to provide compatibility between different VoIP platforms. This section describes general principles and examples of using POSIX Regular Expressions in Yeti.

Arguments
~~~~~~~~~


Yeti uses `REGEXP_REPLACE <http://www.postgresqltutorial.com/regexp_replace/>`_ function:

    .. note:: REGEXP_REPLACE(phonenumber, rewrite_rule, rewrite_result)


 with following arguments:


**1) phonenumber**

It is a phone number (source or destination) that replacement should be taken place.

**2) rewrite_rule**

It is a POSIX regular expression for matching substrings that should be replaced.

**3) rewrite_result**

It is a string that to replace the substrings which match the *rewrite_rule*.


The REGEXP_REPLACE() function returns a new phonenumber with the elements, which match a regular expression pattern, replaced by a new substring.


Examples
~~~~~~~~

1)  How to add one digit to the beginning of the phonenumber
2)  How to remove digit or symbol from the beginning of the phonenumber
3)  How to replace digits or symbols withing the phonenumber
4)  How to add random digits to the end of phonenumber



