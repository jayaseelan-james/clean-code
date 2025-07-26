# Clean Code: A Handbook of Agile Software Craftsmanship

- [Clean Code: A Handbook of Agile Software Craftsmanship](#clean-code-a-handbook-of-agile-software-craftsmanship)
  - [Introduction](#introduction)
  - [Chapter 1: Clean Code](#chapter-1-clean-code)
    - [There Will Be Code](#there-will-be-code)
    - [Bad Code](#bad-code)
    - [The Total Cost of Owning a Mess](#the-total-cost-of-owning-a-mess)
    - [Schools of Thought](#schools-of-thought)
    - [We Are Authors](#we-are-authors)
    - [The Boy Scout Rule](#the-boy-scout-rule)
  - [Chapter 2: Meaningful Names](#chapter-2-meaningful-names)
    - [Use Intention-Revealing Names](#use-intention-revealing-names)
    - [Avoid Disinformation](#avoid-disinformation)
    - [Make Meaningful Distinctions](#make-meaningful-distinctions)
    - [Use Pronounceable Names](#use-pronounceable-names)
    - [Use Searchable Names](#use-searchable-names)
    - [Avoid Encodings](#avoid-encodings)
    - [Avoid Mental Mapping](#avoid-mental-mapping)
    - [Class Names](#class-names)
    - [Method Names](#method-names)
    - [Don't Be Cute](#dont-be-cute)
    - [Pick One Word per Concept](#pick-one-word-per-concept)
    - [Don't Pun](#dont-pun)
    - [Use Solution Domain Names](#use-solution-domain-names)
    - [Use Problem Domain Names](#use-problem-domain-names)
    - [Add Meaningful Context](#add-meaningful-context)
    - [Don't Add Gratuitous Context](#dont-add-gratuitous-context)
  - [Chapter 3: Functions](#chapter-3-functions)
    - [Small!](#small)
    - [Do One Thing](#do-one-thing)
    - [One Level of Abstraction per Function](#one-level-of-abstraction-per-function)
    - [Switch Statements](#switch-statements)
    - [Use Descriptive Names](#use-descriptive-names)
    - [Function Arguments](#function-arguments)
    - [Have No Side Effects](#have-no-side-effects)
    - [Command Query Separation](#command-query-separation)
    - [Prefer Exceptions to Returning Error Codes](#prefer-exceptions-to-returning-error-codes)
    - [Don't Repeat Yourself](#dont-repeat-yourself)
    - [Structured Programming](#structured-programming)
    - [How Do You Write Functions Like This?](#how-do-you-write-functions-like-this)
  - [Chapter 4: Comments](#chapter-4-comments)
    - [Comments Do Not Make Up for Bad Code](#comments-do-not-make-up-for-bad-code)
    - [Explain Yourself in Code](#explain-yourself-in-code)
    - [Good Comments](#good-comments)
    - [Bad Comments](#bad-comments)
  - [Chapter 5: Formatting](#chapter-5-formatting)
    - [The Purpose of Formatting](#the-purpose-of-formatting)
    - [Vertical Formatting](#vertical-formatting)
    - [Horizontal Formatting](#horizontal-formatting)
    - [Team Rules](#team-rules)
  - [Chapter 6: Objects and Data Structures](#chapter-6-objects-and-data-structures)
    - [Data Abstraction](#data-abstraction)
    - [Data/Object Anti-Symmetry](#dataobject-anti-symmetry)
    - [The Law of Demeter](#the-law-of-demeter)
    - [Data Transfer Objects](#data-transfer-objects)
  - [Chapter 7: Error Handling](#chapter-7-error-handling)
    - [Use Exceptions Rather Than Return Codes](#use-exceptions-rather-than-return-codes)
    - [Write Your Try-Catch-Finally Statement First](#write-your-try-catch-finally-statement-first)
    - [Use Unchecked Exceptions](#use-unchecked-exceptions)
    - [Provide Context with Exceptions](#provide-context-with-exceptions)
    - [Define Exception Classes in Terms of a Caller's Needs](#define-exception-classes-in-terms-of-a-callers-needs)
    - [Define the Normal Flow](#define-the-normal-flow)
    - [Don't Return Null](#dont-return-null)
    - [Don't Pass Null](#dont-pass-null)
  - [Chapter 8: Boundaries](#chapter-8-boundaries)
    - [Using Third-Party Code](#using-third-party-code)
    - [Exploring and Learning Boundaries](#exploring-and-learning-boundaries)
    - [Learning Tests Are Better Than Free](#learning-tests-are-better-than-free)
    - [Using Code That Does Not Yet Exist](#using-code-that-does-not-yet-exist)
    - [Clean Boundaries](#clean-boundaries)
  - [Chapter 9: Unit Tests](#chapter-9-unit-tests)
    - [The Three Laws of TDD](#the-three-laws-of-tdd)
    - [Keeping Tests Clean](#keeping-tests-clean)
    - [Clean Tests](#clean-tests)
    - [One Assert per Test](#one-assert-per-test)
    - [F.I.R.S.T.](#first)
  - [Chapter 10: Classes](#chapter-10-classes)
    - [Class Organization](#class-organization)
    - [Classes Should Be Small!](#classes-should-be-small)
    - [Organizing for Change](#organizing-for-change)
  - [Chapter 11: Systems](#chapter-11-systems)
    - [How Would You Build a City?](#how-would-you-build-a-city)
    - [Separate Constructing a System from Using It](#separate-constructing-a-system-from-using-it)
    - [Scaling Up](#scaling-up)
    - [Test Drive the System Architecture](#test-drive-the-system-architecture)
    - [Optimize Decision Making](#optimize-decision-making)
    - [Use Standards Wisely, When They Add Demonstrable Value](#use-standards-wisely-when-they-add-demonstrable-value)
    - [Systems Need Domain-Specific Languages](#systems-need-domain-specific-languages)
  - [Chapter 12: Emergence](#chapter-12-emergence)
    - [Getting Clean via Emergent Design](#getting-clean-via-emergent-design)
    - [Simple Design Rule 1: Runs All the Tests](#simple-design-rule-1-runs-all-the-tests)
    - [Simple Design Rules 2-4: Refactoring](#simple-design-rules-2-4-refactoring)
    - [No Duplication](#no-duplication)
    - [Expressive](#expressive)
    - [Minimal Classes and Methods](#minimal-classes-and-methods)
  - [Chapter 13: Concurrency](#chapter-13-concurrency)
    - [Why Concurrency?](#why-concurrency)
    - [Concurrency Defense Principles](#concurrency-defense-principles)
    - [Know Your Execution Models](#know-your-execution-models)
    - [Beware Dependencies Between Synchronized Methods](#beware-dependencies-between-synchronized-methods)
    - [Keep Synchronized Sections Small](#keep-synchronized-sections-small)
    - [Writing Correct Shut-Down Code Is Hard](#writing-correct-shut-down-code-is-hard)
    - [Testing Threaded Code](#testing-threaded-code)
  - [Chapter 17: Smells and Heuristics](#chapter-17-smells-and-heuristics)
    - [Comments](#comments)
    - [Environment](#environment)
    - [Functions](#functions)
    - [General](#general)
    - [Names](#names)
    - [Tests](#tests)

---

## Introduction

- There are two parts to learning craftsmanship: knowledge and work.
- Master craftsmanship by learning key concepts and deeply internalizing them through hard work and
  consistent practice.
- Knowing the theory isn't enough; like riding a bike, coding requires hands-on practice to truly
  learn and improve.
- Clean code takes hard work and practice. You must struggle, fail, and learn from your own and
  others' mistakes to truly master it.

---

## Chapter 1: Clean Code

### There Will Be Code

- You're reading this because you're a programmer who wants to improve, and the world needs more
  skilled programmers.
- Code will never disappear, as it defines the precise details machines need. Vague needs can't
  create exact results, and formal detail is required for machines to work.

### Bad Code

- Bad code slows everyone down. If you've struggled with it, ask yourself why you added to the
  problem by writing it.
- In a rush, we often leave messy code thinking we'll fix it later. But as LeBlanc's law says, later
  equals never.

### The Total Cost of Owning a Mess

- Messy code slows progress drastically. As systems grow, changes become harder, bugs multiply, and
  eventually the mess feels impossible to fix. As messy code grows, productivity drops.
- Neglecting clean code leads to failed redesigns, long delays, and endless cycles of messy systems.
  Clean code isn't optional—it's key to long-term success.
- Attitude:
  - Code degrades not just from external pressures but from our own lack of professionalism. The real
    cause of messy code often lies within the developers themselves.
  - Just as doctors must refuse unsafe procedures, programmers must defend clean code, even against
    pressure, to act professionally and protect quality.
- The Primal Conundrum: Making messy code to go faster is a false shortcut. Clean code is the only
  way to move quickly and meet deadlines without sacrificing quality.
- Knowing clean code matters is not enough. Like art, recognizing good code doesn't mean you know
  how to create it—you must learn how to write it well.
- Clean code comes from discipline and a developed “code-sense” that guides programmers to transform
  messy code into elegant, effective systems.
- What is Clean Code?
  - *Bjarne Stroustrup*: I like my code to be elegant and efficient. Code should be clear, minimal,
    reliable, and fast to stay clean and maintainable. Clean code does one thing well.
  - *Grady Booch*: Clean code is simple and direct. Clean code reads like well-written prose. Clean
    code shows intent clearly with sharp abstractions and simple control flow.
  - *Dave Thomas*: Clean code can be read, and enhanced by a developer other than its original
    author. It has unit and acceptance tests. It has meaningful names and one way to do one thing.
  - *Michael Feathers*: Clean code always looks like it was written by someone who cares. There is
    nothing obvious that you can do to make it better.
  - *Ron Jeffries*: Runs all the tests; Contains no duplication; Expresses all the design ideas that
    are in the system; Minimizes the number of entities such as classes, methods, functions, etc.
  - *Ward Cunningham*: Clean code feels right when each routine you read turns out to be pretty much
    what you expected. Beautiful code makes it feel like the language fits the problem perfectly.

### Schools of Thought

- This book shares one approach to clean code, shaped by experience. It's not absolute truth, but
  its insights are worth learning from and considering alongside other perspectives.

### We Are Authors

- Code is read more than it's written. Like authors, programmers must write clearly for readers who
  will later rely on and judge their work.
- Since we read code far more than we write it, making code easy to read is key to writing it
  efficiently and working faster overall.

### The Boy Scout Rule

- Writing good code isn't enough. To prevent decay, we must keep it clean over time.
- The Boy Scouts of America have a simple rule: *Leave the campground cleaner than you found it.*
- Small, consistent improvements prevent code rot. Making code better with every change reflects
  true professionalism and ensures continuous progress.

---

## Chapter 2: Meaningful Names

- Names are everywhere in software. We name our variables, our functions, our arguments, classes,
  packages, source files and directories. We name everything, so we should do it well and with care.

### Use Intention-Revealing Names

- Good names reveal intent and save time. They should explain what something is, does, and how it's
  used. If a comment is needed, the name isn't clear enough.

### Avoid Disinformation

- Avoid misleading names that confuse or contradict known meanings. Choose names that clearly
  reflect what the code represents or does.
- Avoid names that differ only slightly, as they cause confusion. Use similar names only when they
  represent closely related concepts.
- Avoid using lower-case L or uppercase O as variable names since they look like 1 and 0. Clear
  naming prevents confusion and avoids relying on fonts or extra instructions.

### Make Meaningful Distinctions

- Don't alter names just to satisfy the compiler. If names must differ, they should reflect
  meaningful differences, not arbitrary changes or errors.
- Avoid number-series names like a1, a2 as they lack meaning and give no insight into the author's
  intent.
- Avoid noise words like *Info*, *Data*, or *Object* in names, as they add no real meaning. Use
  naming that clearly distinguishes purpose without redundancy.

### Use Pronounceable Names

- Use pronounceable names, so code can be easily discussed. Clear naming supports communication,
  which is vital in collaborative programming.
- If you can't pronounce it, you can't discuss it without sounding like an idiot.
  
### Use Searchable Names

- Single-letter names and numeric constants have a particular problem in that they are not easy to
  locate across a body of text.
- Use meaningful, searchable names instead of raw values or short names to avoid confusion and make
  code easier to find, read, and maintain.
- Use single-letter names only as local variables in short methods. Wider-scope variables need
  longer, search-friendly names to ensure clarity and maintainability.

### Avoid Encodings

- Avoid encoding type or scope in names. It adds needless complexity, is hard to read, and creates
  extra work for new developers.
- Old languages forced encoded names (like Hungarian notation) due to limits and weak typing. Modern
  languages support clear, type-safe code, making such encodings unnecessary today.
- Prefixes like **m_** for member variables are no longer needed. Modern tools and clean, small code
  make such markers unnecessary and eventually just visual clutter.
- Avoid prefixing interfaces with letters like **I**. Name interfaces clearly and, if needed, encode
  only the implementation to reduce distraction and reveal intent.

### Avoid Mental Mapping

- Avoid vague names that force readers to mentally map them to real concepts. Use clear, meaningful
  terms from the problem or solution domain.
- Professional programmers prioritize clarity, writing code that others can easily understand and
  maintain.

### Class Names

- Class and object names should be nouns or noun phrases, not verbs, like *Customer* or *Account*.
  Avoid vague terms like *Manager*, *Processor*, *Data* or *Info* in the name for clarity.

### Method Names

- Methods should have verbs or verb phrase names like *PostPayment*, *DeletePage* or *Save*.
  Accessors, mutators, and predicates may use *Get*, *Set*, and *Is* as prefix for clarity.

### Don't Be Cute

- Avoid clever or joke-based names. Choose clear, descriptive names that all readers can understand,
  regardless of humor or cultural context.
- Say what you mean. Mean what you say.

### Pick One Word per Concept

- Use consistent terms for the same concept to avoid confusion and save time. Mixing synonyms like
  *fetch*, *retrieve*, and *get* can make code harder to understand and maintain.
- Function names must be clear and consistent, since modern tools often show little context. Good
  method names help you choose the right one quickly without extra digging.
- A consistent lexicon is a great boon to the programmers who must use your code.

### Don't Pun

- Do not use the same word for different meanings. Reusing terms for separate ideas causes
  confusion. One word per concept keeps naming clear and consistent.
- Avoid reusing names like *add* with different meanings. Use precise names to prevent confusion and
  make code easier to read and understand.

### Use Solution Domain Names

- Use technical terms and computer science concepts in code, as programmers understand them better
  than vague domain terms. Familiar names aid faster comprehension.

### Use Problem Domain Names

- When no technical term fits, use problem domain names. Match naming to context, using domain terms
  for domain logic and technical terms for technical logic.

### Add Meaningful Context

- Most names need context for clarity. Use well-named classes or functions to provide it, and only
  use prefixes when absolutely necessary. For instance, variables named *firstName*, *lastName*,
  *city*, *state*, etc. could be grouped into a class to represent a concept like an *Address*.

### Don't Add Gratuitous Context

- Avoid prefixing class names with the application name. It clutters code, hinders autocomplete, and
  makes reuse harder with long, redundant names.
- Prefer short, clear names with just enough context.

---

## Chapter 3: Functions

### Small!

- The first rule of functions is that they should be small. The second rule of functions is that
  they should be smaller than that.
- In the past, functions were limited to a screen-full, but even today, they should rarely exceed 20
  lines despite larger modern displays.
- Control blocks should be one line, ideally a function call, keeping functions small, readable, and
  shallow in nesting for clarity and documentation.

### Do One Thing

- Functions should do one thing. They should do it well. They should do it only.
- The idea that functions should do one thing is hard to apply, as it's unclear whether a function
  like *RenderPageWithSetupsAndTeardowns* is doing one task or several at different abstraction
  levels.
- A function does one thing if its steps are just one level below its name; mixing abstraction
  levels means it's doing more than one thing.
- If you can extract a function with a meaningful name that's not just a restatement of the code,
  the original function is doing more than one thing.

### One Level of Abstraction per Function

- To ensure a function does one thing, all statements should be at the same abstraction level;
  mixing levels causes confusion and invites clutter over time.
- Reading Code from Top to Bottom: The Stepdown Rule
  - Code should read like a top-down narrative, with each function followed by others at the next
    abstraction level. This is called the Stepdown Rule.
  - Though hard to master, keeping functions at a single abstraction level is vital to keeping them
    short and focused on doing one thing.

### Switch Statements

- Switch statements are hard to keep small or focused, so they should be isolated in low-level
  classes and replaced with polymorphism when possible.

``` csharp Payroll.cs
public Money CalculatePay(Employee e)
{
    return e.Type switch
    {
        EmployeeType.Commissioned => CalculateCommissionedPay(e),
        EmployeeType.Hourly => CalculateHourlyPay(e),
        EmployeeType.Salaried => CalculateSalariedPay(e),
        _ => throw new InvalidEmployeeTypeException(e.Type)
    };
}
```

- This function is large, violates Single Responsibility Principle (SRP) and Open Closed Principle
  (OCP), grows with new types, and sets a pattern for many similar functions to repeat the same
  flawed structure.
- Use a hidden switch in an abstract factory to create polymorphic *Employee* objects, allowing
  functions like *CalculatePay* to dispatch via inheritance, not conditionals.

### Use Descriptive Names

- Good names are key to clean code. Small, focused functions make naming easier. Long, clear names
  are better than short ones or comments, so use readable, descriptive names.
- Take time to try different names using IDEs. Descriptive, consistent names improve clarity, guide
  design, and often lead to better code structure.

### Function Arguments

- The best functions have no arguments (niladic). One (monadic) or two (dyadic) are acceptable,
  three (triadic) should be avoided, and more than three need strong justification but are still
  discouraged.
- Arguments add cognitive load. Removing them, like making shared data an instance variable instead
  of an argument, simplifies code and eases reader understanding.
- Testing grows harder with more arguments. No arguments are easiest, one is manageable, two is
  harder, and more than two makes testing combinations complex.
- Output arguments are confusing because we expect data to go in via arguments and out via return
  values, making output via arguments harder to understand.
- Common Monadic Forms:
  - Single-argument functions usually ask a question or transform the input. Use clear, consistent
    names to reflect the function's purpose and meet reader expectations.
  - Single-argument functions can also represent events that change system state. Use them carefully
    with clear names and context to show they are event-driven.
- Flag Arguments: Flag arguments are bad practice. They signal the function does more than one
  thing, making the code harder to read and the method signature more complex.
- Dyadic Functions:
  - Two-argument functions are harder to read unless the arguments form a natural pair, like
    coordinates. Unrelated arguments add complexity and risk being overlooked.
  - Even common dyads like assertEquals(expected, actual) can confuse due to lack of natural order.
    When possible, refactor dyads into monads to improve clarity and reduce errors.
- Triads: Triads are much harder to understand than dyads due to confusion with argument order and
  meaning. Use them only when truly necessary and with extra care.
- Argument Objects: If a function needs many arguments, group related ones into a class. This
  reduces complexity and often reveals meaningful concepts, like using Point instead of *x* and *y*.
- Argument Lists: Variable argument functions follow the same rules as fixed ones. If *args* are
  treated the same, it's like passing a list, so keep total arguments within monad to triad limits.
- Verbs and Keywords: Good function names explain intent and argument order. Use verb/noun pairs or
  keyword-style names like *assertExpectedEqualsActual* to reduce confusion and improve readability.

### Have No Side Effects

- Side effects break a function's promise by causing hidden changes to variables or globals, leading
  to bugs, order dependencies, and hard-to-find issues in code behavior.
- Output Arguments: Arguments should clearly be inputs. Output arguments cause confusion and force
  readers to check signatures. In OO languages, use object methods instead to avoid this.

### Command Query Separation

- A function should either perform an action or return information, not both. Mixing these roles
  causes confusion and makes code harder to understand.

### Prefer Exceptions to Returning Error Codes

- Returning error codes from commands breaks command-query separation and forces immediate error
  handling, leading to nested code and reduced clarity.
- Try/catch blocks clutter code by mixing error and normal logic. Extract them into separate
  functions, so each handles one task, with try as the first word and nothing after catch.

### Don't Repeat Yourself

- Code duplication hides easily, adds bloat, and increases the chance of errors. Removing it
  improves clarity and reflects a core goal of many programming paradigms and practices.

### Structured Programming

- Single-entry, single-exit rules help in large functions, but with small functions, multiple
  returns, breaks, or continues can improve clarity. *Goto* should still be avoided.

### How Do You Write Functions Like This?

- Writing code is like writing prose: the first draft is messy, but through refactoring, renaming,
  and testing, it becomes clean and well-structured. It's an iterative process.

---

## Chapter 4: Comments

- Comments can help but often harm when outdated or excessive; they're a necessary evil, not pure
  good, ideally replaced by clear, expressive code.
- Comments reflect our failure to express intent in code; use them only when necessary, and always
  prefer clear code over commentary.
- They often become inaccurate over time as code evolves, leading to misinformation, since
  they're hard to maintain and easy to overlook.
- Clear, expressive code is better than comments; inaccurate comments mislead, while only code holds
  the true, reliable source of information.

### Comments Do Not Make Up for Bad Code

- Don't use comments to excuse messy code. Clean and clarify the code instead, as clear code with
  few comments is far better than confusing code with many.

### Explain Yourself in Code

- Code can often explain intent clearly; instead of commenting, write functions that express what
  you mean—it usually takes just a bit of thought.

### Good Comments

- Legal Comments: Legal comments like copyrights are fine, but keep them brief. Refer to external
  documents instead of embedding full legal terms in the code.
- Informative Comments: Use function or class names to convey meaning instead of comments. When
  comments are needed, clear structure or naming may make them unnecessary.
- Explanation of Intent: Comments that explain intent behind decisions, like custom sorting or
  stress testing with threads, add value—even if the implementation is debatable.
- Clarification: Clarifying comments can help explain obscure values, especially in standard or
  unchangeable code, but clarity should be built into the code when possible.
- Warning of Consequences: Warning comments are useful when explaining risks or non-obvious
  behavior, especially in legacy code or when preventing common but unsafe optimizations.
- TODO Comments: TODO comments are useful reminders for future fixes or changes, but they must not
  justify bad code and should be reviewed and cleaned up regularly.
- Amplification: A comment may be used to amplify the importance of something that may otherwise
  seem inconsequential.

### Bad Comments

- Mumbling: Don't write vague or rushed comments just to meet a process. A comment must clearly
  explain intent; unclear ones only confuse and force others to dig through code.
- Redundant Comments: Redundant comments that restate obvious code waste time, obscure clarity, and
  offer no real value. Clear code needs no empty reassurances or filler documentation.
- Misleading Comments: Vague or imprecise comments can mislead and waste time. When comments subtly
  misstate behavior, they create false expectations and debugging headaches.
- Mandated Comments: Mandatory comments for every function or variable add clutter, invite
  confusion, and often mislead more than they help.
- Journal Comments: Change logs in code files are obsolete clutter now that version control systems
  track edits. These outdated journals should be removed to keep code clean.
- Noise Comments: Noisy comments that restate the obvious or vent frustration add no value and
  become ignored. Channel that energy into cleaner code instead of cluttering it.
- Scary Noise: Redundant comments like these add no value and often include careless errors. If a
  comment just repeats the code, it's noise and should be removed.
- Don't Use a Comment When You Can Use a Function or a Variable.
- Position Markers: Banner comments can help group code but often become clutter. Use them rarely
  and only when they add real clarity, or they'll just blend into the noise.
- Closing Brace Comments: Marking closing braces adds clutter in small, clean functions. If you feel
  the need for them, it's a sign your function might be too long and needs refactoring.
- Attributions and Bylines: Author tags like `/* Added by Jayaseelan */` become outdated and clutter
  code. Use version control systems to track authorship instead of embedding it in comments.
- Commented-Out Code: It creates confusion and clutter. With version control systems in place,
  there's no excuse not to delete unused code instead of leaving it behind.
- HTML Comments: HTML in comments clutters code and reduces readability in editors. Let
  documentation tools handle formatting instead of embedding HTML manually.
- Nonlocal Information: Comments should describe nearby code only. Including unrelated system
  details creates confusion and risks becoming outdated or misleading.
- Too Much Information: Avoid stuffing comments with irrelevant history or excessive detail. Focus
  on what helps the reader understand the code, not on unnecessary background.
- Inobvious Comments: A comment should clearly relate to the code it describes. If it's vague or
  confusing, it fails its purpose and may need as much explanation as the code itself.
- Function Headers: Short functions don't need much description. A well-chosen name for a small
  function that does one thing is usually better than a comment header.

---

## Chapter 5: Formatting

- Clean, consistent code signals professionalism. Use simple formatting rules, apply them strictly,
  and automate them if possible to maintain quality and trust.

### The Purpose of Formatting

- Code formatting is vital for communication. Readability impacts future changes more than current
  functionality. Style and discipline outlive the original code.

### Vertical Formatting

- Smaller source files, ideally under 200–500 lines, are easier to understand and maintain. Large
  systems can be built effectively using many small, focused files.
- The Newspaper Metaphor:
  - A source file should read like a newspaper: start with a clear name and overview, then reveal
    more detail gradually, ending with the lowest-level functions and specifics.
  - Like newspapers with short, focused articles, code should be split into small, organized parts.
    Long, disorganized files discourage reading and understanding.
- Vertical Openness Between Concepts: Use blank lines to separate concepts in code. They create
  visual cues, improve layout, and make scanning easier by highlighting distinct concepts.
- Vertical Density: Vertically dense code signals related logic. Keeping tightly related lines close
  improves readability and reduces eye movement for faster understanding.
- Vertical Distance:
  - Keep closely related code concepts near each other to avoid confusion and reduce scrolling.
    Vertical proximity improves understanding and eases code navigation.
  - Declare variables close to where they're used. In short functions, place them at the top; for
    loops, declare control variables in the loop when possible.
  - Instance variables should be declared at the top of the class, in a consistent, visible
    place, since they're often used by many methods and need to be easy to find.
  - Place dependent functions close together with the caller above the callee to enhance flow and
    readability. Constants should be declared at meaningful, visible levels.
  - Code elements with strong conceptual affinity should be placed close together, even if not
    directly dependent, to reflect their related purpose and improve clarity.
- Vertical Ordering: Function calls should flow downward, with high-level logic at the top and
  details below. This mirrors a newspaper format, letting readers grasp key ideas before diving into
  details.

### Horizontal Formatting

- Keep lines short for readability. Aim for under 100–120 characters, as most code naturally fits
  within that. Excessively long lines reduce clarity and signal carelessness.
- Horizontal Openness and Density: Use horizontal white space to clarify relationships in code.
  Space separates weakly related elements, while tightly related ones stay close for better
  readability and meaning.
- Horizontal Alignment: Avoid horizontal alignment in declarations or assignments. Long aligned
  lists reveal a deeper issue—the code is too long, not that it's misaligned.
- Indentation:
  - Indentation reflects the code's hierarchical structure and scopes, making it easier to read,
    scan, and understand. Without it, source files become hard to navigate and comprehend.
  - Avoid breaking indentation rules, even for short code blocks. Skipping proper indentation
    usually reduces clarity and often leads to reverting the change later.
- Dummy Scopes: Avoid dummy loop bodies, but if unavoidable, use proper indentation and braces to
  make lone semicolons visible and prevent logic errors.

### Team Rules

- A team should follow one agreed formatting style to ensure consistency. Unified code style
  improves readability and prevents confusion across the codebase.

---

## Chapter 6: Objects and Data Structures

### Data Abstraction

- Abstraction hides implementation by exposing essential behavior, not just adding getters and
  setters. Thoughtful design matters more than blindly exposing data.

### Data/Object Anti-Symmetry

- Objects hide data and expose behavior, while data structures expose data with little behavior.
  Their opposite nature has deep design implications.
- This exposes the fundamental dichotomy between objects and data structures:

  ``` md
  Procedural code (code using data structures) makes it easy to add new functions without changing
  the existing data structures. OO code, on the other hand, makes it easy to add new classes without
  changing existing functions.
  ```

- OO suits adding new types, procedures suit adding new functions. Mature developers know not
  everything should be an object—sometimes simple data and procedures work best.

### The Law of Demeter

- The Law of Demeter advises that modules should not know internal details of other objects. Using
  accessors can break encapsulation by revealing internal structure.
- The Law of Demeter says that a method *f* of a class *C* should only call the methods of these:
  - *C*
  - An object created by *f*
  - An object passed as an argument to *f*
  - An object held in an instance variable of *C*
- The method should not invoke methods on objects that are returned by any of the allowed functions.
  In other words, talk to friends, not to strangers.
- Train Wrecks:
  - Call chains reveal too much object structure and should be avoided. They violate the Law of
    Demeter by making one function aware of many internal object layers.
  - Objects should hide structure, but data structures may expose it. Accessors often blur this
    line.
- Hybrids: Hybrid structures mix object behavior with exposed data, making code harder to extend.
  They reflect unclear design and should be avoided for clean architecture.
- Hiding Structure: Mixing low-level details in code is messy. Instead, let the object handle the
  task to hide internals and avoid violating the Law of Demeter by exposing object structure.

### Data Transfer Objects

- A DTO is a class with public variables and no functions, ideal for transferring raw data between
  systems like databases or sockets before converting to full objects.
- Active Records are DTOs with methods like *save* or *find*. Adding business logic to them creates
  messy hybrids. Keep logic in separate objects to preserve clean design.

---

## Chapter 7: Error Handling

- Error handling is vital, but if it clutters the code and hides core logic, it violates the
  principles of clean code.

### Use Exceptions Rather Than Return Codes

- Older languages lacked exceptions, forcing error flags or codes that cluttered and confused logic.
  Throwing exceptions keeps calling code cleaner and more readable.
- Separating error handling from logic improves code by isolating concerns, making each easier to
  understand on its own.

### Write Your Try-Catch-Finally Statement First

- Try blocks define a scope where execution may abort, and catch must restore consistency. Begin
  with try-catch-finally to ensure clear, reliable behavior.
- Write tests that trigger exceptions first, then build handlers to pass them. This helps define and
  preserve the transactional scope of the try block.

### Use Unchecked Exceptions

- Checked exceptions seemed useful but break encapsulation by forcing wide code changes. Many robust
  languages work fine without them, raising doubts about their true value.

### Provide Context with Exceptions

- Exceptions should include clear messages about what failed and why, since stack traces lack
  intent. Provide context to help identify the error's source and support useful logging.

### Define Exception Classes in Terms of a Caller's Needs

- Errors can be classified by source or type, but when defining exceptions, focus on how they will
  be caught in the application.
- Wrap third-party APIs to reduce dependency, ease testing, and allow future changes. Use one
  exception class unless distinct handling is needed for different errors.

### Define the Normal Flow

- Separating error handling from logic creates cleaner code, but pushing detection to the edges may
  not fit all cases, especially when you don't want to abort execution.

### Don't Return Null

- Returning null invites errors and burdens callers. Instead, throw exceptions or return special
  case objects to avoid fragile null checks and improve reliability.

### Don't Pass Null

- Passing null into methods is worse than returning it. Avoid it unless required, and treat null
  arguments as errors to reduce mistakes and improve code safety.

---

## Chapter 8: Boundaries

### Using Third-Party Code

- Interface providers aim for broad use, while users seek tailored solutions. This mismatch often
  leads to issues at system boundaries.
- Exposing broad third-party interfaces in code can lead to misuse and fragile code. Encapsulating
  them preserves intent, enforces rules, and improves clarity and maintainability.

### Exploring and Learning Boundaries

- Using third-party code saves time, but unclear usage can cause bugs. Writing tests helps clarify
  behavior and isolate issues.
- Learning and integrating third-party code together is tough. Writing learning tests helps verify
  our understanding before using it in production.

### Learning Tests Are Better Than Free

- Learning tests clarify APIs at no extra cost and offer long-term value by detecting changes in
  future releases.
- These tests ensure third-party code behaves as expected and catch breaking changes early,
  supporting clean boundaries and safer upgrades.

### Using Code That Does Not Yet Exist

- When facing unknown or undefined boundaries, define your own interface to keep code clean,
  adaptable, and testable as understanding or APIs evolve.
- Defining our own interface creates a testable seam, enabling unit tests with fakes and boundary
  tests once the real API is available.

### Clean Boundaries

- Boundaries must be clear and well-tested to handle change. Limit reliance on third-party code by
  wrapping or adapting it to protect flexibility and control.

---

## Chapter 9: Unit Tests

### The Three Laws of TDD

1. You may *not* write production code until you have written a failing unit test.
2. You may *not* write more of a unit test than is sufficient to fail, and not compiling is failing.
3. You may *not* write more production code than is sufficient to pass the currently failing test.

- Writing tests alongside code in short cycles ensures full coverage but can lead to a large,
  hard-to-manage test suite. Thus, have them clean to ease maintenance.

### Keeping Tests Clean

- Neglecting test code quality leads to fragile tests that are hard to maintain and can become a
  bigger burden than having no tests at all.
- Messy tests lead to costly maintenance, failed test efforts, and decaying code. Clean,
  well-designed test code is essential to long-term software health.
- Test code is just as important as production code.
- Tests Enable the -ilities:
  - Clean unit tests remove fear of change and make code flexible, maintainable, and safe to
    improve—even with poor design.
  - Tests enable all the -ilities, because tests enable change. Whereas, dirty tests block
    improvement, leading to decaying code and eventual test loss.

### Clean Tests

- Clean tests prioritize readability through clarity, simplicity, and structure, making them easy to
  understand and maintain.
- Domain—Specific Testing Language: A test-specific API improves readability and evolves through
  refactoring, creating a clear, expressive language for writing and understanding tests.
- A Dual Standard: Test code can trade efficiency for clarity, but must remain clean, simple, and
  expressive, despite differing standards from production code.

### One Assert per Test

- Limiting asserts in a test improves clarity. While one assert per test is ideal, using a few is
  fine if they remain clear and concise. Minimize asserts to keep tests readable.
- Single Concept per Test: Each test should focus on one concept with minimal asserts to keep intent
  clear and avoid confusing, bloated test functions.

### F.I.R.S.T.

- Fast: Tests must be fast. Slow tests discourage frequent runs, delay bug detection, and reduce
  code cleanup, leading to code rot.
- Independent: Tests should not depend on each other. Tests must be independent. When one test
  depends on another, failures cascade, hiding real issues and making debugging harder.
- Repeatable: Tests should be repeatable in any environment. Non-repeatable tests cause unreliable
  results and limit when and where you can test.
- Self-Validating: The tests should have a boolean output. Tests must be self-validating with clear
  pass or fail results. Manual checks make failures subjective and slow down development.
- Timely: The tests need to be written in a timely fashion. Write unit tests before production code
  to ensure testability and better design. Writing them after can make testing harder or neglected.

---

## Chapter 10: Classes

### Class Organization

- Start classes with constants, then private variables. Public functions follow, with related
  private helpers below, making code read top-down like an article.
- Encapsulation: Prefer private variables and functions, but allow internal or protected access for
  tests when needed. Privacy matters, but tests take priority when no better option exists.

### Classes Should Be Small!

- Classes should be small, even smaller than you think. Unlike functions measured by lines, class
  size is judged by how many responsibilities it handles.
- A class name should clearly reflect its responsibilities. If it's vague or hard to name, the class
  likely does too much and needs to be split.
- We should also be able to write a brief description of the class in about 25 words, without using
  the words "if," "and," "or," or "but."
- The Single Responsibility Principle:
  - A class should have only one responsibility and one reason to change, guiding both its purpose
    and size.
  - SRP is simple but often ignored. We focus on making code work, not keeping it clean. Once it
    works, we forget to refactor large classes into focused, single-purpose ones.
  - Small, focused classes make systems easier to navigate. They reduce clutter, clarify purpose, and
    help manage complexity better than a few large, overloaded ones.
- Cohesion:
  - A class should have few instance variables, with methods that use them closely. High cohesion
    means methods and data work together as a unified, logical whole.
  - Too many instance variables used by only some methods often signals a hidden class. Split them
    into smaller, more cohesive classes with clear responsibilities.
- Maintaining Cohesion Results in Many Small Classes: Breaking big functions into smaller ones may
  reveal new classes. If methods share only some variables, split them into cohesive classes for
  clearer, better-organized code.

### Organizing for Change

- Clean systems reduce change risk by isolating impact. New features should extend classes, not
  modify them, keeping existing code stable and easier to maintain.
- Isolating from Change: Code changes with needs, so depend on abstractions, not concrete details.
  This reduces coupling, eases testing, and aligns with the Dependency Inversion Principle (DIP).

---

## Chapter 11: Systems

### How Would You Build a City?

- Cities function through teamwork and modularity, and clean code aims to bring similar structure
  and clarity to software, especially at the system level.

### Separate Constructing a System from Using It

- Building software is different from using it. Clean systems separate startup setup from runtime
  logic, following the key principle of separating concerns.
- Mixing setup code with runtime logic breaks modularity and SRP, making testing harder.
- Separation of Main: Separating construction in main keeps dependencies one-way. The app just uses
  objects, unaware of how they were built. This simplifies control flow and design.
- Factories: Use Abstract Factory to let the app control object creation timing while hiding
  construction details, keeping dependencies flowing from main to the app.
- Dependency Injection: DI separates construction from use by letting external containers provide
  dependencies, supporting SRP and flexible, passive object creation.

### Scaling Up

- Systems should grow iteratively like cities, adapting over time. Clean code and refactoring
  support this at the code level, challenging the myth of perfect first-time design.
- Software systems are unique compared to physical systems. Their architectures can grow
  incrementally, if we maintain the proper separation of concerns.

### Test Drive the System Architecture

- Decoupling domain logic from architecture enables flexible, test-driven design and avoids the
  rigidity and risk of Big Design Up Front.
- High-performing systems use simple, loosely coupled designs that stay flexible while keeping clear
  goals and adapting to change as needed.

### Optimize Decision Making

- Modularity enables decentralized decisions, essential for managing large systems like cities or
  complex software.
- Delaying decisions allows better choices with more insight, avoiding the risks of premature,
  poorly informed commitments.

### Use Standards Wisely, When They Add Demonstrable Value

- Construction thrives on evolved standards, but in software, overreliance on hyped standards can
  shift focus away from real customer value.

### Systems Need Domain-Specific Languages

- DSLs let developers write code in domain-specific terms, improving clarity and aligning closely
  with expert knowledge.
- Effective DSLs close the gap between domain concepts and code, raising abstraction and making
  intent clearer, like agile does for team communication.

---

## Chapter 12: Emergence

### Getting Clean via Emergent Design

- Kent Beck's four rules of Simple Design are of significant help in creating well-designed
  software. According to Kent, a design is "simple" if it follows these rules:
  - Run all the tests
  - Contains no duplication
  - Expresses the intent of the programmer
  - Minimizes the number of classes and methods
- The rules given are in the order of importance.

### Simple Design Rule 1: Runs All the Tests

- A system must be verifiable through testing. Testable systems lead to simpler, single-purpose
  designs, making verification easier and design quality better.
- Writing more tests encourages low coupling and high cohesion by using principles like DIP,
  abstraction, and dependency injection, which improves overall design.

### Simple Design Rules 2-4: Refactoring

- Tests give us the safety to refactor often, keeping code clean. With each change, we check design
  quality and rely on tests to ensure nothing breaks.
- Refactoring lets us apply good design principles like cohesion and separation of concerns, while
  removing duplication and improving clarity with fewer classes and methods.

### No Duplication

- Duplication adds risk, effort, and complexity. It appears in repeated or similar code and
  implementations, all of which should be refactored to improve design.
- Extracting small common code may reveal SRP violations and encourages reuse. Small-scale reuse
  reduces complexity and is key to broader, system-wide reuse.

### Expressive

- Clear code reduces maintenance cost and defects. Use good names, small functions, and clear
  structure to help others understand the system easily.
- Using standard names and patterns improves code clarity. Expressive tests also serve as readable
  documentation to help others quickly grasp class behavior.
- The most important way to be expressive is to *try*. Refine names, simplify functions, and write
  with future readers in mind—often, that reader will be you.

### Minimal Classes and Methods

- Avoid overdoing principles like SRP or duplication removal. Too many tiny classes or rigid rules
  can harm clarity. Favor practical, balanced design over strict dogma.
- Keep the system, classes, and functions small, but prioritize testing, removing duplication, and
  clarity over reducing class or function count.

---

## Chapter 13: Concurrency

- Writing clean concurrent code is very hard. It's easier to write single-threaded or flawed
  multithreaded code that only fails under system stress.

### Why Concurrency?

- Concurrency separates what gets done from when it gets done, boosting throughput and clarity by
  structuring apps as small collaborating units instead of one tightly coupled main loop.
- Myths and Misconceptions:
  - Concurrency always improves performance: Concurrency can improve performance, but only when
    significant wait time exists and can be shared across threads or processors.
  - Design does not change when writing concurrent programs: Concurrent program design often differs
    greatly from single-threaded design, as decoupling what from when significantly impacts system
    structure.
  - Understanding concurrency issues is not important when working with a container.
- Here are a few more balanced sound bites regarding writing concurrent software:
  - Concurrency incurs some overhead, both in performance as well as writing additional code.
  - Correct concurrency is complex, even for simple problems.
  - Concurrency bugs aren't usually repeatable, so they are often ignored as one-offs instead of the
    true defects they are.
  - It often requires a fundamental change in design strategy.

### Concurrency Defense Principles

- Single Responsibility Principle (SRP):
  - Concurrency is a valid reason for change and should be separated to follow SRP, yet it's often
    wrongly mixed into core production code.
  - Concurrency code has a unique life cycle, tougher challenges than regular code, and many failure
    modes, so it should be kept separate from core application logic.
  - *Recommendation*: Keep your concurrency-related code separate from other code.
- Corollary: Limit the Scope of Data
  - To avoid thread interference on shared data, use synchronized blocks, but keep critical sections
    minimal to reduce complexity and risk.
  - The more locations shared data is updated, the higher the risk of unguarded access, duplication,
    and hard-to-trace failures.
  - *Recommendation*: Take data encapsulation to heart; severely limit the access of any data that
    may be shared.
- Corollary: Use Copies of Data
  - Avoiding shared data by using read-only copies or merging results later reduces issues and may
    outperform synchronization despite extra object creation.
- Corollary: Threads Should Be as Independent as Possible
  - Design threads to work independently with unshared data and local variables, avoiding
  synchronization and simplifying behavior.
  - *Recommendation*: Attempt to partition data into independent subsets than can be operated on by
    independent threads, possibly in different processors.

### Know Your Execution Models

- Understanding how to partition behavior in concurrent apps requires learning some definitions:
  - Bound Resources: Resources of a fixed size or number used in a concurrent environment. Examples
    include database connections and fixed-size read/write buffers.
  - Mutual Exclusion: Only one thread can access shared data or a shared resource at a time.
  - Starvation: One thread or a group of threads is prohibited from proceeding for an excessively
    long time or forever. For example, always letting fast-running threads through first could
    starve out longer running threads if there is no end to the fast-running threads.
  - Deadlock: Two or more threads waiting for each other to finish. Each thread has a resource that
    the other thread requires and neither can finish until it gets the other resource.
  - Livelock: Threads in lockstep, each trying to do work but finding another "in the way." Due to
    resonance, threads continue trying to make progress but are unable to for an excessively long
    time—or forever.

- Producer-Consumer: Producer threads add work to a bounded queue, and consumer threads take it.
  Both signal and wait as needed, coordinating access based on queue state.
- Readers-Writers: Balancing reader and writer access to shared data is hard; favoring one risks
  starvation or poor throughput. Coordination must avoid stale reads and long blocks.
- Dining Philosophers: This problem mirrors threads competing for resources, often leading to
  deadlock, livelock, or performance issues if not carefully designed.
- *Recommendation*: Learn these basic algorithms and understand their solutions.

### Beware Dependencies Between Synchronized Methods

- Dependencies between synchronized methods cause subtle bugs in concurrent code.
- *Recommendation*: Avoid using more than one method on a shared object.
- When using multiple methods on a shared object, correctness can be ensured in three ways:
  - Client-Based Locking—Have the client lock the server before calling the first method and make
    sure the lock's extent includes code calling the last method.
  - Server-Based Locking—Within the server create a method that locks the server, calls all the
    methods, and then unlocks. Have the client call the new method.
  - Adapted Server—create an intermediary that performs the locking. This is an example of
    server-based locking, where the original server cannot be changed.

### Keep Synchronized Sections Small

- Synchronized blocks ensure one thread at a time but add overhead, so keep critical sections
  minimal to avoid contention and performance loss.
- *Recommendation*: Keep your synchronized sections as small as possible.

### Writing Correct Shut-Down Code Is Hard

- Graceful shutdown in concurrent systems is tricky; deadlocks or blocked threads can prevent
  shutdown, so handling it correctly requires careful design and testing.
- *Recommendation*: Think about shut-down early and get it working early. It's going to take longer
  than you expect. Review existing algorithms because this is probably harder than you think.

### Testing Threaded Code

- *Recommendation*: Write tests that have the potential to expose problems and then run them
  frequently, with different programmatic configurations and system configurations and load. If
  tests ever fail, track down the failure. Don't ignore a failure just because the tests pass on a
  subsequent run.
- A few more fine-grained recommendations:
  - Treat spurious failures as candidate threading issues: Do not ignore system failures as one-offs.
  - Get your nonthreaded code working first: Do not try to chase down nonthreading bugs and
    threading bugs at the same time. Make sure your code works outside of threads.
  - Make your threaded code pluggable: Make your thread-based code especially pluggable so that you
    can run it in various configurations.
  - Make your threaded code tunable: Tuning thread count needs trial and error. Make it easy to
    adjust, monitor performance, and possibly enable dynamic or self-tuning based on system load.
  - Run with more threads than processors: Running more threads than cores triggers frequent task
    switching, increasing the chance of exposing missing critical sections or deadlocks.
  - Run on different platforms: Run your threaded code on all target platforms early and often.
  - Instrument your code to try and force failures: Use methods that can affect the order of
    execution, thereby increasing the odds of detecting a flaw. Use jiggling strategies to ferret
    out errors.

---

## Chapter 17: Smells and Heuristics

### Comments

- *C1: Inappropriate Information*
  - Use comments only for technical notes on code and design. Comments shouldn't store metadata like
    change history or authorship; that belongs in version control.
- *C2: Obsolete Comment*
  - Obsolete comments are misleading and irrelevant. Avoid writing them, and remove or update
    outdated ones promptly to keep code clear and accurate.
- *C3: Redundant Comment*
  - A comment is redundant if it describes something that adequately describes itself. Comments
    should say things that the code cannot say for itself.
- *C4: Poorly Written Comment*
  - Write comments with care and clarity. Use proper grammar, be concise, and avoid stating the
    obvious or rambling. Quality comments reflect thoughtful writing.
- *C5: Commented-Out Code*
  - Commented-out code is outdated, distracting, and useless. Delete it without fear—version control
    keeps history if it's ever needed.

### Environment

- *E1: Build Requires More Than One Step*
  - Building a project should be simple: one command to check it out, another to build it. Avoid
    complex steps, scattered files, or dependencies.
- *E2: Tests Require More Than One Step*
  - Running all unit tests should be quick and easy—ideally one button click or a single shell
    command—making testing fast and always accessible.

### Functions

- *F1: Too Many Arguments*
  - Functions should have few arguments: none is ideal, then one, two, or three. Avoid using more
    than three as it reduces clarity and maintainability.
- *F2: Output Arguments*
  - Avoid output arguments—they're confusing. Let functions modify the object's state instead of
    returning changes through arguments.
- *F3: Flag Arguments*
  - Boolean arguments loudly declare that the function does more than one thing. They are confusing
    and should be eliminated.
- *F4: Dead Function*
  - Methods that are never called should be discarded. Keeping dead code around is wasteful. Don't
    be afraid to delete the function. Remember, your source code control system still remembers it.

### General

- *G1: Multiple Languages in One Source File*
  - Limit the number of languages in a source file. Mixing too many makes code confusing. Aim for
    one language per file and minimize any necessary extras.
- *G2: Obvious Behavior Is Unimplemented*
  - Following "The Principle of Least Surprise," Code should behave as expected. Follow intuitive
    naming and logic, so users trust the function without digging into its details. Avoid surprising
    or unintuitive behavior.
- *G3: Incorrect Behavior at the Boundaries*
  - Code must behave correctly in all cases. Don't rely on your intuition. Look for every boundary,
    corner case, and write a test for it to ensure reliability.
- *G4: Overridden Safeties*
  - Overriding safety features like compiler warnings or failing tests is risky. Shortcuts may ease
    development but lead to major issues later, just like ignoring safeguards did at Chernobyl.
- *G5: Duplication*
  - Code duplication signals a missed chance to abstract. Replace repeated code with methods or
    classes to improve clarity, reuse, and reduce errors.
  - Repeated switch or if/else chains and similar logic across modules are duplication. Use
    polymorphism or design patterns like Template method, or Strategy pattern to eliminate them and
    improve structure.
- *G6: Code at Wrong Level of Abstraction*
  - Keep high-level and low-level concepts separate. Place detailed logic in subclasses or specific
    modules, and keep base classes or core files focused on general behavior only.
  - Isolating abstractions is one of the hardest things that software developers do, and there is no
    quick fix when you get it wrong.
- *G7: Base Classes Depending on Their Derivatives*
  - Base classes should not depend on their derivatives. Keeping them separate allows independent
    deployment, reducing change impact and simplifying maintenance.
- *G8: Too Much Information*
  - Good modules have small, powerful interfaces with low coupling. Poor ones require many calls for
    simple tasks, increasing complexity and coupling.
  - Keep interfaces small and tight. Expose only what's necessary to reduce coupling. Hide data,
    functions, and variables to keep classes focused and maintainable.
- *G9: Dead Code*
  - Dead code lingers unused, grows outdated, and adds confusion. Delete it to keep the system
    clean, current, and maintainable.
- *G10: Variable Separation*
  - Define variables and functions close to where they're used. Keep scope small and vertical
    distance short to improve readability and maintainability.
- *G11: Inconsistency*
  - Follow consistent naming and coding patterns. Similar things should be done in similar ways to
    avoid surprises and make code easier to read and maintain.
- *G12: Clutter*
  - Remove unused code, empty constructors, and meaningless comments. Clutter reduces clarity. Keep
    source files clean and well organized.
- *G13: Artificial Coupling*
  - Avoid artificial coupling by placing functions, constants, and enums in proper locations. Don't
    group unrelated code for convenience—it harms design and clarity.
- *G14: Feature Envy*
  - A method should work with its own class's data, not rely heavily on another's. Using another
    object's accessors too much shows misplaced responsibility.
- *G15: Selector Arguments*
  - Avoid selector arguments like Booleans or enums in functions. They hide intent and mix
    behaviors. Use separate, focused functions instead.
- *G16: Obscured Intent*
  - Avoid dense code, magic numbers, and cryptic names. Clear, expressive code reveals intent and is
    easier to understand and maintain.
- *G17: Misplaced Responsibility*
  - Place code where readers expect it. Names and location should match purpose. Avoid clever
    placements that confuse intent, even if they're convenient.
- *G18: Inappropriate Static*
  - Prefer nonstatic methods unless polymorphism is clearly unnecessary. Static methods can't adapt
    to different behaviors and may limit flexibility later.
- *G19: Use Explanatory Variables*
  - Use well-named intermediate variables to break up calculations. This boosts clarity and makes
    complex code easier to read and understand.
- *G20: Function Names Should Say What They Do*
  - Function names should clearly express behavior. If you must read the code to understand what a
    function does, rename it to reflect its action and effect.
- *G21: Understand the Algorithm*
  - Don't stop at code that just "works." Understand the algorithm fully. Refactor until the logic
    is clear, expressive, and undeniably correct.
  - It's normal to question an algorithm's suitability, but not knowing what your own code does is
    simply careless.
- *G22: Make Logical Dependencies Physical*
  - Dependencies should be physical, not just assumed. A module must explicitly access what it
    needs, not rely on hidden or logical assumptions.
- *G23: Prefer Polymorphism to If/Else or Switch/Case*
  - Switch statements are often overused. Prefer polymorphism and treat every switch as a potential
    design flaw unless truly necessary.
  - "ONE SWITCH" rule: There may be no more than one switch statement for a given type of selection.
    The cases in that switch statement must create polymorphic objects that take the place of other
    such switch statements in the rest of the system.
- *G24: Follow Standard Conventions*
  - Teams should follow shared coding standards reflected in their code. Consistency matters more
    than personal style, promoting clarity and teamwork.
- *G25: Replace Magic Numbers with Named Constants*
  - Avoid magic numbers or unclear values in code. Use well-named constants to improve clarity,
    reduce errors, and ensure consistency.
- *G26: Be Precise*
  - Be precise in coding decisions. Avoid lazy assumptions, handle exceptions, and write with
    clarity to prevent ambiguity and bugs.
- *G27: Structure over Convention*
  - Prefer structural enforcement over naming conventions. Structures like abstract classes ensure
    consistency, while conventions rely on discipline alone.
- *G28: Encapsulate Conditionals*
  - Make conditionals clear by extracting them into well-named functions. It improves readability
    and reveals intent.
- *G29: Avoid Negative Conditionals*
  - Write conditionals as positives when possible. Positive expressions are clearer and easier to
    understand than negatives.
- *G30: Functions Should Do One Thing*
  - Avoid functions that do many things. Break them into smaller functions, each focused on a single
    task, to improve clarity and maintainability.
- *G31: Hidden Temporal Couplings*
  - Make temporal coupling clear. Design function arguments to reflect the required call order,
    avoiding hidden dependencies.
- *G32: Don't Be Arbitrary*
  - Structure code with purpose and consistency. Clear, intentional design encourages others to
    follow and maintain the same conventions.
- *G33: Encapsulate Boundary Conditions*
  - Handle boundary conditions in one place using well-named variables. This avoids scattered logic
    like +1 or -1 and improves clarity and maintainability.
- *G34: Functions Should Descend Only One Level of Abstraction*
  - Keep all statements in a function at the same abstraction level, just below the function's name.
    Mixing levels harms clarity and makes code harder to follow.
- *G35: Keep Configurable Data at High Levels*
  - Keep high-level constants visible and configurable at the top. Pass them as arguments to
    lower-level functions instead of burying them deep in the code.
- *G36: Avoid Transitive Navigation*
  - Follow the Law of Demeter. Modules should only interact with immediate collaborators, not
    navigate deep object chains like `a.getB().getC().doSomething()`.

### Names

- *N1: Choose Descriptive Names*
  - Choose names carefully and review them often. Good names make code more readable and set clear
    expectations for behavior and structure.
- *N2: Choose Names at the Appropriate Level of Abstraction*
  - Name things to match their level of abstraction. Avoid implementation details in names, and
    refactor names as your code evolves to keep it clear and flexible.
- *N3: Use Standard Nomenclature Where Possible*
  - Use familiar naming conventions and project-specific language to improve code clarity. Following
    known patterns helps readers understand code quickly.
- *N4: Unambiguous Names*
  - Pick names that clearly state what a function or variable does. Clarity is more important than
    brevity, especially when the name removes ambiguity.
- *N5: Use Long Names for Long Scopes*
  - Use short names for short scopes and longer, more descriptive names for wider scopes. Name
    length should match how far the variable or function travels.
- *N6: Avoid Encodings*
  - Avoid encoding names with type or scope info like *m_*. Modern tools make such prefixes
    unnecessary and distracting.
- *N7: Names Should Describe Side-Effects*
  - Names should reveal all actions a function performs. Avoid hiding side effects with simple
    names. Be explicit if a function does more than it appears.

### Tests

- *T1: Insufficient Tests*
  - A test suite should cover everything that might break. If conditions or calculations are
    untested, the suite is incomplete.
- *T2: Use a Coverage Tool!*
  - Coverage tools reveal untested code and help identify gaps. Visual cues in IDEs make it easy to
    spot untested logic like unchecked if or catch blocks.
- *T3: Don't Skip Trivial Tests*
  - They are easy to write, and their documentary value is higher than the cost to produce them.
- *T4: An Ignored Test Is a Question about an Ambiguity*
  - Ignored tests highlight unclear requirements. Use them to document questions about behavior,
    either with relevant attributes or comments, depending on what compiles.
- *T5: Test Boundary Conditions*
  - Take special care to test boundary conditions. We often get the middle of an algorithm right but
    misjudge the boundaries.
- *T6: Exhaustively Test Near Bugs*
  - Bugs tend to congregate. When you find a bug in a function, it is wise to do an exhaustive test
    of that function. You'll probably find that the bug was not alone.
- *T7: Patterns of Failure Are Revealing*
  - Well-ordered, complete tests can reveal failure patterns that help diagnose bugs quickly.
    Patterns in test results often lead to key insights.
- *T8: Test Coverage Patterns Can Be Revealing*
  - Looking at the code that is or is not executed by the passing tests gives clues to why the
    failing tests fail.
- *T9: Tests Should Be Fast*
  - A slow test is a test that won't get run. When things get tight, it's the slow tests that will
    be dropped from the suite. So do what you must to keep your tests fast.

---
