# Today's practice

1. ### More question types
1. ### Clauses

# Useful links

* [Temporary access point](https://klte.ch)
* [Setting variables documentation](https://docassemble.org/docs/fields.html)
* [Flightdeck](https://www.kemplittle.com/flightdeck/)

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

# Template drafting

## Shareholders agreement conduct

```
3.	CONDUCT OF THE COMPANY’S AFFAIRS
	The Shareholders shall exercise all rights available to them in relation to the Company and the Company shall do everything necessary to procure (so far as they are each able to do so) that during the term of this Agreement:
3.1	the business of the Company consists exclusively of the Business.
3.2	[the Shareholders are supplied with [[monthly/quarterly] management accounts] OR [the annual accounts];]
3.3	the Company complies with the provisions of the Articles;
3.4	[any company which becomes a subsidiary of the Company adopts new articles of association in a form approved by a Majority of Shareholders in writing;]
3.5	all cheques drawn and electronic bank transfers processed by the Company and any Group Company, are signed (in the case of cheques) or authorised (in the case of electronic bank transfers) by an executive Director;
3.6	board meetings of the Company are convened at regular intervals, not less than [one each calendar quarter], by not less than 48 hours’ notice in writing accompanied by an agenda specifying the business to be transacted; and
3.7	the Board determines the general policy of the Company (subject to the express provisions of this Agreement and the Articles) including the scope of their respective activities and operations and that the Board reserves to itself all matters involving major or unusual decisions.
```

## Evaluation agreement IPR

```
7.	INTELLECTUAL PROPERTY RIGHTS
7.1	Subject to any express provision in this Agreement to the contrary, each party acknowledges and agrees that this Agreement does not assign or transfer any Intellectual Property Rights between the parties and that nothing in this Agreement shall be deemed to give a party any right, title or interest whatsoever in the other party’s Intellectual Property Rights. 
7.2	The grant or licence of Intellectual Property Rights under this clause 7 are subject to 
(a)	the Customer’s compliance with the terms and conditions of this Agreement; and
(b)	receipt by Supplier of payment of the Licence Fees in full.
7.3	Supplier grants to the Customer a non-exclusive, non-transferable, non-sublicensable, personal licence to use the Software [(in object code form)] for the Licence Purpose during the Licence Period, solely for its own internal business purposes, and not for the benefit of any third party, to:
(a)	at any one time, run and use [a single version][the Licensed Number of versions] of the Software[ on one [or more] computer systems][; and
(b)	for development, test and/or disaster recovery purposes only, run and use the Software.
```

## [PLC Agile Development agreement](https://uk.practicallaw.thomsonreuters.com/3-547-1866)

## [Commercial boilerplate](https://kl-mbl.imanagework.co.uk/work/link/d/KL_CLOUD!10124740.1)

