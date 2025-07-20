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
