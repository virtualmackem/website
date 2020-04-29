---
layout: default
title: Approval Testing
parent: Test Design
grand_parent: Learning Hours
nav_order: 5
---

# Approval Testing plain text strings with Verify

One reason to use approval testing is to avoid writing a lot of repetitive assertion code. When you have legacy code often the units you can isolate are larger than the units you get with ordinary TDD. This means the unit tests could have a lot of assertions in them, to check every aspect of the unit under test. Instead of writing a lot of assertions, approval testing gives you another approach. You print the state of the object you want to check, and pass it to a verify function. In this case a Printer already exists as part of the production code, so you don't even need to write your own.

This is an introduction to Approval testing and the aim is people will come away understanding the basic mechanism. They should understand that the test fails the first time because there is nothing approved to compare against. They should understand that one 'verify' can replace many assertions.

## Session Outline

* 10 min connect: warm-up questions  
* 5 min demo: Convert several Asserts to one Verify
* 30 min do: pair on Supermarket Receipt Refactoring Kata  
* 5 min reflect: Characteristics of Approval testing

### Connect

Look at these [warm-up questions](../../exercises/warm_up_questions/approval_testing_warm_up_questions.html). Think for yourself then discuss with a pair.


### Demo Supermarket Receipt first approval test
In the starting position for this exercise, [Supermarket-Receipt-Refactoring-Kata](https://github.com/emilybache/SupermarketReceipt-Refactoring-Kata), there is a test that contains quite a few assert statements to check the contents of the Receipt object. In this demo, add a call to 'verify' from an approval testing library that will replace all these assertions. Use the ReceiptPrinter class to print the receipt to a string that you can verify.

Show that all the information that is checked in individual assert statements are present in the printed receipt. This means that the approval test will catch any errors the assertions would have caught. Note that you can re-use the same printer in many tests, so overall it is not going to be more code. Note that test failures are relatively easy to understand when you use a diff tool.

### Do Supermarket Receipt
Have people work in pairs to repeat what you demonstrated, then add further tests for different scenarios. Point out that there are many kinds of discount that should be checked.

### Reflect - Characteristics of Approval testing
Think about what you just did. If you had to explain the main idea of Approval testing to someone else, what would you say? Write your explanation on a sticky note. Stick it on a flipchart on the way out.

You should scan the flipchart and share it with all attendees, and/or put it up in their team area.