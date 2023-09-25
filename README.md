# Exploratory Testing Checklists and Heuristics

VS Code snippets created using <https://www.ministryoftesting.com/articles/5631d7b0?s_id=14717348> and test heuristics cheatsheet by Elisabeth Hendrickson, James Lyndsay, Dale Emery. See pdf files in `attachments` folder.

## Links

1. [GitHub - ckenst/testing-guides: A set of guides and catalogs to help test software](https://github.com/ckenst/testing-guides)
2. [Checklist for Testing Web Page Functionality | Ministry of Testing](https://www.ministryoftesting.com/articles/5631d7b0?s_id=14717348)
3. [Snippet generator](https://snippet-generator.app/)

## Installation

Copy snippets from markdown.json in this repo to your VS Code folder markdown.json file. For macOS VS Code folder with snippets is typically located in

- `/Users/username/Library/Application Support/Code/User/snippets/markdown.json`

You can find your snippets following these steps

1. `Cmd+Shift+P` (macOS)
2. Select `Snippets: Configure user snippets`
3. Select `markdown.json`

## VS Code Editor Settings

This enables suggestions in markdown files. Make sure to set `"editor.suggest.showSnippets": true` 

Also I find this extension is very useful when working with markdown:
- [DavidAnson/vscode-markdownlint: Markdown linting and style checking for Visual Studio Code](https://github.com/DavidAnson/vscode-markdownlint)

Here are example settings for markdown that I use.

1. `Cmd+Shift+P` (macOS)
2. Type 'Preferences: Open User Settings (JSON)'
3. Select `markdown.json`

```json
  "[markdown]": {
  "editor.quickSuggestions": {
   "other": true,
   "comments": true,
   "strings": true
  },
  "editor.tabCompletion": "onlySnippets",
  "editor.wordBasedSuggestions": true,
  "editor.tabSize": 2,
  "editor.suggest.showSnippets": true,
  "editor.snippetSuggestions": "top",
  "editor.defaultFormatter": "DavidAnson.vscode-markdownlint",
  "editor.inlineSuggest.enabled": false
 },
```


## Usage Example

1. Create markdown file
2. Start typing in VS code editor `/dta paths file`. This will trigger markdown text snippet suggestions.
3. Select option fom suggestions.
4. Press `Enter`.
5. Selected snippet will be inserted.

Markdown file:  

![Markdown file](media/example1.png)

Result:  

![result](media/example3.jpg)

markdown.json:  

![markdown.json](media/example2.jpg)

## Data type attacks

- Data type attack text field (1)
  - prefix: `/dta text field 1`
  - [ ] valid data
  - [ ] invalid data
  - [ ] letters
  - [ ] numbers
  - [ ] blank or empty
  - [ ] mandatory fields  |

- Data type attack text field (2)
  - prefix: `/dta text field 2`
  - [ ] minimum and maximum length
  - [ ] space
  - [ ] long (64, 255, 256, 257, 1000, 1024, 2000, 2048 or more characters)
  - [ ] short (1,2, 3 characters)
  - [ ] one word
  - [ ] multiple words  

- Data type attack text field (3)
  - prefix: `/dta text field 3`
  - [ ] space leading/trailing/in the middle
  - [ ] tabs
  - [ ] null value
  - [ ] special characters (such as<!#$|%)
  - [ ] emojis 😀👍
  - [ ] line break  

- Data type attack (5)
  - prefix: `/dta text field 5`, `/dta text field 5`
  - [ ] accessibility: tab navigation
  - [ ] existing value
  - [ ] Hidden text
  - [ ] Usability: Different browsers
  - [ ] Usability: Browser zoom in/out
  - [ ] Security: Extremely big requests
  - [ ] Scenario: "nasty words"  

- Data type attack  paths, files
  - prefix `/dta paths file◊s`
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
  - prefix `/dta time date`
  - [ ] Timeouts
  - [ ] Time Difference between Machines
  - [ ] Crossing Time Zones
  - [ ] Leap Days, leap years
  - [ ] Always Invalid Days (Feb 30, Sept 31)
  - [ ] Feb 29 in Non-Leap Years
  - [ ] Different Formats (June 5, 2001; 06/05/2001; 06/05/01; 06-05-01; 6/5/2001 12:34)
  - [ ] Daylight Savings
  - [ ] Changeover
  - [ ] Reset Clock Backward or Forward  

- Data text size with spaces
  - prefix `/dts w spaces`
  - [ ] 128b: `Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.Lorem`
  - [ ] 129b: `Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.Lorem `

## Heuristics

- Quality areas
  - prefix `/heuristic quality areas`
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
  - prefix `/heuristic SFDIPOT`
  - (S) structure
  - (F) function
  - (D) data
  - (I) interfaces
  - (P) platform
  - (O) operations
  - (T) time  

- Heuristic CRUD
  - prefix `/heuristic CRUD`
  - (C) create
  - (R) read
  - (U) update
  - (D) delete  

- Heuristic FDSFSCURA
  - prefix: `/heuristic FDSFSCURA`
  - (F) functional testing
  - (D) domain testing
  - (S) stress testing
  - (F) flow testing
  - (S) scenario testing
  - (C) claims testing
  - (U) user testing
  - (R) risk testing
  - (A) automated checking  

- Heuristic HICCUPS
  - prefix: `/heuristic HICCUPS`
  - (H) history
  - (I) image
  - (C) comparable products
  - (C) claims
  - (U) user's expectations
  - (P) product itself
  - (P) purpose
  - (S) statutes  

- Heuristic CRUCSS-CPID
  - prefix: `/heuristic CRUCSS-CPID`
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

- Heuristic follow the data
  - prefix: `/heuristic follow the data`
  - Perform a sequence of actions involving data, verifying the data integrity at each step.
  - (Example: Enter → Search → Report → Export → Import → Update → View)
- Heuristic interruptions
  - prefix: `/heuristic interruptions`
  - Perform actions that interrupt some workflow, verifying that system or module gracefully system handles such events
  - Log Off, Shut Down, Reboot, Kill Process, Disconnect, Hibernate, Timeout, Cancel
- Heuristic dependencies
  - prefix: `/heuristic dependencies`
  - Identify “has a” relationships (a Customer has an Invoice; an Invoice has multiple Line Items). Apply CRUD, Count, Position, and/or Selection heuristics (Customer has 0, 1, many Invoices; Invoice has 0, 1, many Line Items; Delete last Line Item then Read; Update first Line Item; Some, None, All Line Items are taxable; Delete Customer with 0, 1, Many Invoices)  

- Heuristics list
  - prefix: `/heuristics list`
  - HICCUPS
  - SFDIPOT
  - CRUD
  - FDSFSCURA
  - CRUCSS-CPID
  - Follow the data
  - Interruptions
  - Goldilocks
  - Boundaries
  - Dependencies
  - Constraints
  - Input Method
  - State Analysis
  - Users & Scenarios  

## Testing types

- Basic test types
  - prefix `/testing types`
  - [ ] Basic positive tests (happy paths)
  - [ ] Extended positive testing with optional parameters
  - [ ] Negative testing with valid input (for example, trying to add an existing username)
  - [ ] Negative testing with invalid input (trying to add a username which is null)
  - [ ] Destructive testing (for example, fill in long text into input field).
  - [ ] UI verification.
  - [ ] Accessibility testing.
  - [ ] Usability testing
  - [ ] Security testing.
  - [ ] Mobile testing
  - [ ] Performance testing.
  - [ ] Compatibility testing.  

## Accessibility

- Accessibility checklist 1
  - prefix `/checklist ac1`
  - [ ] Google Chrome Lighthouse. Accessibility score
  - [ ] Keyboard Navigation. All interactive elements are accessible through the keyboard
  - [ ] Keyboard Navigation. Non-interactive elements are not focusable
  - [ ] Text. Sufficient text size, color contrast
  - [ ] Images. Alt text for important pictures. Empty alt text for pictures that lack importance
  - [ ] w3.org/WAI/tutorials/  

- Accessibility testing checklist 2
  - prefix `/checklist ac2`
  - [ ] Elements. It is clearly shown what object is active
  - [ ] Images. Pictures are not used to represent only textual content
  - [ ] HTML. No big validation errors in the HTML/XHTML code
  - [ ] Labels. Forms use the correct label for every element
  - [ ] Media. Any video/sound content has textual alternatives explaining the content  

## Security

- Security testing checklist 1
  - prefix: `/checklist sec1`, `/security1`
  - [ ] html-tags `<blink>Hello there</blink>`
  - [ ] js injection `<script>alert('Executing JS')</script>`
  - [ ] js injection single quote `'-prompt()-'`
  - [ ] broken html `<i><b>Bold</i></b>`
  - [ ] sql injection `and  ‘1’=’1`
  - [ ] sql injection `admin'--`
  - [ ] reasonable limit for input field (characters, file size, number, etc)
  - [ ] Unexpected errors: The system must not show information about server, database etc
  - [ ] Input fields are validated, sanitized on both  frontend and backend
  - [ ] Session variables can't be accessed /manipulated, for example via address bar  

- Security testing checklist 2 authentication
  - prefix: `/checklist sec2`, `/security auth`
  - [ ] Cookies are saved  encrypted  and cannot be read/manipulated
  - [ ] You cannot access other users' documents, accounts, orders, etc.
  - [ ] You cannot access private resources without authentication
  - [ ] You cannot create, update, delete data using other users' authentication
  - [ ] Password hash is used  

- Security testing checklist 3 OWASP top 10 API
  - prefix: `/checklist sec3`, `/security owasp api`
  - [ ] Broken object level authorization
  - [ ] Broken user authentication
  - [ ] Excessive data exposure
  - [ ] Lack of resource limiting and rate limiting
  - [ ] Broken function level authorization
  - [ ] Mass assignment
  - [ ] Injections
  - [ ] Improper assets management
  - [ ] Insufficient logging and monitoring

## Compatibility

- Top 10 most common screen resolutions
  - prefix: `/checklist screen size`
  1) 1920×1080 (22%)
  2) 1366×768 (11%)
  3) 1440×900 (9%)
  4) 1536×864 (8%)
  5) 2560×1440 (7%)
  6) 1680×1050 (4%)
  7) 1280×720 (3%)
  8) 1280×800 (2%)
  9) 1792×1120 (2%)
  10) 1600×900 (1%)

## Usability

- Usability testing checklist 1
  - prefix: `/checklist usability1`
  - [ ] Consistent language
  - [ ] Consistent use of fonts
  - [ ] Correct alignment of text, numbers and fields
  - [ ] Correct spelling and grammar
  - [ ] Correct tab order
  - [ ] Error messages (language, spelling, grammar)
  - [ ] Objects have a consistent shape and size (buttons, images etc)
  - [ ] Inactive links and objects are clearly disabled (grey, toned down, not shown)

- Usability testing checklist 2
  - prefix: `/checklist usability2
  - [ ] No broken links, images or objects
  - [ ] Test with different screen sizes
  - [ ] Test with different browsers
  - [ ] Test with different devices
  - [ ] Dark-light mode
  - [ ] Scroll bars are not shown if not needed
  - [ ] Scroll bars are shown if needed
  - [ ] Windows can be resized without losing functionality


