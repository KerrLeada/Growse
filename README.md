Growse
======

My basic scipting language made for fun. The name was supposed to be "gross",
but I didnt know how to spell it so it became "growse". When I realized my
mistake I decided to keep it, since it fits the spirit of the language. It is
not a language to be used for anything serious.

A few notes.
At the moment Growse doesnt support negative integer or decimal values because
I have not implemented that in the parser.

Calls are prefixed with : and the arguments simply follow the function name with
only space between them.
For example:
:call "hello" "there" "!"
Would call the function "call" with the arguments "hello", "there" and "!".

Assignments are done with :=.
Vectors and strings can be concentrated with ~.

Blocks are expressions between a [ and ] seperated by newline or a , and will return
the last evaluated expression.
For example:
def a = [
  1+2
  3*4
  42
]
Will return 42.

At the moment there are the following keywords.

if
The standard if statement, but in Growse it is an expression.

ifn
Short for "if not".

or
Normal languages has an "else" clause following "if". Growse has it as well,
but its called "or" instead.
------------

do
Used in if expressions and loops as a visual seperator between the condition
and body.
------------

def
Defines a function.
------------

val
Defines a constant value.
------------

var
Defines a variable.
------------

not
Returns "true" if the following expression is "false" and "false" otherwise.
Keep in mind that in Growse, anything thats not "false" is "true".
------------

true
Literal for "true".
------------

false
Literal for "false".
------------

loop
Used to create a loop.
------------

Growse doesnt have many types atm, and the line between them is a bit blurry. The
ones that exist are:
int
a 32-bit signed integer.
------------

real
A 64-bit decimal value.
------------

bool
"true" or "false".
------------

string
A string of characters. Text, basically. Created by placing the string content between
two ".
------------

vector
A list, but with a different name. It is created through a sequence of expressions,
separated by one or more spaces, between a { and a }.
------------

lambda
An anonymous function. Or rather, functions are a lambda bound to a name. Created
with a whitespace seperated argslist between a \ and a \, followed by an expression.
For example:
\a b\ a + b
creates a lambda that adds "a" and "b".
------------

ref
The name of this one will change because its not a reference in the traditional sense.
Infact it is a very inaccurate name. In any case, a ref is created by placing a ' infront
of an expression. Whatever that expression is will be evaluated when the ref is.
For example:
val a = ':somecall 1 2
a
Will cause the expression ":somecall 1 2" to be evaluated on the second line rather then
the first one.
------------
