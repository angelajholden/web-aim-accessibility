# Web Aim Accessibility

## Jan 27, 2021

### WCAG 2

WCAG is the foundation of all accessibility laws worldwide

### Principles based

-   perceivable
-   operable
-   understandable
-   robust

### Resources

-   https://www.w3.org
-   https://www.w3.org/WAI
-   https://www.w3.org/WAI/WCAG21/quickref

The ADA does not refer to websites or web accessibility. Case law says that websites are public/commercial space and subject to being accessible and compliant with the ADA.

### Assistive technology

Can be as straight forward as needing...

-   eye glasses
-   contact lenses

### Low Vision

adjacent colors apply to anything that conveys meaning

### Best Practices

-   add a borders for adjacent contrast
-   all links need to be underlined on hover and focus
-   link contrast is not the same as text contrast
-   not all screen reader users are blind, but rather have low vision
-   One H1 per page
-   H1 can come after and H2
-   Ok to skip headings backwards
-   no WCAG recommendation for opening links in a new window
-   page <title> is first thing read by a screen reader; should match the H1

### Rules for ARIA

-   use HTML regions before using ARIA roles
-   screen readers don't distinguish between ARIA roles and HTML
-   role="" is ARIA
-   Region/Landmark are the same thing

### Forms

-   explicit vs implicit form labels
-   implicit wraps the label around the input
-   screen readers don't care as long as they're linked properly
-   use fieldset and legend to group radio buttons and checkboxes

### Tables

-   spancol="" is not a best practice; reads it every time
-   use <caption> tags
-   do not put headers in the middle of the table; screen readers read all of those headers
-   use multiple tables to avoid multiple headers
-   think "semantic structure"
-   role="presentation" for HTML emails; even though it probably doesn't matter
-   data tables must support complex images/graphs conveying data

### Disabilities

-   cognitive/learning is the largest disability group
-   use the 'prefers-reduced-motion', but does not fulfill the WCAG requirement

### CSS

-   avoid a fixed height; instead use min-height
-   tannerhodges@hey.com for an alternative to flex-box columns
-   44px x 44px is AAA clickable standard for WCAG; this doesn't always work

### ARIA & HTML

-   use HTML before you use ARIA
-   ARIA only does what HTML cannot do
-   don't change native semantics unless you have to
-   title="" attribute may or may not be read to the user
-   placeholder="" attribute is read by screen readers but not a suitable replacement for <label>
-   don't rely on placeholders to tell the user what is needed; placeholder disappears as soon as user starts typing
-   stick with the traditional <label>; don't be cute
-   ARIA labels override default HTML/accessible labels and text; don't double up or be redundant
-   <div> <span> <p>, etc. cannot have an accessible name/ARIA label; screen reader will skip
-   <button> can take an ARIA label/accessible name
-   see the screen shots for guidance on SVGs; not ok to use aria-hidden="true"; use alt="" to explicitly say it's decorative
-   aria-describedby="" will override display: none;
