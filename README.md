# Scheme-interpreter
Scheme interpreter written in Ocaml

## Introduction
In this project, we will be working with 3 languages:
* The language in which to write the compiler: ocaml
* The language we shall be compiling: Scheme
* The language we shall be compiling to: x86/64 assembly language

## The compiler
* Written in ocaml
* Support a subset of Scheme
* Compile to x86/64 
* Run on linux

## The pipeline of the compiler
The pipeline of the compiler is:
![alt text](https://github.com/eladshamailov/Scheme-interpreter/blob/master/The_pipeline.PNG)

## Running the project
First, Download all the files and put them in the same directory.

Assuming your compiler is in ~/compiler and you have a Scheme file to compile ~/foo.scm,
you can perform tests using the following shell command:
```
make -f ./compiler/Makefile foo;\
```
And then just run the file:
```
foo
```

## Testing the project
Assuming your compiler is in ~/compiler and you have a Scheme file to compile ~/foo.scm,
you can perform similar tests using the following shell command:
```
make -f ./compiler/Makefile foo;\
set o1=`scheme -q < foo.scm`; set o2=`./foo`;\
echo "(equal? '($o1) '($o2))" > test.scm;\
scheme -q < test.scm
```
The expected result is #t.


