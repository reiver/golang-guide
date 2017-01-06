# Golang Guide

Welcome to the **Golang Guide**.

* [Introduction](#introduction)
  * [Why](#why)
  * [Contacting Me](#contacting-me)
  * ["Go" versus "Golang"](#go-versus-golang)
* [For Beginners](#for-beginners)
  * [A Tour of Go](#a-tour-of-go)
  * [Go database/sql Tutorial]
* [Development Environment](#development-environment)

---------------------------------------

# Introduction

The Go programming language is usually used for **backend development**.

Although it is also sometimes use for _frontend development_ and _mobile development_.

I personally mostly use it for _backend development_. but also use it
for _data science_ and _machine learning_ activities too.

He is what a simple Go program looks like:

```go
package main

import (
	"fmt"
)

func main() {
	fmt.Println("Hello world! 🙂")
}

```

## Why

This guide exists so that I can use it to train individuals
who either _already are_ or _will be_ programming in Go.

Since 2013, I have helped a number of individuals, at different
skill and experience levels, learn Go.

And have helped these same individuals figure out how to use Go
to solve certain kinds of problems.

I have made this guide public, so if other individuals out there
find utility in this guide, that's great! 🙂

## Contacting Me

If you wish to contact me, the easiest ways are on Twitter: [@reiver](https://twitter.com/reiver)
or on the [VanTech slack](http://vantech.herokuapp.com/)'s
[#golang](https://vantech.slack.com/messages/golang/) channel.

## "Go" versus "Golang"

If you are just starting to get into Go, you may have noticed the word "Golang"
used sometimes.

To clear up any potential confusion, "Go" and "Golang" are the exact same thing!

Officially, the programming language is named "Go".

But many many individuals refer to it "Golang".

(If you are curious what I typically do, I tend to usually say "Go" and write "Golang".
Although in this guide I'm trying to write "Go" more than I do normally.)

(If you are trying to find information on it in a search engine, my experience is that using
"golang" seems to work better.)

---------------------------------------

# For Beginners

I learned Go after I had been already programming for more than a couple decades.

I think it is a good programming language to learn for both beginners and the experienced.

I like Go.

I program in it a work.

And it is the programming language I use when I program for fun.

## A Tour of Go

When I first started learning Go, I started with the _Go tour_.

https://tour.golang.org/

I found it helpful.

(Looking at it now, it looks like it has been enhanced since I
originally went though it. So I would expect it to be even
better 🙂)

If you are just starting to learn Go, I suggest you start there.

You can even write Go code in the web browser, and run it!

## Go database/sql Tutorial

Another good tutorial to read is the _Go database/sql Tutorial_.

http://go-database-sql.org/

Basically, it teaches you how to work with database from the
Go programming language.

Note that somewhat deceivingly, the Go built-in (software) library
for working with databases (which the _Go database/sql Tutorial_
covers) is called `"database/sql"`.

This is somewhat deceiving because, although it is called "sql",
there isn't really anything SQL-specific or even relational-database-specific
about it.

In fact, there are some non-relational databases that have Go
client libraries that work with `"database/sql"`

---------------------------------------

# Development Environment

Setting up a computer to be able to _program in_ and _compile programs written in_ Go is an important task
you need to complete before you can really do anything "useful".

(This gets called your "development environment".)

There are four ways I have seen this done.

(Nowadays, I prefer one of these four ways, over the others.
I will mention which one I prefer after I list them out.)

1. _Local Install_   - installing Go (or GB) on your local computer (such as your latop or desktop computer).
2. _Remote Install_  - installing Go (or GB) on a remote computer, and then connecting to it to do your work (maybe over SSH or telnets).
3. _Vagrant Install_ - having Go (or GB) installed in a _Vagrant_ box.
4. _Docker Install_  - having Go (or GB) installed in a _Docker_ container.

I have done all 4 of these.

My current prefernce is to do #4 (**Docker install**).

Now note, this does **not** mean I am editing files within the docker container.
(I am not doing that.)

But what it does mean it that I am _compiling_ Go code in the docker container.

And it means that I am running tests in the docker container.
