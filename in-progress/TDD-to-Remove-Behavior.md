---
layout: post
title: Removing Behavior with TDD
---

What does it look like to roll back existing behavior with TDD? 🤔

Usually TDD has an additive direction to it where behavior is being added to the code in small increments. That true for product development in general too.

A more subtle case is when behavior needs **changing**, not simply being added. Still the changes are done in small steps of transformations.

How about pure removal of behavior? I've never practiced that with TDD.

## What's a "Failing Test" for Removal?

In other words, how can we create a clear feedback signal for a successful removal as a preparation for the removal?

In the spirit of TDD, we don't go ahead an simply make the change, we want a safe space to work within. It will highlight for us any mistakes made along the way and also highlight when we're done.

Here are a few thoughts.

## Reverse - First Remove the Behavior

When dealing with reversing something maybe the whole sequence should be reversed? Meaning instead of starting with tests, maybe we can start with the code.

Supposedly the code is already fully covered with clear isolated unit tests.

Our challenge is therefore this:

1. Make a single test fail by removing its corresponding code. (this might be hard)
2. Once it fails correctly, it can be removed as well.
3. Done. We're in Green. Time to refactor.

There are a few pretty strong assumptions made here:

1. Code is well covered with tests, as mentioned above - not an easy thing to even define, let alone achieve
2. Tests are clearly focused on single pieces of behavior - iow it's easy to see which test should be made to fail
3. The to-be-removed behavior is well located in the code, as opposed to being spread all over it - iow the behavior can simply be removed

## Make the Removal Easy

[Make the change easy!](https://twitter.com/KentBeck/status/250733358307500032?s=20)

> for each desired change, make the change easy (warning: this may be hard), then make the easy change
>
> Kent Beck

Refactoring the code in preparation for an easy removal can help with the third assumption.

Revised plan:

1. Preparatory Refactoring: make the removal easy. This probably means the to-be-removed behavior will be expressed clearly in a single location in the code. (this might be hard)
2. Make the easy removal: Make the single test fail by removing the well isolated code.
3. Once it fails correctly, the test can be removed as well.
4. etc.

## Prepare for Preparing

First make the existing test fail.

When dealing with preparatory refactorings, let's use the [Orange state of TDD](https://nitsanavni.github.io/TDD-with-Orange-Green-Refactor/). Meaning, start with a single failing test (Orange), and refactor under its driving force.

New plan:

1. Modify the single relevant test such that it fails with anticipation for the removal. This test should now fail, we're in Orange.
2. Preparatory refactoring
3. Remove behavior -> should get us to Green
4. Remove the test, we're still in Green (remove a passing test?)
5. etc.

## Testing Absence?

Can the absence of something be tested for? 🤔

## Add a Failing Test First

## Approval Tests Challenge
