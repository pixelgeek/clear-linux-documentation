.. _grammar:

Grammar guide
#############

This guide provides valuable insight into the correct grammar for the
|CLOSIA| documentation. It covers subjects such as capitalization, verbs,
hyphenation, possessives, and contractions.

Capitalization
**************

The preferred capitalization style for all documentation is sentence
case.

Words should only be capitalized when:

* They are proper nouns or adjectives.
* They refer to trademarked product names.

.. note::
   Do not capitalize a word to indicate it has a greater status than other
   words. Never change the case of variable, function or file names; always
   keep the original case.

Menu capitalization
===================

When referring to software menu items by name, replicate the
capitalization as it appears in the software menus the user will see.
It is acceptable to refer to these items generically by using
lowercase letters if it is clear that your reference is generic and
not a specific name of a window or field on a menu, for example:

Click :guilabel:`Edit` to display the :guilabel:`Widget Configuration` window.

The widget configuration window has several advanced widget configuration
options.

The second sentence could have capitalized the term "Widget
Configuration window"; but there are times when you might want to
refer to something with a generic descriptor and not its name. Observe
the use of the ReST markup ``:guilabel:`` on the first sentence.

A few other menu capitalization rules to keep in mind:

* Use "Select :menuselection:`File --> New`."

* Put the option to be selected last. "Select
  :menuselection:`View --> Side Bar --> Hide Side Bar`"

* Do not include more than 3 navigation steps in a menu selection. If
  more than three steps are needed divide the steps using
  ``:guilabel:`` or ``:menuselection:``. For example: "Go to
  :guilabel:`File` and select
  :menuselection:`Print --> Print Preview --> Set Up`."

Software version capitalization
===============================

Do not capitalize the word version or letter v when listing software
or hardware version numbers. The v is lowercase and closed with the
number (no period). For example:

* Widget Pro v5.0
* Widget Master v2.1.12

Hyphenated or slashed-concatenated terms
========================================

For hyphenated or slash-concatenated terms, capitalize only the first
letter, even if they are headings. For example:

* Day/night Menu
* Follow-up Action Items

Plurals and possessives
***********************

Because English plurals and possessives use the same /s/ and /z/
phonemes, they can create problems for even experienced writers. This
section deals with these issues.

Singular vs. plural possessives
===============================

Here are some guidelines for singular and plural possessives:

* Use only the apostrophe to show possession for a plural that ends in
  s: The boys' books.

* Use apostrophe + s to show possession for a plural that does not end
  in s: The men's books.

* Use apostrophe + s to show possession for a singular that ends in a
  silent sibilant: Illinois's capital.

* Use apostrophe + s to show
  possession for a singular that ends in a sibilant; s, x, c, z, or
  others.

The following table provides some examples with the correct and
incorrect cases and the notes that accompanies them.

+-------------------+------------------+---------------------------+
| Correct           | Incorrect        | Notes                     |
+===================+==================+===========================+
| the boys' books   | the boy's books  | The books that belong to  |
|                   |                  | several boys.             |
+-------------------+------------------+---------------------------+
| the men's books   | the mens' books  | The books that belong to  |
|                   |                  | several men.              |
|                   |                  |                           |
+-------------------+------------------+---------------------------+
| Arkansas's code   | Arkansas' code   | The s at the end of       |
|                   |                  | Arkansas is silent and    |
|                   |                  | Arkansas is not a plural. |
+-------------------+------------------+---------------------------+
| the boss's office | the boss' office | We say: "the /BOSS-iz/    |
|                   |                  | office" not "the/BOSS/    |
|                   |                  | office."                  |
+-------------------+------------------+---------------------------+
| the box's lid     | the boxe's lid   | One could say "the box    |
|                   | the box' lid     | lid," avoiding the        |
|                   |                  | possessive.               |
+-------------------+------------------+---------------------------+
| Lopez's average   | Lopez' average   | We say "/LO-pez-iz/       |
|                   |                  | average," not "/LO-pez/   |
|                   |                  | average."                 |
+-------------------+------------------+---------------------------+
| business's sales  | business' sales  | If you pronounce another  |
|                   |                  | syllable to show          |
|                   |                  | possession, it must have  |
|                   |                  | the apostrophe-s.         |
+-------------------+------------------+---------------------------+

Apostrophe-s anomalies
======================

If a company name ends in s, x, c, or a sibilant sound, use the
apostrophe-s ending for
possessives:

Traktronix's oscilloscopes

Exception: If the company name is intended as a plural, we allow the
apostrophe-only ending:

Tejada Instruments' calculators

In many cases, it is actually best to avoid the possessive form
altogether for s-ending singular possessives, such as for company
names and use the company name as a nonpossessive modifier instead:

Traktronix oscilloscopes
Tejada Instruments calculators

We say "Intel equipment" when discussing Intel-branded products, not
"Intel's equipment", which implies that we own it, not that we produce
it. "Intel's equipment" sounds like the equipment that Intel employees
use.

Plural modifiers
================

Avoid plural modifiers. For example, it should be a system
administrator, not a systems administrator. It doesn't matter how many
systems this person manages, we don't typically use the plural of a word
to modify a noun. Here is a list of exceptions:

* operations manager
* sales department
* graphics team


There are always exceptions, especially when the plural form is
generally considered to be singular: sales, physics, operations. It is
best to adhere to this rule and ask if you are unsure.

Parenthetical plurals
=====================

Do not parenthesize optional plurals, whether added to the end of a
word, typically with the letter s, or internally. In general, think in
plurals when you write, assume that the user understands that a plural
could mean a singular as well. A typical user who has only one unit
will not be confused if you say "connect the units." On the contrary,
using parenthetical plurals often creates more confusion.

Correct

Men, women, children, college alumni, moose,
and even desert plants such as cacti should not
use parentheses around plurals.

Incorrect

A m(e)n, wom(a)n, a child(ren), college alumn(i), (moose), and
even a desert plant(s) such as a cact(i) should not use a
parenthes(e)s around a plural(s).

Internal plural acronyms
========================

Some abbreviated terms can cause trouble, particularly when the
pluralized portion does not fall at the end of the phrase. These
internal-plural words should follow standard English pluralization
rules when abbreviated: The plural goes at the end of the term.

* Alarms acknowledged and logged: AAL, AALs.
* Attorneys-general: AG, AGs.
* Regions of interest: ROI, ROIs.

Plurals of acronyms and capitalized product names
=================================================

Pluralize acronyms, initialisms, and capitalized product names by
adding a lowercase s; do not use an apostrophe. If the term ends in a
sibilant (s, x, z, sometimes c and others), pluralize it by adding a
lowercase es. Examples:

Use TVs, DVDs, CDs, DVMRs not TV's, DVD's, CD's, DVMR's.
Use OSes not OSs, OS's.
Use TRAXes, iBOXes not TRAXs, TRAX's, iBOX's, iBOXs.
Use FAACes not FAAC's, assuming it is pronounced "face".
Use FAACs not FAAC's Assuming it is pronounced "fake".

Whenever you hear the extra syllable in the plural, add the -es suffix
for the plural; if you do not hear the extra syllable, add the -s
suffix for the plural.

Latin plurals
=============

Pluralize Latin terms in body text as shown:

* Use appendixes not appendices.
* Use matrixes not matrices.
* Use indexes not indices.
* Use vertexes not vertices.

.. note::
   Some Latin plurals, such as parentheses, phenomena, alumni, and
   crises, are widely used and accepted in English.

Contractions
************

Avoid the use of contractions since some of them might be ambiguous and
confusing to non-native English-speaking audiences.

Some contractions can cause confusion for non-native English-speakers
because these contractions stand for more than one construction. For
example, there's can be a contraction of there is or there has. The
same applies to where's, it's, that's, and others.

Also, avoid contractions of the word is, especially when combined with
company or product names: Say, WidgetPro is an awesome product; not
WidgetPro's an awesome product.

Hyphenation
***********

The hyphen is often used to join words together to form a compound noun.
Compound nouns often go through this progressions:

* open compound: health care
* hyphenated compound: health-care
* closed compound: healthcare

The English language is trending away from hyphenated compounds to
closed compounds.

Prefix hyphenation
==================

Do not hyphenate the prefixes listed below. Join the prefix to the
term being modified, even if this results in a double vowel or double
consonant:

ante, counter, intra, mini, pro, super, anti, extra, meta, non,
pseudo, trans, bi, by, infra, micro, post, re, ultra, bio, inter, mid,
pre, sub, un.

Here are some words that are often inappropriately hyphenated; do not
hyphenate these words either:

antitheft device, multicamera, multiscreen, prepackaged, reuse,
submenu, autofocus, multifamily, multiuser, pseudoscience, semiannual,
subtotal, autoiris, multimedia, nonprofit, reengineered, semicircle,
superuser, microarchitecture, multiposition, predefined, reevaluate,
subfolder, superscript, microorganism, multiprotocol, predrilled,
reinvent, submarine.

.. note::
   Question whether the pre- prefix is needed at all and consider
   leaving it off the word entirely if the meaning is the same.

Exceptions
----------

One overriding exception to the prefix rule is when the prefix is
prepended to a proper and capitalized noun:

* Non-European
* Mid-April (but: midweek)

Another exception is when the second word of a compound is a numeral:

* Pre-1914

Some prefixes, such as self-, half-, quasi-, and ex-, when meaning
"formerly", usually need a hyphen:

* Self-control, half-truth, quasi-corporation, ex-governor

Suffix hyphenation
==================

In general, do not hyphenate suffixes. Here are some examples.
The suffix -wide is usually not hyphenated:

* Nationwide, worldwide, systemwide, campuswide, statewide,
  companywide, etc.

The suffix -wise is usually not hyphenated:

* Otherwise, businesswise, revenuewise, clockwise, counterclockwise


Quotation marks
***************

Follow these guidelines for quotation marks:

* Restrict use of quotation marks to terms as terms.
* Do not use quotation marks for emphasis; use *italics* for emphasis.
* Avoid using single-quote marks.
* In terms of punctuation: commas and periods typically go inside the
  end-quote; semicolons, colons, question marks, and exclamation points
  typically go outside quotation marks. Unless they are part of the
  actual quotation.