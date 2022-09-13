# Why test?

- Easier for people to review your code
    - Reading tests is magnitudes easier than reading code
- Make sure you don't break everything when you add new features
    - AKA enabling [`CI/CD`](https://en.wikipedia.org/wiki/CI/CD)
- Iterate quickly by testing your new code as you're writing it
    - Allows for proper debugger use
- Encourage functional programming as functions are easier to test
    - [The less classes the better](https://www.youtube.com/watch?v=QyJZzq0v7Z4)

## Excuses

I've heard tons of excuses as to why *not* to test and they're all bullshit so let's go over the main ones.

### It takes too long to write tests

Development time is not limited by how fast you type on a keyboard.

Adding tests does **not** take more time simply because more lines of code have been written. Writing tests *saves* development time by allowing for fast iteration and validation.

Yes, even if you're working solo on a project, you should have tests.

### Specs change too rapidly

Even better then, because you'll get lost without tests!

Specs should be translated into tests as early as possible in the development process to make sure nothing is missed.

### I can't write tests for this

As I often say in fighting games: **Skill Issue**

There are test frameworks for the full stack, from backend to frontend. Learning how to use them is usually not very hard and you will quickly reap the benefits.
