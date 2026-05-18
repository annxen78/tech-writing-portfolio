# **Wiki Article Style Guide**

[**About This Document**](#about-this-document)

[**Target Audience**](#target-audience)

[**Style and Tone**](#style-and-tone)

[**Wiki Article Structure**](#wiki-article-structure)

[**Formatting**](#formatting)

[**The \[details\] Macro for Long Lists**](#the-details-macro-for-long-lists)

[**Tags and Cross-References**](#tags-and-cross-references)

---

## About This Document

This style guide helps you write wiki articles that are clear, well-structured, and consistent. It is intended for technical writers, editors, and anyone who contributes to internal documentation.

Following this style guide is just as mandatory as following standard rules of grammar and spelling.

---

## Target Audience

Wiki documentation is written for ERP system users with varying levels of experience — from warehouse staff to department managers.

Some users are newcomers who need step-by-step instructions. Others are experienced specialists who need to quickly locate a specific section or setting. Documentation must be useful, accurate, and understandable for everyone.

---

## Style and Tone

1. **Write in plain language** — keep it concise and to the point, without unnecessary detail. Aim for clarity over formality.

2. **Address the user directly** — use "you" in a neutral, respectful way. Avoid overly formal constructions.

3. **Use the imperative mood** — *click*, *open*, *launch*. This form makes instructions easier to follow.

   *Examples:* Click **Save**. Open the Settings menu. Launch the application.

4. **Avoid jargon and informal language:**

   ❌ user (as slang), login (as a verb), log in (in a colloquial sense)
   ✅ user, sign in, sign into the system

5. **Avoid vague abbreviations** like *etc.*, *e.g.* used lazily, or *and so on* — they make text feel incomplete.

   Instead:
   - Write things out in full.
   - Use **"for example"** and list 2–3 specific options.

   ❌ Use filters for searching by categories, tags, etc.
   ✅ Use filters — for example, by category, tag, or date.

6. **Spell out IT abbreviations on first use.** Write the full term followed by the abbreviation in parentheses. After that, you may use the abbreviation alone.

   *Example:* database management system (DBMS).

7. **Avoid modal verbs** like "you need to", "you should", "you must" in instructions.

   ✅ Click the Save button.
   ❌ You need to click the Save button.

   Use modal verbs only when they genuinely affect the meaning:

   *Example:* "You can choose any of the available options."

---

## Wiki Article Structure

### Headings and Table of Contents

- Every heading must clearly reflect the content of its section.
- Use only second- and third-level headings (`##`, `###`).

The first-level heading (`#`) is the name of the section or page itself (e.g., *Knowledge Base*) and is set by the system or entered once manually.

For the article itself, `##` and `###` are sufficient — this keeps the structure clean and the table of contents readable.

Fourth-level headings (`####`) should not be used — they make text harder to navigate. If there is too much content, consider moving it to a separate article.

Heading levels must be nested in order: `#` → `##` → `###`. Do not skip levels.

- Avoid overloading sections with content — break large sections into subsections.
- Headings should be no longer than 7 words (excluding prepositions and conjunctions).

---

### General Structure of an Instruction Article

Write instructions using this structure. This approach helps users understand what is expected of them and complete the task successfully on the first attempt.

1. **Purpose** — explain what the user will accomplish. For example: configuring a warehouse or creating a new order.
2. **Prerequisites** — list what needs to be prepared in advance: access rights, data, configurations.
3. **Step-by-step actions** — format as a numbered list. One step = one action. Start each step with a verb: *Open*, *Select*, *Click*.
4. **Result** — describe what the user should see when done. This helps them verify that everything was completed correctly.

---

### Information Callouts

Use callouts to draw attention to important details. They help users notice key information without cluttering the main text. Choose the right callout type for the context:

1. **Note** — for general important information, clarifications, or reminders.
2. **Warning** — when there is a risk of error, data loss, or other critical consequences.
3. **Tip** — for helpful recommendations or alternative approaches.

---

### Screenshots and Images

1. Place a screenshot immediately after the text it relates to.
2. Do not add captions or numbering.
3. If needed, add a short description before the screenshot.

**Important:** In printed documentation, screenshots must be captioned and formatted accordingly. See the [editorial style guide](https://docs.google.com/document/d/10KBEj2VmhODRS5Gv2ja3RxDfWHCVACoS3mLWJ0HujNU/edit?tab=t.0#heading=h.btju92bxda72) for details.

---

## Formatting

### Bulleted and Numbered Lists

Use **numbered lists** for sequential steps in instructions — when order matters. Use **bulleted lists** for clarifications or sub-items within steps.

1. List items begin with a capital letter.
2. Do not end items with a period or semicolon.
3. If an item contains multiple sentences, use periods.

*Examples of short items:*

- First item
- Second item
- Third item

*Examples of multi-sentence items:*

- The first item turned out to be longer than expected. This will help you understand the difference.
- The second item is also a bit longer. And this will help too.

---

### Bold and Italic

- **Bold** — for button names, field labels, and menu items in the UI.
- *Italic* — for emphasis and clarifications.
- ***Bold italic*** — for file paths, identifiers, and configuration parameters.

*Example:*

Open the file ***C:\Windows\notepad.exe***.

---

### Dashes and Hyphens

A dash is not a hyphen.

**Em dash (—)** is used in sentences for emphasis or logical contrast.
*Example:* She handles the warehouse — I handle shipments.

**Hyphen (-)** connects parts of a word.
*Example:* client-server, well-known, follow-up.

**En dash (–)** is used between numbers.
*Example:* 10–15 items.

In wiki articles, use only the em dash (—) and en dash (–) as appropriate. Do not substitute hyphens.

---

### Quotation Marks

In web and wiki content, **do not use quotation marks**. They clutter the layout and reduce readability. This rule does not apply to printed documentation.

---

## The \[details\] Macro for Long Lists

If an article contains a long list — 10 or more items — use the `[details]` macro so the list can be expanded on click. This saves space and keeps the page uncluttered.

*Markup example:*

| `<details>` `<summary>List of possible statuses</summary>` `- Pending` `- Accepted` `- In transit` `- Delivered` `- Cancelled` `</details>` |
|:---|

---

## Tags and Cross-References

### Using Tags

Tags make articles easier to find via search and help connect related content.

- Use key terms that accurately describe the article's topic: *setup*, *inventory*, *access rights*, *shipment*, etc.
- Include the product name if the article relates to a specific system: *iBOX*, *marketplace*, *HR*.
- Avoid overly generic or rarely used terms.
- Each article should have a minimum of 2 tags and a maximum of 6.

---

### Cross-References

To simplify navigation and avoid repeating content across articles, use cross-references. They allow readers to jump to the relevant section without losing context.

**When to use links:**

- A term or process is mentioned that is described in another article.
- There is an instruction on a related topic.
- You need to point to where a specific setting is configured.

| Link format: *Internal link:* `[See the Returns article](../returns)` *External link:* `[official website](https://...)` |
|:---|

