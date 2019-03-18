# Today's practice

1. ### YAML
1. ### The playground
1. ### Markdown
1. ### Setting variables

# Useful links

* [Docassemble authoring guide](https://docassemble.org/docs/interviews.html)
* [General markdown syntax](https://daringfireball.net/projects/markdown/)
* [Docassemble markdown syntax](https://docassemble.org/docs/markup.html)
* [Setting variables documentation](https://docassemble.org/docs/fields.html)
* [Main site](https://klt.rocks)
* [Backup site](https://docasm02.azurewebsites.net)

# Code

#### Buttons
```
metadata:
  title: Buttons
  documentation: "https://docassemble.org/docs/fields.html#field with buttons"
---
field: user_gender
question: What is your gender?
buttons:
  - Male
  - Female
---
question: Result of question
subquestion: |
  You are ${ user_gender }.
mandatory: True
```

#### Radio buttons
```
metadata:
  title: Radio buttons
  documentation: "https://docassemble.org/docs/fields.html#field with choices"
---
question: |
  What type of shoes do you wear?
field: target_variable
choices:
  - Sneakers
  - Sandals
  - Clogs
  - Other
---
question: Result of question
subquestion: |
  target_variable is: "${ target_variable }"
mandatory: True
```

#### Radio with help

```metadata:
  title: Radio buttons with help
  documentation: "https://docassemble.org/docs/fields.html#field with choices"
---
question: |
  What type of shoes do you wear?
field: target_variable
choices:
  - Sneakers: sneakers
    help: |
      Comfortable shoes.
  - Sandals: sandals
    help: |
      For summer.
  - Clogs: clogs
    help: |
      For hippies.
  - Other: other
    default: True
    help: |
      Because the other types suck.
---
question: Result of question
subquestion: |
  target_variable is: "${ target_variable }"
mandatory: True
```

### Date picker

```
metadata:
  title: Date
  documentation: "https://docassemble.org/docs/fields.html#date"
---
question: |
  What is your date of birth?
fields:
  - Birthdate: target_variable
    datatype: date
---
question: Result of question
subquestion: |
  When inserted in into a question,
  `target_variable` looks like
  ${ target_variable }.
  But `target_variable` is also a
  special date object.
  For example, when you were one
  week old, the date was
  ${ target_variable.plus(days=7) }.
  Toggle "Source" in the navigation bar
  to see the source code for this screen.
mandatory: True
```

### Sliders

```
metadata:
  title: Range slider
  short title: Range slider
  documentation: "https://docassemble.org/docs/fields.html#range"
---
question: |
  On a scale from 1 to 10, how
  much do you like these animals?
fields:
  - Possums: possum_preference
    datatype: range
    min: 1
    max: 10
    step: 0.5
  - Rabbits: rabbit_preference
    datatype: range
    min: 1
    max: 10
---
question: |
  % if possum_preference > 7:
  You really like possums!
  % elif possum_preference > 3:
  You think possums are ok.
  % else:
  I guess you don't really like possums.
  % endif
  % if rabbit_preference > 7:
  You really like rabbits!
  % elif rabbit_preference > 3:
  You think rabbits are ok.
  % else:
  I guess you don't really like rabbits.
  % endif
mandatory: True
```
