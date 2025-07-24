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
