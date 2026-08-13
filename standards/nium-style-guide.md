# Nium Style Guide

Follow these guidelines to create Nium documentation.

In addition to these guidelines, we use:

* The [_Microsoft Manual of Style_](https://docs.microsoft.com/en-us/style-guide/welcome/) for user interface style and formatting
* The [_AP Stylebook_](https://www.apstylebook.com)
* [_The Chicago Manual of Style_](https://www.chicagomanualofstyle.org/home.html)
* [U.S. federal plain language guidelines](https://plainlanguage.gov/guidelines/)
* [_GitLab Markdown Style Guide_](https://about.gitlab.com/handbook/markdown-guide/)

In cases of conflict between our guidelines and the ones listed, use our guidelines.

# Target audiences and products

We address two audiences in our documentation: clients and customers. We estimate that 70% of our audience is product developers and 10% is customers. Many of our readers speak English as a second language.

| **Audience** | **Who they are** |
| --- | --- |
| Client | The client is our customer. The client is also our partner. Sometimes we call the client the Nium One platform client. The client is a money movement service that wants to onboard their individual customers or businesses. The client is an enterprise that wants to issue financial instruments, such as cards, for their customers or employees. The client is directly associated with Nium. Nium creates an entity for the client when they're onboarded to the platform. Nium manages multiple client-level parameters under the client entity. Nium enters these client-level details into the system based on the program application form that the client fills out as the first step of onboarding. |
| Customer | The client onboards the customer under them. The customer is an actual cardholder. There are two types of customers: **Corporate:** This customer has employees that need to have the client send them money such as salary compensation. **Individual:** The corporate employee, for example, needs to be onboarded as an individual Nium customer. |

| **Audience products** | **What they are** |
| --- | --- |
| Wallet | A wallet is a multicurrency virtual purse account that Nium helps a customer use with multicurrency banks in 190 countries. Nium has a bank account. You can send money from one wallet to another, from one customer to the other. A wallet has cash. It can wire money and it can send and receive money in different ways. It can do a wallet-to-wallet transfer. |
| Card | Wallets have cards. A customer can issue two types of cards. A **virtual card** is a full-function card with a 16-digit number, complete with a card verification number and an expiration date. This card acts in the same way for an online transaction without the need for a physical card. A **physical card** is an actual piece of plastic that a customer issues to a cardholder to spend online and offline. A card is printed with a 16-digit number, complete with a card verification number, expiration date, and scheme name. The card can be personalized to your customer such as display their preferred name or corporate name (for corporate card use case), and Nium can issue it in bulk without any customer information. Nium still issues it with a full card number, card verification number, and expiration date. |
| Payin | Receive money in 35 countries through bank transfers, cards, and wallets. |
| Payout | Send money on demand to more than 190 countries. More than 100 countries send money in real time. |

# Writing guidelines quick reference

| **Yes** |
| --- |
| Use US English |
| Use the Oxford comma |
| Use Nium's voice and tone |
| Write for a global audience |
| Write in active voice |
| Use present simple tense |
| Write to _**you**_ |
| Write for scanning |
| Keep sentences short, concise, and positive |
| Write effective links |
| Write effective lists |
| Make effective tables |
| Write file name extensions correctly |

| **No** |
| --- |
| No ampersands |
| Don't humanize inanimate objects |
| Don't use please or thank you |
| Don't editorialize, just state facts. Don't express an opinion in the form of an editorial in your text. |
| Don't use very, quite, quickly, easily, effectively; omit unnecessary adverbs—words that describe how, when, or where. Unless they're important to the meaning of a statement, leave them out. |
| Don't use current, see Avoid redundancies |
| Don't use jargon |
| Avoid the future tense; use present continuous instead |

# Use US English

Use standard United States (US) English and keep a conversational casual business tone.

**Use US spelling.** Use US English spelling for English words whose spelling varies by locale, such as the UK. For example, use _license,_ not _licence._
Avoid non-English words or phrases. For example, use _in fact_, not _de facto,_ or use _necessary_, not _ad hoc_.

When in doubt about the US spelling of a word, use the first spelling in the [Merriam-Webster](https://www.merriam-webster.com/) or the [The American Heritage Dictionary](https://www.ahdictionary.com/) instead of the "also xxxx" spelling variants.

# Contractions

**Use contractions.** We recommend using most types of contractions. Contractions are useful because it's easy for a reader to miss the word _not_, whereas it's harder for a reader to misread _don't_ as _do_. If you need to emphasize the negative, use text formatting such as "is `<em>`not`</em>`," which renders as "is _not_."

Avoid ambiguous or awkward contractions, such as _there'd, it'll,_ and _they'd._

# Capitalization

Nium style uses sentence-case capitalization. That means you only capitalize the first letter of the first word of a sentence and lowercase everything else, except for proper nouns, which include the names of brands, products, services, and APIs.

Follow these guidelines in Nium content:

* Use sentence-case capitalization all the time. That means:
    * Capitalize the first word of a sentence, heading, title, UI label (such as the name of a button or checkbox), or a standalone phrase.
    * Capitalize proper nouns. See [Nouns and pronouns](https://learn.microsoft.com/en-us/style-guide/grammar/nouns-pronouns).
    * Use lowercase for everything else.
* Always capitalize the first word of a new sentence. Rewrite sentences that start with a word that's always lowercase.
* Don't use all uppercase for emphasis. It's OK to use italic sparingly for emphasis.
* Don't use all lowercase as a design choice. Although all uppercase is used occasionally as a design element, don't use it in text.
* Don't use internal capitalization unless it's part of a brand name.
* Don't capitalize the spelled-out form of an acronym unless it's a proper noun.
* When words are joined by a slash, capitalize the word after the slash if the word before the slash is capitalized.
  **Examples**
  Country/Region
  Turn on the On/Off toggle.
* For information on capitalization in hyphenated compound words see [Hyphens](https://learn.microsoft.com/en-us/style-guide/punctuation/dashes-hyphens/hyphens).

To learn more about capitalization, see [_The Chicago Manual of Style_](http://www.chicagomanualofstyle.org/home.html). If you're not sure whether to capitalize a term, check the A–Z word list and [_The American Heritage Dictionary_](https://ahdictionary.com/).

For information about capitalizing UI labels in instructions, see [Formatting text in instructions](https://learn.microsoft.com/en-us/style-guide/procedures-instructions/formatting-text-in-instructions).

## Title-case capitalization

Occasionally, title-case capitalization—capitalizing most words—is appropriate. For example, product and service names, the names of blogs, book and song titles, article titles in citations, white paper titles, and titles of people (_Vice President_ or _Director of Marketing_) require title-style capitalization. In a tweet, it's OK to use title-style capitalization to highlight the name of a quoted article.

On the rare occasions when title-case capitalization is required, follow these guidelines:

* Always capitalize the first and last words.
  **Example**
  A Home to Go Back To
* Capitalize all other words, including nouns, verbs (including _is_ and other forms of _be_), adverbs (including _very_ and _too_), adjectives, and pronouns (including _this, that,_ and _its_).
  **Examples**
  Enterprise Agility Is Not an Oxymoron
  This Is All There Is
  Teaching Math Over and Over Again, in Less Time Than Before
* Capitalize the word after a hyphen if it would be capitalized without the hyphen or if it's the last word.
  **Examples**
  Self-Paced Training for GitHub Desktop
  GitHub Management Console: Five Essential Snap-Ins
  Five Essential Snap-ins for GitHub Management Console
  Copy-and-Paste Support in Windows Apps
* Capitalize the first word of labels and terms that appear in UI and APIs unless they're always lowercase (for example, _fdisk_).
* In programming languages, follow the traditional capitalization of keywords and other special terms.

# Punctuation

## Em dash

Use the em dash, also known as a long dash, like a comma, a colon, or a parenthesis. Instead of using a comma or parentheses, an em dash can help you set off extra information or break the flow in a sentence, such as examples, explanatory or descriptive phrases, or supplemental facts. Like a colon, an em dash can also introduce a clause that explains or expands upon something that precedes it.
The em dash is sometimes considered a less formal equivalent of the colon and parenthesis.
Don't add a space before or after it. Most technical documentation omits this spacing.
Don't mistake the em dash for the narrower en dash (–) or the even narrower hyphen (-). Those marks serve different purposes. You can type the em dash character in various ways:
HTML `&mdash;`
macOS: Press Option+Shift+hyphen.

**Examples:**
Upon discovering the errors (all 124 of them), the writer immediately unpublished the page.
Upon discovering the errors—all 124 of them—the writer immediately unpublished the page. (preferred)
After one week of training, the employees were tired of his style (or, rather, his one-way approach).
After one week of training, the employees were tired of his style—or, rather, his one-way approach. (preferred)

## Italics

Use only as an adjective to describe or modify a noun and pronoun, for example:

* The italic message
* The italic word

Use italics formatting, `<i>` or `_`, when drawing attention to a specific word or phrase, such as when defining a term or using words as words. Example:

A _Clos network_ is a kind of multistage circuit switching network, first formalized by Charles Clos in 1952.

Although an asterisk, `*`, can also indicate italics in Markdown, we recommend underscores to make it easier for humans to distinguish italics from bold in the Markdown file.

Italicize parameter names. For example, when you refer to the parameters of a method like doSomething(Uri data, int count), italicize _data,_ and _count_.

Italicize mathematical variables and version variables. For example, _x_ + _y_ = 3, version 1.4._x_.

## Oxford comma

In a series consisting of three or more elements, separate each element with a comma.

**Example:** "Oxford comma: learn it, live it, and love it."

## Quotation marks

* Single or double quotation mark rules and usage differ between the US and the UK or Europe; so, avoid them.
* Instead use **boldface,** _italics,_ `code`, or other formatting to specify a particular phrase or text.

**Examples:**

Press the **Enter** key.

Use the search string `str$`.

Screen readers read **bold** and _italic_ with some emphasis while saying "quote mark" whenever there are quotation marks, so avoid quotation marks as much as possible.

## Parentheses

Because they're so jarring to the reader, avoid parentheses whenever possible. **If removing a parenthetical note changes the meaning of the sentence, it should not be in parentheses**. Place a period outside a closing parenthesis if the material inside isn't a sentence (such as this fragment).

## Slashes

Apart from fractions and code samples, the slash has almost no good uses and should be avoided. It's better to write out the "or" or "and" that it represents. If a slash is used, then a space is placed before it and after it for readability, and the word after the slash uses the same capitalization as the word before the slash.

When you instruct customers to enter a slash, always include the spelled-out term (_backslash_ or _forward slash_) first, followed by the symbol in parentheses.

**Examples:**

Enter two backslashes (`\\`) …
CD / DVD drive
Use the on / off switch to turn your mouse off when you're not using it.
Turn on the On / Off toggle

# Write for a global audience

Many of our customers speak English as a second language. We improve our documentation's readability by using simple words, short sentences, and short paragraphs.

## Write dates correctly

If you can avoid writing dates, do, because they can become a maintenance liability. If you can't avoid writing them, follow these guidelines:

In body text, use "Month Day, Year" – this eliminates any confusion for international users who may format dates differently; don't abbreviate the month's name and don't use an ordinal indicator, for example: Oct 15th.

Follow the year with a comma if using a full date within a sentence.

**Example**: December 3, 2022

Use the `YYYY-MM-DD` date format in your documentation when referring to the date format that appears in code examples.

## Write short sentences

Keep sentences under 20 words if possible. Research shows that people stop retaining your sentence after about 20 words.

Guidelines for keeping your sentences brief and accessible:

* Aim for 12 words or less.
* Don't exceed 35 words.
* One sentence is one idea.

# Write in active voice

In general, write in active voice rather than passive voice.

* **Active voice** identifies the agent of action, usually the user, as the subject of the verb. Active voice clarifies who or what completes an action and is easier to understand than passive voice.
* **Passive voice** identifies the recipient of the action as the subject of the verb. When you use passive voice, the actions and responses of the software are difficult to distinguish from those of the user. Passive voice is usually less engaging and wordier than active voice.

You might choose to use passive voice when:

* You want to de-emphasize the agent of action and emphasize the object
* Active voice sounds like you're blaming the user
* Active voice is wordy or awkward

# Use present simple tense

Users read documentation to complete tasks or gather information. These activities take place in their present, so the present simple tense is appropriate in most cases. Additionally, the present tense is easier to read than the past or future tense.

## Avoid the future tense

Avoid using _will_ where possible—for example:

**Recommended:** Send a query to the service. The server sends an acknowledgment.

**Not recommended:** Send a query to the service. The server will send an acknowledgment.

**As a rare exemption, and only if you need to convey futurity,** use the **present progressive (be + verb + ing)** to write about future events which have already been planned. Time words in the sentence, such as next week, next year, tomorrow, etc., need to make it clear that the action isn't happening in the present. **Example:**

**Correct:** Nium is releasing new APIs in January of 2024.

**Incorrect:** Nium is needing to update its Payment APIs at the end of the year.

# Avoid redundancies

**Don't use current:** It's redundant routinely to use _currently_ with the present tense, just as it's wrong to use _previously_ with the past tense. _We're overbooked_ and _We're currently overbooked_ mean the same thing, just as _We were previously overbooked_ and _We were overbooked_ mean the same. The only point in using the adverb is to emphasize something temporary, for example, _"We're currently overbooked but we expect that to change shortly."_
Beware of redundancy in language. There's no difference in meaning between _"Please keep all your belongings with you"_ and _"Please keep your belongings with you"._ You can spot redundant words by posing the question "As opposed to...?" "Please keep all your belongings with you" as opposed to "Please keep some of your belongings with you"?

# Avoid jargon

Use familiar terms, such as _symbol_ instead of _glyph._ Avoid marketing and promotional jargon, such as using _leverage_ to mean _take advantage._

# Page headings

These guidelines apply to all page headings and table headers:

* Use sentence case, capitalize the first word, and lowercase the rest.
* For tasks, start with an imperative verb
* For concept or reference, start with a noun
* For ordered steps, precede the header with a step number.
* Don't use _the_, _a_, or _an_
* Don't end with a punctuation sign

**Page heading guidelines**

Page headings are equal to H1, or one hash mark # headings. Use sentence case on page headings.

In ReadMe, use two hash marks, for the first heading under the H1 heading, to achieve an H2 heading.

**Heading guidelines**

**When writing headings, concentrate on what developers can achieve or what they need to know.**

Think of headings as an outline, only more interesting. Research shows readers skim documents for headings first, so headings should boil the section down to one idea.

Topic and sub-topic headings are equal to H2, H3, and H4 headings.

Follow these guidelines for writing headings:

| Do | Example |
| --- | --- |
| Focus on what matters to customers. Choose words they'd use themselves. | |
| For a task, start with an imperative verb. | Get API credentials |
| For a concept or reference, start with a noun | Sandbox API URLs |
| For tasks where the order matters, start the heading with a number and a period | Create order |
| Keep headings brief but descriptive. If conflict occurs, prioritize clarity over brevity. | |
| Use parallel sentence structure for all headings at the same level. | Set up payments / Add capabilities / Test and go live |
| Use sentence case | **Exceptions:** Proper nouns, including brand, product, and service names, are always capitalized. If a title or heading includes a colon, capitalize the first word after it. Titles of blog posts, documentation articles, and press releases use sentence-style capitalization. |

**Don't**

* Don't use H5 headings. Rethink the organization of your document instead.
* Avoid having two headings in a row without text in between — that might indicate a problem with organization or that the headings are redundant. But don't insert filler text just to separate the headings.
* Don't end headings with a period or exclamation mark.
* Don't use the, a, or an in headings.
* Don't use -ing verbs in headings.
* Don't repeat words in the heading if the word is already in the page title or parent heading.

  **Don't:**
      Title: Set up your server
          H1: Step 1: Set up your server to create an order
          H1: Step 2: Set up your server to capture an order
  **Do:**
      Title: Set up your server
          H1: 1. Create order
          H1: 2. Capture order

**Figure, table, and image heading guidelines**

In addition to the headings guidelines, follow these guidelines for figures, tables, and image headings:

* Place the heading above the figure, table, or diagram
* Don't number the figure, table, or diagram
* Don't use the word _figure_, _table_, or _diagram_ in the heading

# Formatting

## Lists

Lists are a great way to present complex text in a way that's easy to scan.
A list should have at least two items but no more than seven items. Each item should be fairly short—the reader should be able to see at least two, and preferably three, list items at a glance. It's OK to have a couple of short paragraphs in a list item, but don't exceed that length too often.
Make all the items in a list consistent in structure. For example, each item should be a noun or a phrase that starts with a verb.

* Add bullets for non-ordered lists and at least for two bullet items.
* Add numbers (1, 2, 3, …) for steps or instructions.
* Add letters (A, B, C, …) for items of a list whose order doesn't matter.
* Add periods at the end of each bulleted, numbered, and lettered item if they're complete sentences.
* Add the Oxford comma before the final **and** and the final **or** in a list.

### Bulleted lists

Use a bulleted list for things that have something in common but don't need to appear in a particular order.
**Examples**
The database owner can:

* Create and delete a database.
* Add, delete, or modify a document.
* Add, delete, or modify any information in the database.

Bring your customers into focus

* Own your customer relationship.
* Create raving fans.
* Engage in new ways.

### Numbered lists

Use a numbered list for sequential items (like a procedure) or prioritized items (like a top 10 list).
**Example**
To sign on to a database

1. On the File menu, select Open database.
2. In Username, enter your name.
3. In Password, enter your password, and then select OK.

## Abbreviations

* Avoid **i.e.,** (that is) and **e.g.** Instead use for example or for instance.
* All abbreviations, such as **etc.**, end with a period.
* Abbreviations are spelled out, with the abbreviation in parenthesis, at least once near the top of each page that uses it, except abbreviations that are more common than their meaning, such as _AI_ and _DNA_.

## Tables

Tables help understand difficult information by presenting it in a clear structure. In a table, data is arranged into two or more rows (plus a header row) and two or more columns. Don't use a table just to present a list of items that are similar. Use a list instead.
Tables are sometimes useful for:
Data or values, example: text formats and their associated HTML codes
Simple instructions, example: user interface actions and their associated keyboard shortcuts
Categories of things with examples, example: SKUs and the products they include
Collections of things with two or more attributes, example: event dates with times and locations

### Table content

Make sure the table's purpose is clear. If needed, add a table title or brief introduction.
Place information that identifies the contents of a row in the leftmost column of the table. For example, in a table that describes commands, put the command names in the left column.
Make entries in a table parallel. For example, make all the items within a column a noun or a phrase that starts with a verb.
Don't leave a cell blank or use an em dash to indicate there's no entry for that cell. Instead, use _Not applicable_ or _None._
Keep responsive design in mind. Limit the number of columns and keep the text in each cell brief—ideally one line. If you're writing for the web, assume your content is used on a variety of devices. Many websites today are _responsive_—that is, they reconfigure automatically based on the device in use. Assume your content is viewed at small sizes.
Balance row height by increasing the width of text-heavy columns and reducing the width of columns with minimal text.

### Header rows

If the first row of your table contains column headers, you have a header row. Distinguish the text in the header row from the rest of the text in the table. For example, make it larger, bolder, or a different color.
Column headers identify the data each column contains. Make headers precise for usability. For example, don't use "Name". Instead, make column headers specific as in "Group" or "Employee". (While screen readers use header information to identify rows and columns, specificity helps all users find the information they're looking for.)
Don't organize a table so that the column header forms a complete sentence when combined with the cell contents. This can make the table difficult to localize.
In long tables, make sure the header row is always visible. For example, on the web, use a fixed header row that stays in place during scrolling. Or, in a downloadable document, occasionally repeat the header row. Some authoring tools provide a way to do this automatically. In Microsoft Word, select the header row. On the Layout tab under Table Tools, select Repeat Header Rows.

### Table capitalization

Use sentence-style capitalization for the table title and each column header. Use sentence-style capitalization for the text in cells unless there's a reason not to (for example, keywords that must be lowercase).

### Table punctuation

If there's text that introduces the table, it should be a complete sentence and end with a period, not a colon.
Don't use ellipses at the end of column headers.
For the text in cells, use periods or other end punctuation only if the cells contain complete sentences or a mixture of fragments and sentences.

## Acronyms

* Write out acronyms in first reference, unless they're easily recognizable such as USB, FAQ, URL, etc.
* Don't make up acronyms from product names or product features.
* Add the acronym in parentheses after the written-out term. On subsequent mentions in the same article, page, or screen, use the acronym without writing it out.
* Don't write out the term if the acronym is listed in [_The American Heritage Dictionary_](https://ahdictionary.com/)

  **Examples:**
  - Conversation as a platform (CaaP) has the potential to make booking a flight as easy as sending a text message. Developers are also looking to CaaP to make computing more accessible to users of all abilities.
  - Learn how to connect a USB device to your computer.

* Don't introduce acronyms that are used just once.
* If an acronym appears only once in your content, just write out the term. Don't introduce it in parentheses after the written-out version.
* Be careful with acronyms in titles and headings. If the first mention of an acronym occurs in a heading, you can use the acronym alone and then write it out in the first paragraph that follows the heading.
* Avoid using an acronym for the first time in a title or heading, unless it's a keyword that you need to place in the title or heading for SEO. If the first use of the acronym is in a title or heading, introduce the acronym in parentheses, following the written-out term, in the following body text.
* Lowercase the spelled-out term.
* Lowercase all words in the spelled-out form of an acronym except for proper nouns. The names of many protocols and specifications are considered proper nouns and are capitalized when spelled out.

  **Examples:**
  - infrastructure as a service (IaaS)
  - dynamic-link library (DLL)
  - High-Definition Multimedia Interface (HDMI)

* Use _a_ or _an_ before the acronym depending on its pronunciation.
* Which article (_a_ or _an_) you use depends on whether you pronounce the acronym like a word or pronounce each letter.

  **Examples:**
  - a DLL
  - an ISP
  - a URL
  - a SQL database (pronounced sequel)

* Add _s_ to make an acronym plural.
* Form the plural of an acronym like you would any other noun. If the acronym stands for a singular noun, add a lowercase _s_ to make it plural. If an acronym stands for a plural noun, don't add an _s._

  **Examples:**
  - three APIs
  - 5 URLs

* Avoid the possessive form when using an acronym.
    * Unless an acronym refers to a person or an organization, avoid using the possessive form. Examples: the IDE enhancements, the purpose of the FAQ, the CEO's blog.

## UI Elements

* **Boldface** items
    * Boldface the name of the element the user clicks, for example:
        * Click the **Submit** button.
        * Click the **Type** dropdown to see ...
* _Italicize_ items
    * Italicize the UI element or option inside a dropdown box, for example:
        * In the **Type** dropdown, select _Internal_ and then ...
    * Italicize the name of a page section or dialog, for example:
        * In the _Dashboard Options_ section, select the ...
* Monospace items
    * Characters typed in a field or dropdown box, for example:
        * In the _Search_ box, enter `client`.
    * Code snippets or command prompt actions, for example:
        * `for iCount = 1 to maxCount`
* Underlined items
    * Avoid underlining text except for [hyperlinks](http://www.google.com/).
    * Use _hyperlink_ or _link_ to describe text or a graphic that readers can select to go to another document, to another place within the same document, or to a webpage. Use _hyperlink_ to refer to a UI element labeled _hyperlink_.
      Don't use _hot spot, hot link,_ or _shortcut_ to refer to a link.
      Use _go to_ to describe the process of going to another document, place, or webpage. Don't use _click_ or _click on._
      Use _create_ to describe writing the HTML code that forms the link.
      In content for web designers, it's OK to use _followed link_ to refer to a destination that the reader has already visited. Don't use in content for other audiences.
      **Examples**
      Select the link to go to another webpage.
      On the **Insert** tab, select **Hyperlink** in the **Links** group.
      **See also** [URLs and web addresses](https://learn.microsoft.com/en-us/style-guide/urls-web-addresses), [Describing interactions with UI](https://learn.microsoft.com/en-us/style-guide/procedures-instructions/describing-interactions-with-ui)
* A **text box** is an area where the user can enter text; a **Dialog** (or **Dialog Box**) can contain a text box and other elements, such as clickable buttons.

## Trademarks and brand assets

Protect Nium, Inc.'s trademarks and brand assets. Also, protect other partner names and brand assets in your work. Use the correct trademark symbols in the right place of the trademark name. Use the symbol **consistently**. This is the case regardless of whether you're using TM, SM, or ®. We refer to partner names in our documentation, especially when we work with several vendors in the KYC/KYB part of the corporate onboarding and individual onboarding of customers.

## Colors

* Find the full list of colors that NIUM Marketing approves at https://niumbrand.frontify.com/document/395721#/basics/colors.
    * **User:** brandsite@nium.com
    * **Password:** _(stored in the source Confluence page; omitted here)_
* For all diagrams, try to use only the basic NIUM company colors:

| **Name** | **Hex** | **RGB** |
| --- | --- | --- |
| NIUM blue (teal) | #24BAD6 | 36, 186, 214 |
| Black | #000000 | 0, 0, 0 |
| Mid gray | #494948 | 73, 73, 72 |
| Additional gray | #8F8F8C | 143, 143, 140 |
| Light gray | #F0F0F0 | 240, 240, 240 |
| White | #FFFFFF | 255, 255, 255 |

## Images

* All images need to be outlined with a thin black box.
* Annotations to point out an area need to be a 3pt red rectangle, circle, or oval, and not be hand-drawn.

# Wording

## Word choice

* **Allowlist and Denylist** are used instead of Whitelist and Blacklist.
* **Chapter** is a huge set of sections. Always refer to a particular **section** instead.
* **Drop-down** (always hyphenated) for noun and adjective.
* **Sign in** and **Sign out** are used instead of Log on and Log off.
* **Multiple currencies** or multicurrency: don't hyphenate words that start with the word _multi-_ unless it's necessary to avoid confusion or _multi-_ is followed by a proper noun. Check [_The American Heritage Dictionary_](https://ahdictionary.com/).
* **Payin:** (n.) The Nium product that puts money in an account as a result of making a deposit is a Nium proper product name. **Pay in** (v.), **payin** (n., adj.) Note the hyphenation.
* **Pay in:** (v.) The act of putting money in an account or making a deposit.
* **Pay-in:** (adj.) The adjective used to modify or describe a noun as in "pay-in request."
* **Payout:** (n.) The Nium product that pays out money to a merchant as a result of sales. The payout (n. and not the product name) consistency is determined by the merchant's choice of a payment service provider. It normally takes three to seven days to complete.
* **Pay out:** (v.) The act of distributing or disbursing money.
  **Pay-out:** (adj.) The adjective used to modify or describe a noun as in "pay-out request."
* **Should** implies something might not happen or might not be needed. Always use need instead.
* **Sign in, sign in to** (v.), sign-in (n., adj.) Note the hyphenation. Users _sign in to_ services and applications (not _sign into, sign on to_, or _log in to_).
* **Sign out, sign out of** (v.), **sign-out** (n., adj.) Note the hyphenation. Users _sign out_ of services and applications (not _sign off of_ or _log out of_).

## Voice and second-person pronoun

* In general, use second-person pronouns such as you or you're in a casual business tone that can apply to any audience. In the second person, you write as though you're speaking to your reader. The second person often uses the personal pronoun _you_ or _your_, but sometimes the word _you_ is implied. It supports a friendly, human tone and helps avoid passive voice by focusing the discussion on the reader. Omit _you can_ whenever the sentence works without it.
* Make sure you know who _you_ is - the client's developer, the client's customer, partners, or some combination. **Be consistent**. Don't use _you_ in one part of a document to refer to a developer and _you_ in another part to refer to a seller.

**Examples:**

* Check if you have local admin rights.
* Depending on your choice, some features may be turned off by default.
* Change your settings
* Suggested for you
* Active voice is preferred; use passive voice sparingly when active sounds awkward.
    * **Active voice** identifies the agent of the action, usually the user, as the subject of the verb. Active voice clarifies who or what completes an action and is easier to understand than passive voice.
    * **Passive voice** identifies the recipient of the action as the subject of the verb. When you use passive voice, the actions and responses of the software are difficult to distinguish from those of the user. Passive voice is usually less engaging and wordier than active voice.

    You might choose to use passive voice when:

    * You want to de-emphasize the agent of action and emphasize the object
    * Active voice sounds like you're blaming the user
    * Active voice is wordy or awkward
* Write for a lay person audience. A lay audience doesn't have expert knowledge. A lay audience connects with the human interest aspect of the content. They usually need a little background information; they expect more definition and description; and they may want attractive graphics or visuals.
* Write in a conversational tone.

# Callouts and notices

To make a particular piece of information stand out from your writing flow, **use a callout or a notice.** Use these types of notes sparingly since research shows readers skip these types of elements on a page. If you're not sure whether something should be a callout or a notice, write it first in regular text and then decide if you need one.

Avoid having two callouts and notices in a row. If you feel you need to have two different types of callouts, reorganize your writing. Refer to these research articles for more information.

* https://www.wisconsin.edu/uwsa/digital-communication/2015/04/17/using-callouts-effectively/
* https://www.nngroup.com/articles/tunnel-vision-and-selective-attention/

[ReadMe offers the following types of callouts](https://docs.readme.com/rdmd/docs/callouts):

📓 **Note:** This is an ordinary aside or tip. It gives the reader useful, but not critical information. For details, see [When to use a _note_ notice type](#when-to-use-a-note-notice-type).

Example: "Making too many API calls overloads the system and affects its performance. Rate limits protect against that by curtailing the number of requests that come into your server."

📌 **Important:** This is guidance that the reader needs to know and which has a major effect on them or on something.

⚠️ **Caution:** This tells the reader to proceed carefully.

Example: "Regenerating your API key breaks your connections. Proceed with caution." "Your request isn't finished yet."

⚠️ **Warning:** Stronger than a _caution_ notice; it means "Don't do this" or that this step might be irreversible, such as leading to permanent data loss. If a reader doesn't heed the warning, they can lose money, lose work, or open themselves to a security breach. API and product deprecation notices use this type.

Example: "If using the EU instance of Opsgenie, the URL needs to be `https://api.eu.opsgenie.com` for requests to be successful."

✅ **Success:** Describes a successful action or an error-free status. Used only in interactive or dynamic content; don't use this notice type in ordinary static pages.

Example: "You've successfully registered your client ID."

💁‍♀️ **Tip:** This is task-based information that may save time or future-proof something. If there's a prebuilt or dashboard option, use a tip.

## When to use a _note_ notice type

Create a _note_ when all of the following are true:

* The information you're sharing is _relevant_ but not _necessary_ to what the reader is doing right now. If the reader skips the information, they'll still succeed.
* Interrupting the reader at this point isn't an obstacle to the reader. For example, your _note_ isn't suggesting an alternative that leads the reader down a different path.
* The information isn't part of the flow of what you're writing—it's not just a continuation, a result, or a pointer to additional information.

## When not to use a _note_ notice type

* Don't use _notes_ for cross-references.
* Don't use _notes_ to tell the reader about prerequisites or about steps they should have taken earlier. Information like this should precede the step.
* Don't make a full procedural step into a _note_.
* Don't use _notes_ to provide information that's necessary for the reader to succeed.
* Don't use _notes_ for information that's in flow with the preceding text. For example, don't use a _note_ to state expected results or to include information that simply describes what precedes.

## Deprecation notice

* Include that the API or product is deprecated or when it will be, preferably with a target date (`MMMM YYYY`) but can use "eventually" until there's a target date.
* Provide a link to the latest version and guide.

These are our deprecation notices:

Example of future deprecation:

```
>⚠️ WARNING
 In **December 2023**, this API version will be deprecated and eventually unsupported.
 [Virtual Account Details V2](ref:virtualaccountdetailsv2) is the latest version of this API.
```

NOTE: If the date is unknown, replace "In December 2023," with "Eventually" and remove the 2nd "eventually".

Example of past deprecation:

```
>⚠️ WARNING
 This API version is deprecated and eventually unsupported.
 [Virtual Account Details V2](ref:virtualaccountdetailsv2) is the latest version.
```

# Editing or reviewing

* Delete edit comments after updating the content.

# Anchors

Anchors are named the same as their corresponding heading with the following adjustments:

* Anchor names are all lowercase.
* Region names are replaced by their two-letter code of `au`, `eu`, `hk`, `sg`, `uk`, or `us`.
* Each space is replaced by a hyphen.
* Each non-alphanumeric character is replaced by a single hyphen.
* Conjunctions and prepositions are not included unless part of the API name or status name.
* Do not include appended text that refers to something that may change.

Example 1:

```
<a id="edocverify-eu-uk"></a>
eDocVerify in EU / UK by `Onfido`
```

Example 2:

```
<a id="ekyb-eu-uk"></a>
eKYB in Europe and United Kingdom
```

Example 3:

```
<a id="response-conditions-exhaustive-corporate-details-api"></a>
### Response conditions for the Exhaustive Corporate Details API
```

Example 4:

```
<a id="applicantidentity-request-body-respond-to-rfi-api"></a>
### `applicantIdentity` request body for the Respond to RFI API
```

---

_Source: [Nium Style Guide](https://instarem.atlassian.net/wiki/spaces/CE/pages/3365241081/Nium+Style+Guide) (Confluence, space CE)._
