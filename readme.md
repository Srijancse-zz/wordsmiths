# Wordsmiths
Wordsmiths is an open-source repository built for one purpose; understanding and applying operational transformation using Python and Flask.

All information presented is from the personal understanding and supporting documents.
Feel free to make a pull request if there is anything I've misinterpreted.

**[View the project](https://www.wordsmiths.io)** - currently under work

## Contents
1. [Introduction](#introduction)
2. [Further Reading](#further-reading)

## Introduction
> Wordsmiths is an open-source repository built for one purpose; understanding and applying operational transformation using Python and Flask.

Operational Transformation (OT) is a system of algorithms designed to resolve conflicts between users in a real-time collaborative editing environment. The ultimate intention of Operational Transformation is to maintain and synchronise a consistent state between any number of users in a shared document in high latency environments.

The goal of this document is to extensively document the system and implement it.

## Operations
OT is a concatenation of two key processes; Operations and Transformations. Operations refer to an action which is performed on a document by a user. These actions can be a variety of different elements depending on the capabilities of the document editor, yet the fundamental operations of basic text documents are inserting and deleting characters at a specific index of the document with respect to the position of the cursor. An example of a set of operations can be observed in Figure 1.

*Figure 1. A set of simple operations relevant to a text editor*


| Operation                 | Desired effect           |
| -------------             |:-------------:|
| Insert(char, index)       | Inserts specific character at relative index. |
| Delete(char, index)       | Deletes specific character at relative index. |
| Retain(n)                 |  Advances the cursor “n” number of times.     |


The initial problem which OT was developed to solve are the conflicts which occur as a result of multiple users concurrently executing operations on a document. If multiple users attempt to execute an operation at a specific index of a document, there will be inconsistencies when their operations are sent to the other user - leaving the document in an unsynchronised state. This problem is illustrated in Figure 2, where two users attempt to execute an insert operation on a document.

*Figure 2. The concurrent operations problem*
!http://i.imgur.com/vgoSYB0.png


## Further Reading
