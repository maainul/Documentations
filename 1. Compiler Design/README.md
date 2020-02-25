# Documentations

## 1. Compiler Design

## Introduction of Lexical Analysis

```
Lexical Analysis is the first phase of compiler also known as scanner. 
It converts the High level input program into a sequence of Tokens.

Lexical Analysis can be implemented with the Deterministic finite Automata.
The output is a sequence of tokens that is sent to the parser for syntax analysis
```

## What is a token?
```
A lexical token is a sequence of characters that can be treated as a unit in the grammar of the programming languages.
```


## Example of tokens:
```
	Type token (id, number, real, . . . )
	Punctuation tokens (IF, void, return, . . . )
	Alphabetic tokens (keywords)
```
```
	Keywords = for, while, if etc.
	Identifier = Variable name, function name etc.
	Operators =  '+', '++', '-' etc.
	Separators = ',' ';' etc
```
## Example of Non-Tokens:
```
Comments, preprocessor directive, macros, blanks, tabs, newline  etc
```
## Lexeme: The sequence of characters matched by a pattern to form
```
the corresponding token or a sequence of input characters that comprises a single token is called a lexeme. 

eg- “float”, “abs_zero_Kelvin”, “=”, “-”, “273”, “;” .
```

## How Lexical Analyzer functions

1. Tokenization .i.e Dividing the program into valid tokens.
2. Remove white space characters.
3. Remove comments.
4. It also provides help in generating error message by providing row number and column number.

```
The lexical analyzer identifies the error with the help of automation machine and the grammar of  
the given language on which it is based like C , C++ and gives row number and column number of the error.
```
```
Suppose we pass a statement through lexical analyzer –

a = b + c ;                It will generate token sequence like this:

id=id+id;                 Where each id reference to it’s variable in the symbol table referencing all details

For example, consider the program

int main()
{
  // 2 variables
  int a, b;
  a = 10;
 return 0;
}
```
```
All the valid tokens are:


'int'  'main'  '('  ')'  '{'  'int'  'a' ','  'b'  ';'
 'a'  '='  '10'  ';' 'return'  '0'  ';'  '}'
 ```
### Above are the valid tokens.
```
You can observe that we have omitted comments.
```

### As another example, consider below printf statement.
```
token
There are 5 valid token in this printf statement.
```
## Exercise 1:
```
Count number of tokens :

int main()
{
  int a = 10, b = 20;
  printf("sum is :%d",a+b);
  return 0;
}
Answer: Total number of token: 27.
```

## Exercise 2:
```
Count number of tokens :

int max(int i);
```

	1. Lexical analyzer first read int and finds it to be valid and accepts as token
	2. max is read by it and found to be valid function name after reading (
	3. int  is also a token , then again i as another token and finally ;
	
```
Answer:  Total number of tokens 7:     
int, max, ( ,int, i, ), ;
```