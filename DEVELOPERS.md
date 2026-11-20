# Cicero Development Guide

## ❗ Accord Project Development Guide ❗
We'd love for you to help develop improvements to Accord Project technology! Please refer to these Accord Project Development guidelines we'd like you to follow.

## Installation

To build the documentation locally:
```
cd ./website
npm install
npm run start
```
If you want to re-generate the JSDoc API:
```
npm run build:api
```

## Creating a new version of the documentation

```
cd ./website
npm install
npm run version `0.23.0`
```
If you want to re-generate the JSDoc API:
```
npm run build:api
```

## Accessibility checks

When changing documentation or a user interface, check the affected pages and
workflows for accessibility before submitting a pull request. Start with the
[W3C accessibility checks](https://www.w3.org/WAI/test-evaluate/easy-checks/).
The checks below cover common barriers; passing them does not establish full
[WCAG 2.1 conformance](https://www.w3.org/TR/WCAG21/).

### Keyboard navigation

1. Open the affected page and use `Tab` and `Shift+Tab` to move through links,
   buttons, and form fields without using a mouse. Check that the focus indicator
   is visible and the order follows the page's reading order.
2. Activate links with `Enter` and buttons with `Enter` or `Space`. Check that
   menus and dialogs can be opened, used, and closed from the keyboard, with
   focus returning to the control that opened them.
3. Follow the page's main workflow, including any editor or form. Check that you
   can leave every control without getting trapped. If a component uses special
   keyboard shortcuts, check that its instructions explain them.

See [WCAG 2.1: Keyboard](https://www.w3.org/WAI/WCAG21/Understanding/keyboard.html).

### Content and visual presentation

* Give headings a logical hierarchy and links meaningful text. Describe the
  purpose of informative images in their alternative text; decorative images
  should have empty alternative text.
* Check that form fields have labels and that required fields and validation
  errors are explained in text, rather than by color alone.
* Measure text contrast in each supported theme. WCAG 2.1's
  [Contrast (Minimum) criterion is Level AA](https://www.w3.org/WAI/WCAG21/Understanding/contrast-minimum.html):
  ordinary text needs a ratio of at least 4.5:1, and large text needs at least
  3:1. Large text means at least 18 point, or 14 point when bold. The criterion
  includes exceptions such as logos and inactive controls.
* Zoom to 200% and check that text and controls remain readable and usable.
  For [reflow](https://www.w3.org/WAI/WCAG21/Understanding/reflow.html), also check
  a viewport 320 CSS pixels wide. Ordinary text should wrap without requiring
  horizontal scrolling; content that needs a two-dimensional layout, such as
  a data table, has an exception.

### Screen reader checks

Use a screen reader such as VoiceOver on macOS or
[NVDA on Windows](https://download.nvaccess.org/documentation/userGuide.html).
Learn its navigation commands before testing; moving between headings and
reading text is different from tabbing between interactive controls.

1. Navigate by headings and landmarks. Check that the page title, structure,
   and main content are understandable without seeing the page.
2. Move to each changed control and check that its name, role, and state are
   announced. For example, a menu button should expose whether it is expanded.
3. Complete the affected workflow. Check that field labels, instructions,
   validation errors, and relevant status updates are available to the screen
   reader, including after content changes.

### Report the results

In your pull request, record the pages or workflows checked, browser and
operating system, and screen reader and version if used. Describe the steps and
observed results for any problems, and identify checks you did not run or that
do not apply. Automated checks can supplement this review, but cannot replace
manual keyboard and screen reader testing.

## Commits
When committing your changes, it is required you adhere to the [commit message conventions]. This is important because the release notes are automatically generated from these messages.

[commit message conventions]: https://www.conventionalcommits.org/en/v1.0.0/
