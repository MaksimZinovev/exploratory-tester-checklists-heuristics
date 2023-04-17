# Exploratory tester checklists heuristics

VS Code snippets created using <https://www.ministryoftesting.com/articles/5631d7b0?s_id=14717348> and test heuristics cheatsheet by Elisabeth Hendrickson, James Lyndsay, and Dale Emery

## Install

Copy snippets from markdown.json to your markdown.json file.

## Usage

Example 1:

1. Start typing in VS code editor `dta 1`.
2. Select option fom suggestions.
3. Press enter
4. Snippet will be inserted

![](media/example1.png)

## Data type attacks

- Data type attack text field (1)
  - [ ] valid data
  - [ ] letters
  - [ ] numbers
  - [ ] blank or empty
  - [ ] mandatory fields
- Data type attack text field (2)
  - [ ] minimum and maximum length
  - [ ] long (64, 255, 256, 257, 1000, 1024, 2000, 2048 or more characters)
  - [ ] short (1,2, 3 characters)
  - [ ] one word
  - [ ] multiple words
- Data type attack text field (3)
  - [ ] leading/trailing space
  - [ ] line break
  - [ ] tabs
  - [ ] null value
  - [ ] HTML-tags
  - [ ] special characters (such as<!#$|%)
  - [ ] emojis 😀👍
- Data type attack  paths, files
  - [ ] Long Name (>255 chars)
  - [ ] Special Characters in Name (`space * ? / \ | < > , . ( ) [ ] { } ; : ‘ “ !
@ # $ % ^ &`)
  - [ ] Non-Existent
  - [ ] Already Exists
  - [ ] No Space
  - [ ] Minimal Space
  - [ ] Write protected
  - [ ] Unavailable
  - [ ] Locked
  - [ ] On Remote Machine
  - [ ] Corrupted
- Data type attack time and date
  - [ ] Timeouts
  - [ ] Time Difference between Machines
  - [ ] Crossing Time Zones
  - [ ] Leap Days
  - [ ] Always Invalid Days (Feb 30, Sept 31)
  - [ ] Feb 29 in Non-Leap Years
  - [ ] Different Formats (June 5, 2001; 06/05/2001; 06/05/01; 06-05-01; 6/5/2001 12:34)
  - [ ] Daylight Savings
  - [ ] Changeover
  - [ ] Reset Clock Backward or Forward

## Heuristics

- Quality areas
  - (C) capability
  - (R) reliability
  - (U) usability
  - (C) charisma
  - (S) security
  - (S) scalability
  - (C) compatibility
  - (P) performance
  - (I) installability
  - (D) development
- Heuristic SFDIPOT
  - (S) structure
  - (F) function
  - (D) data
  - (I) interfaces
  - (P) platform
  - (O) operations
  - (T) time
- Heuristic CRUD
  - (C) create
  - (R) read
  - (U) update
  - (D) delete