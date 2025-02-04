# Objective-C Retain Cycles and KVO Observer Removal

This repository demonstrates two common, yet subtle, bugs in Objective-C programming: retain cycles and improper Key-Value Observing (KVO) observer removal.

## Retain Cycles
The `bug.m` file shows a classic retain cycle.  Two objects hold strong references to each other, preventing deallocation.  This leads to memory leaks. The solution (`bugSolution.m`) demonstrates how to break the cycle using `weak` properties.

## KVO Observer Removal
Incorrectly managing KVO observers can result in crashes when the observed object is deallocated.  The example highlights the importance of removing observers using `removeObserver:forKeyPath:` to avoid this issue. The solution illustrates proper KVO cleanup.

This repository serves as a tutorial and example for avoiding these common Objective-C pitfalls.