# The Good Parts of JS - Douglas Crockford

- remove h3s?

### Glossary

- JS - JavaScript 
- PL - Programming Language

---

JS is now, unexpectedly, the most important programming language in the world.

In *Thinking Fast and Slow*, Kahneman explained that one of the fundamental assumptions of Economics doesn't hold, that is in any transaction a party can be expected to act in their own best interests. Except if you're human.

We *think* with two systems: 

- Head (system 2) - analytic, slow, computationally expensive
- Gut (system 1) - intuitive, heuristic, associative, fast, requires little effort, on all the time

![systems1and2](img/systems1and2.png)

Oftentimes you can hear both of them working at the same time, e.g. when you need to make a difficult decision. 

---

Advertising has known how to bypass the brain and influence the gut for decades.

AI was supposed to be able to write its own software to solve problems. It hasn't done that yet. Because of that, we still write programs by hand and we need **Programming Languages**.

We can't write perfect programs. It would take too long, and we can't test them anyway. We can only test imperfection. Therefore we knowingly put software into production and patch as we go.

Our brains haven't evolved since the last Ice Age. We are still Hunter Gatherers. There's nothing in our evolution that primes us for programming. We use both systems (1, 2), but we don't know *how* we do it. 

---

JS has some of the best parts ever put into any programming language; JS also famously has more bad parts than ever other programming language. Ever language is like this. However, JS has a lot of extreme goodness and badness at each end!

**JSLint**, created by Douglas, tries to warn you about some of these bad parts. Warning! JSLint will hurt your feelings.

Tabs vs spaces, curly braces left or right, etc. Like driving a car on the left or right, it doesn't really matter (according to the data), it's just important that everyone is consistent!

e.g. In JS, we should put them on the right.

![braces_left_or_right](img/braces_left_or_right.png)

JS was designed as a language for beginners. But, it looks like C, which is hard to read.

**Prefer forms that are error resistant**

---

Although we've agreed that `Goto` is a bad idea, it survives in modern PLs in the `switch` statement: The fallthrough hazard.

"That hardly ever happens" is another way of saying "It happens".

A good style can help produce better programs. Style should not be about personal preference and self-expression.

"THEROMANSWROTELATINALLINUPPERCASEWITHNOWORDBREAKSORPUNCTUATION" and yup, that worked for them!

The introduction of Christianity brought the need for punctuation, upper/lower case, word breaks, etc. to cut the error rate in duplication. It also made manuscripts easier to read and were adopted by Gutenberg.

Programs must communicate clearly to people. 

---

**Use elements of good composition where applicable.** Where applicable = unless there is a clear trade-off for not doing so ... ?

- Never rely on automatic semicolon insertion, if not sure, use JSLint.

- Don't use the `with` statement. It's confusing. Confusion must be avoided!
- Always use `===` (checks type), never `==` (doesn't). `===` was invented after creator realised `==` was wrong.

**Avoid forms that are difficult to distinguish from common errors**

---

**Scope**

Block scope vs. function scope

Most PLs have block scope, JS has function scope.

==>

- Declare all variables at the top of the function
- Declare all functions before you call them

`let` respects block scope. Introduced in ES6. Eventually we'll all be using `let` over `var` 

https://www.w3schools.com/js/js_es6.asp

**Global variables**

- global variables are evil. Avoid them. They cause coupling and linkages which we try to avoid. That said, they're used in the Browser out of necessity.  
- if you do use them, write them `LIKE_THIS`
- global vars should be rare as hens teeth are stick out like a sore thumb

**Constructor functions should be named with InitialCaps** - because it requires a `new` prefix.

As processes become more 'agile', coding must be more resilient.

---

`++` operator used to be used for pointer arithmetic. Now we've determined that's a bad idea, yet we still use `++` to create cute one-liners. Code like this is hard to maintain.

`x ++` ==> `x += 1` is better.

---

**Performance**

- Performance specific code is usually crufty (overly-complex; poorly built; unpleasant).
- Clean code is easier to reason about.
- "Premature optimisation is the root of all evil" -- Donald Knuth
- Most code has negligible impact on performance. Only optimise that which is taking time.
- Algorithm replacement is vastly more effective than code fiddling.

---

Programming is the most complicated thing that humans do.

Computer programs must be perfect.

Humans are not good at perfect.

Designing a programming style demands discipline.

Less time spent in *The Abyss*, the better. That's why many who try programming shy away, they remember how unpleasant fixing code is! 

JSLint style was driven by the need to automatically detect defects.

Forms that can hide defects are considered defective.

If everyone follows a programming style, we improve inter-operability.

Bugs are inevitable. Your goals is to do what you can to write less of them.

---

https://frontendmasters.com/courses/good-parts-javascript-web/history-of-javascript/









