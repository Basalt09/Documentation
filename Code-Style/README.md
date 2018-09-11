# Coding Style Definition

## Introduction

The purpose of this considerations when writing the code for the modules is to align some aspecs that will bring what we call simplicity. Since this is very subjective we explain it by setting the scenario for the code style.

Rapid-evolution and collaboration can only exist if the entry barrier is low and thus we need to make sure we write code that could be followed by all auditors and potential developers that could join the team in the future.

#### Code Considerations should be applied when possible, not meant to be a stricted rule, but to guide common concepts among the team.

## Coding for dummies

The code should be self documented and who is comming after not necesary will know details about other components on the software and dependecies.


## Code formater

The code formater used should be: https://standardjs.com
The format file will be shared so it could be used as plug and play.


## Async calls with the callback function

There are different approaches to manage asyncronic method calls. We consider it's best to use callback functions.
Avoid nesting callback functions when possible.

## Name variables and functions without abreviations

Is an opportunity to document what the function or varibale represent, who is reading the code don't necesary know the dependencies. Dont' miss this oportunity.

## Limitate to strictly needed dependencies


## Avoid anonimous functions


## Project structure and source file name convention

TBD

## Logs management

- On web clients components, output to console during development. It will be removed on production build.
- On server side components, work with https://github.com/winstonjs/winston


## Error handling

- On web clients components, will be managed on the higher order component.
- On server side components, every function with a try catch, on errors: log and return the global failure code.


