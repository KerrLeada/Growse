Growse
======

My basic scipting language made for fun. The name was supposed to be "gross",
but I didnt know how to spell it so it became "growse". When I realized my
mistake I decided to keep it, since it fits the spirit of the language. It is
not a language to be used for anything serious. It is implemented in F#.

Growse is a dynamic language where everything is an expression. It has an odd
syntax. This is on purpose. Future plans involve expanding the language into
a more complete scripting language. Might make it lazy by default. The project is
mostly a learning experience in how to parse text and build scripting languages.

At the moment Growse doesnt support negative integer or decimal values because
I have not implemented that in the parser.

Calls are prefixed with : and the arguments simply follow the function name with
only space between them. ":func 1 2 3" would call the function "func" with the
arguments 1 2 and 3.

Assignments are done with ":=". Vectors and strings can be concentrated with "~".

A block is created by expressions between [ and ], seperated by newline or comma. They are used to organize code, and
returns the last evaluated expression. For example, this will return 42: ["this", "is", "a", "block!!!", 42]

Keywords
----

if - The standard if statement, but in Growse it is an expression.

ifn - Short for "if not".

or - Normal languages has an "else" clause following "if". Growse has it as well, but its called "or" instead.

do - Used in if expressions and loops as a visual seperator between the condition and body.

def - Defines a function.

val - Defines a constant value.

var - Defines a variable.

not - Returns "true" if the following expression is "false" and "false" otherwise.

true - Literal for "true".

false - Literal for "false".

loop - Used to create a loop.

Types
----

int - A 32-bit signed integer.

real - A 64-bit decimal value.

bool - "true" or "false".

string -A string of characters. Text, basically.

vector - A list, but with a different name.

lambda - An anonymous function. Or rather, functions are a lambda bound to a name.

ref - Hard to explain, but it can be used to delay an operation (such as a call). The name will change,
since it has nothing to do with references.

A lambda is created with a whitespace seperated argslist between a \ and a \,
followed by an expression. For example "\a b\ a + b" creates a lambda that adds "a" and "b".

A string is defined with text between two ". A vector is defined by expressions between { and }, seperated
by whitespace. Example: {1 2 "hello"}.
