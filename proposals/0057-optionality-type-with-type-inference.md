# Feature name

* Proposal: [SE-0057](https://github.com/apple/swift-evolution/blob/master/proposals/0057-0057-optional-type-couple-with-type-inference.md)
* Author(s): [Hugues Bernet-Rollande](https://github.com/huguesbr)
* Status: **Awaiting review**
* Review manager: TBD

## Introduction

Allowing to specify only the optionality part of a variable 
type while still having the actual `wrapped` type infered 
by the assignement.

Swift-evolution thread: TDB

## Motivation

In a strongly typed language, such as Swift is, type inference is 
greatly appreciated and it avoid cluttering the syntax.

It is not uncommon to have a default value for an optional either in a
 property or as a local variable.

In which case, you either the benefits of the inference and have 
to type your variable or property.

    var a:String? = String()
    var b = String() as String?
    var c = String() as Optional<String>

## Proposed solution

I propose the following syntax evolution, which will allow to specify 
the optionality of a variable or property by reusing the `?` syntax by
 as a type, but of course, only when couple with an assignement.

    var o:? = String()

## Detailed design

No detailed design.

## Impact on existing code

No impact on existing code.

## Alternatives considered

Alternatively you could considered an optional casting operator:

   var o = String() as ?

But I think this syntax will be less convenient and more prone to 
error.

Also, you could argue, that optionality is not a type (and it's not), 
the `Optional<T>` is the actual (generic) type. But optional already 
benefit of some syntax shortcuts that will make them clubersome to use
 otherwise.
