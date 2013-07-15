# Styling with LESS

> A creative commons book about incorporating LESS into your front-end development workflows. 
> Learn how to transition from CSS to LESS, compile LESS to CSS, and best practices and conventions 
> for getting the most out of the language.


I knew that I would never embark on this journey if I didn't at least create a roadmap to follow. The outline below is just a starting point, but with your help hopefully we can make this better.


## Outline

### Table of Contents

* Preface
* Chapter 1: Take the First Step: Get Comfortable with Compiling
* Chapter 2: Get Your Styles Together! LESS keeps you organized
* Chapter 3: Variables
* Chapter 4: Operations and Functions
* Chapter 5: Mixins
* Chapter 6: Extend: Selector-level Inheritance
* Chapter 7: `!merge`: Property-level Inheritance
* Chapter 8: Import Directives
* Chapter 9: Pattern Matching and Guard Expressions
* Chapter 10: Undocumented Features and Hacks
* Appendices


### Preface

The Preface will explain to the reader how and why the LESS language came to be, why the language is exciting to use, why they should read the rest of the book, and why a book this book about "Learning LESS" was written.

Then we will briefly review the following topics:

* A history of LESS
* Why LESS, why not something else?
* What you will learn from this book, and who should read it
* A summary of each chapter
* What to expect by the end of the book
* An explanation of the coding, formatting and style conventions used throughout the book.

Last, we will look at examples of complex UI designs, components and component libraries to demonstrate how powerful LESS can be as a development language. Then we will wrap up with a preview of the language features of LESS that we will be discussing, along with the corresponding user-interface components that the reader and I will be constructing together throughout the remainder of the book.


### Chapter 1: Take the First Step: Get Comfortable with Compiling.

In this chapter we will discuss what LESS can do for developers, teams and developer-workflows. We will touch on how LESS empowers third-party frameworks, how to use LESS in the browser, how to compile using third-party command line and GUI build systems.

**Topics discussed**:

* Improving developer workflows
* Compiling with the command line and Less.js ("lessc")
* Compiling with Node.js and  Grunt.js
* Compiling LESS in the browser
* Watch mode, "env" and "Live refresh"
* Why the core team recommends against compiling in the browser.



###  Chapter 2: Get Your Styles Together! LESS keeps you organized.

In this chapter, I will introduce the reader to actual features of LESS, focusing on features that are useful for organizing styles and stylesheets. These same features are also responsible for attracting many developers to the language.

**Topics discussed**:

* Nesting styles makes code more readable
* Nesting too much makes code less readable
* @import Statements in LESS versus CSS
* Code comments: block and inline styles
* Strategies for converting CSS to LESS, or refactoring old code
* Design Patterns, Coding Conventions and Best Practices


### Chapter 3: Variables

In this chapter, we will use variables to construct a typography component.

Variables make it easier to maintain and control values for things like palette and typography, by keeping those values in one place. So the chapter will review how basic variables work, and then we will briefly discuss a number of different potential applications and creative uses for variables.

**Topics discussed**:

* Basic variables: Make Less.js do the math
* Escaping
* Scope
* String interpolation
* Selector interpolation
* Media queries as variables
* Variable variable names (duplicate word intentional)
* Differences from other precompilers
* Proposals for native CSS variables


### Chapter 4: Operations and Functions

In this chapter we will construct a palette component, or color scheme, using math operations and variables. Operations make variables much more powerful, and they pave the way for mixins, which will be discussed in the next chapter.  Operations are useful for calculating values "on-the-fly", so we will see in this chapter that operations can be used for generating multiple matching color variations or "modifier"values based off of a single color value. 


**Topics discussed**:

* Math Evaluation (`strictMaths`)
* Unit evaluation (`strictUnits`)
* Boolean Operations
* Color Operations
* String Functions
* Math Functions
* Miscellaneous Functions
* CSS `calc()`,  and how LESS operations differ.


### Chapter 5: Mixins

In this chapter we will construct a small mixin library.

Mixins are reusable blocks of code that can be applied throughout your stylesheets, and even modified when necessary. Thus, mixins make it easy for developers to generate complex styles that render consistently across browsers.

To help the reader understand how mixins work, and how they can be applied in the real world, the mixins we add to our library can not only be used with the other components we create in this book, but also with other projects. Additionally, each mixin will also build upon the operations and variables features discussed in previous chapters.

**Topics discussed**:

* Code reuse
* Implicit mixins
* Parametric mixins
* Nested mixins
* Compound mixins
* Mixins with return values
* Mixin-name interpolation (in anticipation of the release of this feature)
* Namespaces
* Utility Classes


### Chapter 6: Extend: Selector Inheritance

In this chapter, since we will construct a complex UI component such as a modal dialog or a dropdown- menu.

The extend feature offers ways to reduce code footprint, so the advantages of using this feature will be most prevalent and obvious when implementing styles that are complex or potentially repetitious such as gradients and transitions.

**Topics discussed**:

* Selector Inheritance versus the Cascade. When to extend, and when to mix-in.
* Extend Directives
    - :extend(all)
    - :extend(any)
* Chaining
* Extending Mixins (in anticipation of the release of this feature)
* How the LESS implementation of `:extend` differs from other pre-processors


### Chapter 7: `!merge`: Property-level Inheritance

(I'm not sure that "property-level inheritance" is an accurate description for !merge, suggestions or pull-requests are welcome.)

In this chapter we will construct a component that makes heavy use of transforms, such as a navigation slider or carousel. Some of the styles we create in this chapter will also be shuffled into the mixin library we started in [Chapter 5](#chapter-5).

`!merge` works at the property-level in a similar way to how mixins work at the selector level, except that `!merge` enables aggregating values from multiple "source" properties into single "destination" property, which is most advantageous with properties such as background and transform.

**Topics discussed**:

* How `!merge` works
* Merging box shadows
* Merging background gradients
* Merging transforms


### Chapter 8: Import Directives

To demonstrate the power of import directives, in this chapter we will create a "micro-theme" for a previous created component.

Import directives give the developer a great deal of control over how the Less.js parser processes `@import` statements. So this chapter will leverage features discussed in previous chapters to demonstrate how import directives can, for example, enable implementing multiple themes for a single UI component while only rendering the CSS for the theme or themes required.

**Topics discussed**:

* External Mixin Libraries
* Using Frameworks as "style wells"
* `@import` Directives
* `@import (once)`
* `@import (multiple)`
* `@import (less)`
* `@import (css)`
* `@import (reference)`
* Importing from inside mixins or rule sets


### Chapter 9: Pattern Matching and Guard Expressions

In this chapter, we will construct a basic CSS grid system that has a variable number of columns, so that the reader may customize it to meet his or her needs.

Pattern matching is used to change the behavior (output) of mixins, and the patterns matched against are either the arity of the mixins' arguments or the parameters passed to the mixins. Guard expressions are a basic form of "if statement" used for matching against expressions. Guard expressions and pattern matching together are often leveraged to create dynamic grid systems or to enable complex, end-user- generated themes.

**Topics discussed**:

* Arity: how to make mixins even more dynamic
* The "when" keyword
* Looping with guard statements
* Structural CSS, layouts, containers and "clearfix"
* Grid rows
* Grid columns


### Chapter 10: Undocumented Features and Hacks

Features or hacks that don't fit into other chapters will be added to this chapter throughout the course of writing the book. Such as:

* Undocumented features of LESS
* Language quarks
* Escaping
* Browser Hacks


### Appendices

* Frameworks and Tools that use LESS
* Syntax Highlighting
* Other implementations (language translations)
* A few sentences on how the parser works
* A few sentences on how the compiler works

