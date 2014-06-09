KhanAcademy_code_analysis
=========================

Khan Academy Interview Project

### Step 1: Check out the intro CS videos to know what the questions look like
- The early drawing ones are very very simple (no structure) and the hints are pretty good
- This sort of code is more useful in the later programming logic challengs
  - One use case for the core code would be to match different patterns and do things conditionally (e.x. "you are using an if without an else" a la Flashy Flash card)
  
### Step 2: Look into the technology available
- Esprima:
  - IE 8+
  - Triple the popularity on GitHub
  - Older
  - Not very extensive public docs
- Acorn: 
  - Slightly faster
  - Very similar by it's creator's admission
  - Good source-code documentation
  - Good usage docs
  - parse_dammit :)
  - Smaller source code
  - Support for IE6+
- astjs:
  - Based on esprima
  - Provides pattern matching
  - A good place to start looking at techniques
- jsgrep:
  - No longer supported
  - No claims about support
  
### Goals:
- Positive pattern match or fail
- Structured pattern match or fail
- Negative match or fail
- Return generic error messages
- Include variable names in error messages
- Scrape KhanAcademy and inject script into CS console


-----------------------------
### What Blocks?
- If
- Else
- While
- For
- Variable declaration
- Assignment
- Increment/Decrement?
- Function calls
- Expressions
  - Structured style variable match fail-over? (This is computationally super-expensive)

#### Edge Cases to consider
- Strip empty statements from pattern
- Separate declaration and instantiation;
- Warn if the grammar includes uncheckable content:
    - Recursing into switch-case
    - Expressions in if(), for(), while(), switch(), function param names

-Full disclosure: let the commite logs show this is the moment I found structured.js

### Todo:
- Web Workers that will cancel remaining tests if it is terminated.
- Check if es5-shim is already loaded in the main page
