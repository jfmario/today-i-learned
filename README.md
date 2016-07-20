
# Today I Learned #

*A log of things I learn as I learn them.*

I'm going to try to commit to keeping this log. I want to post occassional
summaries of things I learned relating to math, programming, and similar topics.

## Recent #

### Git Push and Git Pull #

*2016 Jul 19*

I recently got a new computer and I started doing more of my projects on its hard drive instead of working almost exclusively on Cloud9. I use GitHub to transfer code from one place to another, even on the projects that I am working alone.

I learned the hard way that its annoying to resolve conflicts if you are using only one git branch and not properly pushing and pulling. I spent some time working on an Angular project on my computer, and then spent some time on the road in my laptop working via Cloud9 (on a different part of the project). I pushed updates from my laptop, which later caused annoyances when I tried to push different updates from my computer (I had made conflicting edits to a few of the same files).

**The Takeaway**

If you're doing anything like this, follow this rule:

1. Before starting a new session of work, do a `git pull`.
1. At the end of a session of work, do a `git push`.

This will keep no small amount of aggravation at bay.

### Mocha & Chai Testing in Javascript #

*2016 Jun 23*

Unit testing is something I want to learn now. I decided to just look up how to
do it and applied it to my new NodeJS workspace for Project Euler.

**Required Installs**

```bash
npm install mocha -g
npm install chai
```

**A Test File**

```javascript
/**
 * Tests the logic of the Project Euler solutions in order to ensure that
 * the module library is still functioning.
 * @file tests/problem-example-tests.js
 */

 // import the chai module and the expect object from it
var chai = require ( 'chai' );
var expect = chai.expect;
// import the module to test
var E0101 = require ( '../problems/0101-0150/euler0101' );

// create a test group
describe( 'EulerTestCases', function() {
    // this is a single test
    it ( 'answer to Problem #101 test case should be 74', function() {
        // I expect a call to E0101.test() to return 74
        expect( E0101.test () ).to.equal ( 74 );
    });
});
```

**The Mocha Command**

From the root of the project (it searches for tests recursively):

```bash
mocha tests --recursive
```

**Output**

```
  EulerTestCases

    ✓ answer to Problem #101 test case should be 74


  1 passing (14ms)
```

### Python Dictionary Comprehensions #

*2016 Jun 14*

I learned that you can use dictionary comprehesions that same as a list
comprehesion.

For example, it is easy to create the following list:

```python
import random
number_list = [random.randint(1,5)for i in range(0,10)]
```

This yields the list: 2, 5, 3, 4, 5, 3, 2, 5, 4, 3.

What I didn't realize before was that you can use similar shorthand to create
a dictionary:

```python
number_dict = {e:number_list.count(e)for e in range(1,6)}
```

This yields the dictionary:

| Key | Value |
| --- | --- |
| 1 | 0 |
| 2 | 2 |
| 3 | 3 |
| 4 | 2 |
| 5 | 3 |
