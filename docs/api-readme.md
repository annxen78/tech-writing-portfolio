# Style Guide for README and REST API Documentation

## Table of Contents

- [1. About This Document](#1-about-this-document)
- [2. General Conventions](#2-general-conventions)
- [3. README Style Guide](#3-readme-style-guide)
  - [3.1. Purpose and Audience](#31-purpose-and-audience)
  - [3.2. Required Structure](#32-required-structure)
  - [3.3. Writing Style](#33-writing-style)
  - [3.4. Code Formatting](#34-code-formatting)
  - [3.5. Badges and Shields](#35-badges-and-shields)
- [4. REST API Documentation Style Guide](#4-rest-api-documentation-style-guide)
  - [4.1. Purpose and Audience](#41-purpose-and-audience)
  - [4.2. Required Structure](#42-required-structure)
  - [4.3. Endpoint Descriptions](#43-endpoint-descriptions)
  - [4.4. Parameters](#44-parameters)
  - [4.5. Request and Response Examples](#45-request-and-response-examples)
  - [4.6. Error Codes](#46-error-codes)
- [5. Text Formatting Rules](#5-text-formatting-rules)
- [6. Screenshots and Images](#6-screenshots-and-images)

---

## 1. About This Document

This style guide defines writing and formatting standards for two types of developer-facing documentation: **README files** and **REST API references**.

Following these rules ensures documentation is consistent, scannable, and useful — whether a reader is evaluating a project for the first time or integrating an API endpoint.

This guide applies to all documentation written in Markdown.

---

## 2. General Conventions

- Use American English spelling throughout (e.g., *authorization*, not *authorisation*).
- Write in plain language. Prefer short sentences and active voice.
- Address the reader directly using "you". Use the imperative mood for instructions: *Run the command*, *Set the value*, *Open the file*.
- Introduce abbreviations and acronyms on first use: write the full term followed by the abbreviation in parentheses. Use the abbreviation alone after that.

  Example: A JSON Web Token (JWT) is used for authentication. Include the JWT in the `Authorization` header.

- Do not use the same term and a synonym interchangeably for the same concept. Pick one term and use it consistently throughout the document.
- Limit heading depth to three levels (`#`, `##`, `###`). If you need a fourth level, restructure the content or split it into a separate document.
- Number all sections. Use the format `1.`, `1.1.`, `1.1.1.`

---

## 3. README Style Guide

### 3.1. Purpose and Audience

A README is the entry point to a project. It answers four questions a new reader will have immediately:

1. What does this project do?
2. How do I get it running?
3. How do I use it?
4. How do I contribute or get help?

The primary audience is developers: engineers evaluating the project, contributors setting it up, and integrators looking for quick usage examples.

### 3.2. Required Structure

Every README must include the following sections, in this order:

| Section | Purpose |
|---|---|
| Project title and one-line description | Identifies the project at a glance |
| Badges *(optional)* | Shows build status, version, license |
| Overview | Explains what the project does and why it exists |
| Prerequisites | Lists everything needed before installation |
| Installation | Step-by-step setup instructions |
| Usage | Basic usage examples with real commands or code |
| Configuration *(if applicable)* | Documents available settings and environment variables |
| Contributing | Explains how to report issues and submit changes |
| License | States the license |

Do not add sections that duplicate information found elsewhere (e.g., a full API reference inside a README). Link to a separate document instead.

### 3.3. Writing Style

- Keep the Overview to 3–5 sentences. State what the project does, who it is for, and what problem it solves.
- In the Prerequisites section, list exact version requirements where relevant.

  Example: Node.js 18 or later, npm 9 or later.

- In the Installation section, write one action per step. Use a numbered list.
- In the Usage section, show the simplest possible working example first. Add more complex examples after.
- Avoid marketing language. Describe what the project does, not how great it is.

  ❌ A blazing-fast, developer-friendly framework for building modern APIs.  
  ✅ A Node.js framework for building REST APIs. It includes built-in request validation and OpenAPI export.

### 3.4. Code Formatting

Use fenced code blocks for all code, commands, and file contents. Always specify the language for syntax highlighting.

**Inline code** — use backticks for all of the following:
- File and directory names: `config.yaml`, `/etc/app/`
- Command names: `npm install`, `git clone`
- Parameter names and values: `--port`, `true`
- Environment variable names: `DATABASE_URL`

**Code blocks** — use triple backticks with a language identifier:

````markdown
```bash
npm install
npm run start
```
````

````markdown
```json
{
  "port": 3000,
  "debug": false
}
```
````

If a code block contains a command the reader should copy and run without modification, do not add a prompt symbol (`$`) unless it is necessary to distinguish between input and output in the same block.

For configuration file fragments, include comments inside the block using the syntax of the relevant language. Do not explain configuration options in prose outside the block if they can be explained with an inline comment.

```yaml
server:
  port: 3000        # The port the server listens on
  debug: false      # Set to true to enable verbose logging
```

### 3.5. Badges and Shields

- Place badges immediately after the project title, before the Overview section.
- Use only badges that reflect real, current information: build status, test coverage, version, license.
- Do not use decorative badges that add no information.
- Align badges on a single line. Do not stack them vertically.

---

## 4. REST API Documentation Style Guide

### 4.1. Purpose and Audience

API documentation describes how to interact with an API programmatically. The audience is developers writing code that calls your API. They need to know: what endpoints exist, what each endpoint does, what inputs it accepts, and what outputs it returns.

### 4.2. Required Structure

Every REST API reference must include:

1. **Authentication** — how to obtain and use credentials.
2. **Base URL** — the root URL for all requests.
3. **Versioning** — how the API version is specified (URL path, header, or query parameter).
4. **Rate limiting** — request limits and the headers used to communicate them.
5. **Errors** — the standard error response format and a table of error codes.
6. **Endpoints** — one section per resource, each listing all operations on that resource.

### 4.3. Endpoint Descriptions

Each endpoint entry must include:

- A one-line summary of what the endpoint does.
- The HTTP method and path.
- A description (2–5 sentences) explaining the behavior, any side effects, and important constraints.
- Prerequisites or required permissions, if any.
- Parameters table (see [4.4. Parameters](#44-parameters)).
- Request example (see [4.5. Request and Response Examples](#45-request-and-response-examples)).
- Response example.
- Error codes specific to this endpoint (in addition to global errors).

Format the method and path as inline code. Use uppercase for the HTTP method.

Example:

---

**`POST /users`**

Creates a new user account. The email address must be unique across the system. A confirmation email is sent to the provided address after successful creation.

**Required permission:** `admin`

---

Write endpoint summaries in the third person, present tense.

✅ Returns a paginated list of orders.  
❌ This endpoint will return a paginated list of orders.

### 4.4. Parameters

Document all parameters in a table. Use separate tables for path parameters, query parameters, headers, and request body fields.

**Column order:** Name — Type — Required — Default — Description.

| Name | Type | Required | Default | Description |
|---|---|---|---|---|
| `user_id` | string | Yes | — | The unique identifier of the user. |
| `page` | integer | No | `1` | The page number to return. Must be greater than 0. |
| `per_page` | integer | No | `20` | The number of results per page. Maximum: `100`. |

Formatting rules for parameter tables:

- Write parameter names in backticks.
- Write types in lowercase: `string`, `integer`, `boolean`, `array`, `object`.
- For required parameters, write **Yes**. For optional, write No.
- If a parameter has no default value, write a dash (—) in the Default column.
- Include valid values or constraints in the Description column, not in a separate column.

### 4.5. Request and Response Examples

Include at least one complete request example and one response example per endpoint.

Use `json` as the language identifier for all JSON blocks. Show realistic but fictional data — not placeholder text like `string` or `your_value_here`.

**Request example:**

```http
POST /users HTTP/1.1
Host: api.example.com
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.example
Content-Type: application/json

{
  "email": "alex.morgan@example.com",
  "name": "Alex Morgan",
  "role": "viewer"
}
```

**Response example:**

```json
{
  "id": "usr_01j4k8m2n3p5q7r9",
  "email": "alex.morgan@example.com",
  "name": "Alex Morgan",
  "role": "viewer",
  "created_at": "2024-09-15T10:32:00Z"
}
```

If an endpoint has multiple meaningful response scenarios (success, partial success, empty result), show an example for each.

Do not show examples of invalid requests in the main endpoint description. Document error cases in the error codes table.

### 4.6. Error Codes

Define a global error response structure at the top of the documentation. Every error response must follow this structure.

```json
{
  "error": {
    "code": "RESOURCE_NOT_FOUND",
    "message": "The requested user does not exist.",
    "request_id": "req_7f3b2c1d"
  }
}
```

Document all error codes in a table. Use a global table for common errors, and a per-endpoint table for errors specific to that operation.

| HTTP Status | Error Code | Description |
|---|---|---|
| `400` | `VALIDATION_ERROR` | The request body is missing a required field or contains an invalid value. |
| `401` | `UNAUTHORIZED` | The request does not include a valid authentication token. |
| `403` | `FORBIDDEN` | The authenticated user does not have permission to perform this action. |
| `404` | `RESOURCE_NOT_FOUND` | The requested resource does not exist. |
| `409` | `CONFLICT` | The request conflicts with the current state of the resource (e.g., duplicate email). |
| `429` | `RATE_LIMIT_EXCEEDED` | The client has sent too many requests. See the `Retry-After` header. |
| `500` | `INTERNAL_ERROR` | An unexpected error occurred. Include the `request_id` when reporting this error. |

---

## 5. Text Formatting Rules

Use formatting consistently. The table below defines what each style is used for.

| Element | Formatting | Example |
|---|---|---|
| UI button names | **Bold** | Click **Save**. |
| UI navigation paths | *Italic*, with `→` between steps | Go to *Settings → Integrations*. |
| Form field names, checkbox labels | Regular text, in double quotes | Fill in the "Username" field. |
| Parameter names, file names, commands, values | `Inline code` | Set `debug` to `true`. |
| File paths and system identifiers | `Inline code` | Open `C:\Windows\notepad.exe`. |
| New terms on first use | *Italic* | The *idempotency key* ensures that retrying a request does not create duplicate records. |
| Code blocks and command-line examples | Fenced code block with language | See [3.4. Code Formatting](#34-code-formatting). |

**Callout types**

Use callouts to highlight information that requires special attention. Do not use callouts for general information that belongs in the main text.

> **Note:** Additional context that helps the reader but is not critical to completing the task.

> **Tip:** A recommended approach or a useful shortcut.

> **Warning:** Information the reader must not overlook. Use for actions that are irreversible or that may cause data loss.

---

## 6. Screenshots and Images

- Place a screenshot immediately after the text it illustrates.
- Crop screenshots to show only the relevant part of the interface. Remove personal data, internal URLs, and test credentials before publishing.
- Every screenshot must have a caption.
  - The caption starts with the word *Figure*, followed by the figure number (sequential, document-wide).
  - Do not put a period after the figure number or at the end of the caption.
  - Center-align the caption below the image.

  Example: *Figure 3 Application settings*

- In the main text, refer to a figure by its number in parentheses.

  Example: Open the application settings (Figure 3).

- Do not use screenshots to show information that can be expressed clearly in text or a code block. A screenshot of a JSON response adds less value than a properly formatted code block.
