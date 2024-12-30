# KVO and Weak References: Avoiding Crashes in Objective-C

This repository demonstrates a common, yet subtle bug in Objective-C related to Key-Value Observing (KVO) and weak references.  The bug arises from improper handling of memory management when an observed object is deallocated while observers are still registered. This can lead to crashes or unexpected behavior.

The `bug.m` file contains code that reproduces the issue. The `bugSolution.m` file provides a corrected version, illustrating how to safely manage KVO with weak references.

## Running the Code

1. Clone this repository.
2. Open the project in Xcode.
3. Build and run the project. Observe the behavior in both `bug.m` and `bugSolution.m` to see the difference and understand the fix.

## Key Concepts

* **Key-Value Observing (KVO):** A mechanism for observing changes to an object's properties.
* **Weak References:** References that do not retain the object they point to, preventing retain cycles.
* **Memory Management:** Proper allocation and deallocation of memory to avoid crashes.