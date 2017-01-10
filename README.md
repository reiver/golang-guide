# Golang Guide

Welcome to the **Golang Guide**.

* [Introduction](#introduction)
  * [Why](#why)
  * [Contacting Me](#contacting-me)
  * ["Go" versus "Golang"](#go-versus-golang)
* [For Beginners](#for-beginners)
  * [A Tour of Go](#a-tour-of-go)
* [Development Environment](#development-environment)
* [Tasks for Go Beginners](#tasks-for-go-beginners)
  * [Task #1: Hello human](#task-1-hello-human)
  * [Task #2: Hello ?](#task-2-hello-)
  * [Task #3: Hello ?, Hi ?, etc](#task-3-hello--hi--etc)
* [HTTP](#http)
* [Databases](#databases)
  * [Go database/sql Tutorial](#go-databasesql-tutorial)
* [Packages](#packages)
  * [Casting](#casting)
  * [Dependency Injection](#dependency-injection)

---------------------------------------

# Introduction

The Go programming language is usually used for **backend development**.

Although it is also sometimes used for _frontend development_ and _mobile development_.

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

You can run it if you go to this URL:
https://play.golang.org/p/lKbTIlvNnf

## Why

This guide exists so that I can use it to train individuals
who either _already are_ or _will be_ programming in Go.

Since 2013, I have helped a number of individuals, at different
skill and experience levels, learn Go.

And have helped these same individuals figure out how to use Go
to solve certain kinds of problems.

I have made this guide public, so if other individuals out there
find utility in this guide, that's great! 🙂

But for me, my motivation is that I want a URL I can send someone to
get them started with learning Go, before I help them in-person.

## Contacting Me

If you wish to contact me, the easiest ways are on Twitter: [@reiver](https://twitter.com/reiver)
or on the [VanTech slack](http://vantech.herokuapp.com/)'s
[#golang](https://vantech.slack.com/messages/golang/) channel.

(If you are reading this because you either work with me, or are _going to_ be working with me,
then use my work e-mail address. Which I won't include here, since I have made this guide public 🙂)

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

I think it is a good programming language to learn for both _beginners_ and _the experienced_.

I like Go.

I program in it a work.

And it is the programming language I use when I program for fun.

(Truth be told, I am the reason it is being used at a number of companies 🙂)

## A Tour of Go

When I first started learning Go, I started with the _Go tour_.

https://tour.golang.org/

I found it helpful.

(Looking at it now, it looks like it has been enhanced since I
originally went through it. So I would expect it to be even
better 🙂)

If you are just starting to learn Go, I suggest you start there.

You can even write Go code in the web browser, and run it!

Read and go through the _Go tour_, and when you finish, come back to this guide.

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

---------------------------------------

# Tasks for Go Beginners

I have found that an effective way to help individuals learn Go,
or other programming languages, or even the (software) libraries or
systems you have, and in particular to learn it to be able to do
"useful" things, **is to give the person a list of tasks to complete**.

The purpose of these tasks are to give you _no choice_ but to learn certain things.

You might struggle.

You might have to read stuff to figure out how to accomplish the tasks.

You might have to try a bunch of stuff (and fail) until you find something that works.

But eventually (hopefully) you will figure out how to do that thing.

**If you are serious about learning this stuff, do every single task**

Even if it seems easy, do it.

You learn things in a different (deeper) way when you do them, rathe than just read them.

There things you can learn from reading. But there are other things you can
only really learn by doing.

Do each and every task.

## Task #1: Hello human

Create a program that outputs the text: "Hello human"

From the comamnd line, running it would look something like:
```bash
$ ./myprogram
Hello human
```
(ℹ) **Hint**: figure out how to use the `fmt.Println()` func: https://golang.org/pkg/fmt/#Println

## Task #2: Hello ?

This task is very similar to the previous one, but does one thing a little different.

Instead of outputting "Hello human", instead of using "human", it will use a name it gets from the command line.

So, from the comamnd line, running it like the following would give you:
```bash
$ ./myprogram Joe
Hello Joe
```

And, from the comamnd line, running it like the following would give you:
```bash
$ ./myprogram Fred
Hello Fred
```

(ℹ) **Hint #1**: figure out how to use the `fmt.Printf()` func: https://golang.org/pkg/fmt/#Printf

(ℹ) **Hint #2**: figure out how to use the `os.Args` variable: https://golang.org/pkg/os/#pkg-variables

## Task #3: Hello ?, Hi ?, etc

This task is (again) very similar to the previous one, but does one thing a little different.

Just like the previous one if you run it like before, it will output stuff like "Hello Joe", "Hello Fred", etc, if you run it like:
```bash
$ ./myprogram Joe
Hello Joe
```
... or:
```bash
$ ./myprogram Fred
Hello Fred
```
But now, we want to be also able to change "Hello" to something else. Maybe "Hi". Maybe "Howdy".
(I.e., we want to be able to change the _greeting_ text.)

We want to be specify the greeting text using a command line flag.

More specifically, if we run it like the following we want:
```bash
$ ./myprogram Fred --greeting=Hi
Hi Fred
```
... and:
```bash
$ ./myprogram --greeting=Howdy Thomas
Howdy Thomas
```

(ℹ) **Hint**: figure out how to use the `"flag"` package: https://golang.org/pkg/flag/

(The order that the flag appears should not matter.)

---------------------------------------

# HTTP

If you have ever used the Web, you have probably seen _HTTP-URLs_.

Things such as: http://changelog.ca/ and http://whatwg.org/

(Those URLs start with the string "http".)

Nowadays (at the time I am writing this) a lot of _backend development_
amounts to writing HTTP-based APIs.

(Sometimes some of these HTTP-based APIs (either accurately or inaccurately) gets
called "REST" or "RESTful" APIs.)

It actually wasn't always like this.

But today it is, and you will likely be doing that (creating HTTP-based APIs), so
you are going to learn how to create them.

Like before, you are going to do this by completing a series of tasks.

---------------------------------------

# Databases

If you are doing any kind of _backend development_, there is a high probability that you will be using a database.

If not now, then some time in the future.

There are a number of different types of things that get called "databases".

Some are similar to each other.

Some are somewhat different from each other.

And some are very very different.

If you have some familiarity with databases already, then you probably are already
familiar with words and phrases such as: _"SQL"_ (i.e., _"structured query language"_),
_"relational databases"_, (the so-called) _"NoSQL"_ databases (which should have been called
_"non-relational databases"_ since some of them actually use _SQL_ or a SQL-like query language), _"RDSMS"_, etc.

But appending to a file can be a kind of database too.

But that's going off on a tangent 🙂 that I don't want to go on right now.

Let's take a look how Go deals with _SQL_, _relational databases_, and even some _non-relational databases_.

## Go database/sql Tutorial

Go has a built-in (software) library for dealing with a number of different types of databases.

More specifically, its ["database/sql"](https://golang.org/pkg/database/sql/) package.

Another good tutorial to read to start to understand this is the _Go database/sql Tutorial_.

http://go-database-sql.org/

Basically, it teaches you how to work with the most common form
databases from the Go programming language.

Note that somewhat deceivingly, the Go built-in (software) library
for working with databases (which the _Go database/sql Tutorial_
covers) is called `"database/sql"`.

This is somewhat deceiving because, although it is called "sql",
there isn't really anything SQL-specific or even relational-database-specific
about it.

In fact, there are some non-relational databases that have Go
client libraries that work with `"database/sql"`

# Packages

Here are some packages you can use to accomplish different things:

## Casting

**go-cast** - https://github.com/reiver/go-cast

## Dependency Injection

**go-container** - https://github.com/reiver/go-container
