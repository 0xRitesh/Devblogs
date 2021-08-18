![banner.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1629298912214/UGIDwR3gI.png)

## art of writing a good commit message
Hi there, In this article, I will be discussing the importance of commit messages and I'll walk you through a format that will assist you in crafting effective commit messages.


> “A commit message shows whether a developer is a good collaborator.”

-Peter Hutterer, *Senior Software Engineer at Red Hat*

#### **Let's start with an explanation of what a commit message is:**

A commit message is a short description of the changes you've made to a file added before committing the changes. It is one of the most common ways for developers to communicate with one another & important to properly express any changes so that someone else reading it isn't left in the dark. 

If you browse through a random GitHub repository, you'll frequently come across an extremely random commit message that is not descriptive and is difficult to understand.
So, It is essential that you take the time to write a proper commit message. Good commit messages are important not only for the people working on the project with you but also for you to keep track of all your commits and know exactly what changes were made during that commit.

**To compose a good commit message, I will recommend using This Commit Message Style Guide**


### Defining a Commit Message Convention

---
`type(scope): subject`

`body (optional)`

`footer (optional)`



The commit contains the following structural elements, to communicate intent to the consumers:
 
###  Type of commit
---
- ** feat - a new feature**

-  **fix - a bug fix**

-  **docs - changes in documentation**

-  **style - everything related to styling**

-  **refactor - code changes that neither fixes a bug or adds a feature**

-  **test - everything related to testing**

-  **chore - updating build tasks, package manager configs, etc**

### Scope of commit (Optional)
---
A scope MUST consist of a noun describing a section of the codebase affected by the changes (or simply the epic name) surrounded by parenthesis. Example:

### Subject
---
This contains a short description of the changes made. It shouldn't be greater than 50 characters, should begin with a capital letter and written in the imperative eg. Add instead of Added or Adds.

### Body
---
The body is used to explain what changes you made and why you made them. Not all commits are complex enough that they need a body, especially if you are working on a personal project alone, and as such writing a body is optional.
A blank line between the body and the subject is required and each line should have no more than 72 characters.


### Footer
---
The footer is also optional and mainly used when you are using an issue tracker to reference the issue ID.
Good commit messages serve at least three important purposes:

To speed up the reviewing process.
To help us write a good release note.
To help the future maintainers of Erlang/OTP (it could be you!), say five years into the future, to find out why a particular change was made to the code or why a specific feature was added.

### Example of a good commit message used by  [Udacity ](https://udacity.github.io/git-styleguide/) 


> feat: Summarize changes in around 50 characters or less

> More detailed explanatory text, if necessary. Wrap it to about 72
characters or so. In some contexts, the first line is treated as the
subject of the commit and the rest of the text as the body. The
blank line separating the summary from the body is critical (unless
you omit the body entirely); various tools like log, shortlog
and rebase can get confused if you run the two together.

> Explain the problem that this commit is solving. Focus on why you
are making this change as opposed to how (the code explains that).
Are there side effects or other unintuitive consequences of this
change? Here's the place to explain to them.

> Further paragraphs come after blank lines.

>- Bullet points are okay, too

> - Typically a hyphen or asterisk is used for the bullet, preceded
by a single space, with blank lines in between, but conventions
vary here

> If you use an issue tracker, put references to them at the bottom,
like this:

> Resolves: #123
See also: #456, #789

Some more simple examples :

> feat: JIRA-123 -implement new set-group api

> docs: added banner in README.md


While writing a commit message, keeping these things in mind

### Rules for a great git commit message style
* Separate subject from body with a blank line
* Do not end the subject line with a period
* Capitalize the subject line and each paragraph
* Use the imperative mood in the subject line
* Wrap lines at 72 characters
* Use the body to explain what and why you have done something. In most cases, you can leave out details about how a change has been made.

### Information in commit messages
* Describe why a change is being made.
* How does it address the issue?
* What effects does the patch have?
* Do not assume the reviewer understands what the original problem was.
* Do not assume the code is self-evident/self-documenting.
* Read the commit message to see if it hints at improved code structure.
* The first commit line is the most important.
* Describe any limitations of the current code.
* Do not include patch set-specific comments.

## Summarizing the Commit Message Guide

```
type(scope): subject 
<body>
<footer>
```

### 1. Type of commit
```
feat:     The new feature being added to a particular application
fix:      A bug fix
style:    Feature and updates related to styling
refactor: Refactoring a specific section of the codebase
test:     Everything related to testing
docs:     Everything related to documentation
chore:    Regular code maintenance
```

### 2. Scope (optional)
Provided in parentheses after the type of commit, describing parts of the code affected by the changes or simply the epic name.
```
feat(claims)
fix(orders)
```

### 3. Subject
Short description of the applied changes.
- Limit the subject line to 50 characters
- Your commit message should not contain any whitespace errors or punctuation marks
- Do not end the subject line with a period
- Use the present tense or imperative mood in the subject line
```
feat(claims): add claims detail page
fix(orders): validation of custom specification
```

### 4. Body (Optional)
Use the body to explain what changes you have made and why you made them.
- Separate the subject from the body with a blank line
- Limit each line to 72 characters
- Do not assume the reviewer understands what the original problem was, ensure you add it
- Do not think your code is self-explanatory

```
refactor!: drop support for Node 6
BREAKING CHANGE: refactor to use JavaScript features not available in Node 6.
```

### 5. Footer (optional)
Use this section to reference issues affected by the code changes or comment to another developers or testers.

```
fix(orders): correct minor typos in code
See the issue for details
on typos fixed.
Reviewed-by: @John Doe
Refs #133
```


#### references
* http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html
* https://wiki.openstack.org/wiki/GitCommitMessages
* http://chris.beams.io/posts/git-commit/
* https://www.conventionalcommits.org/en/v1.0.0-beta.2/#why-use-conventional-commits
* https://github.com/conventional-changelog/commitlint/tree/master/@commitlint/config-conventional

### Thanks for reading! 
Let me know your thoughts and feedback in the comments section.



