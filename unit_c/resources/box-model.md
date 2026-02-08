# The Box Model

Principles and actionable concepts extracted from Shift Nudge lesson notes.

---

## Core Principle

**See every piece of interface as a box** — with a left edge, right edge, top edge, and bottom edge. Every single thing.

This applies to:
- Every string of text
- Every container that holds multiple elements
- Every image (round or not)
- Every single piece of interface

This mental model is non-negotiable. It makes your life as a designer significantly easier by providing a consistent framework for thinking about layout and spacing.

---

## The Four Properties

The box model consists of four main properties (from inside to outside):

1. **Content** — The actual element (text, image, etc.)
2. **Padding** — Built-in spacing inside the box, between content and border
3. **Border** — The edge of the box (visible or invisible)
4. **Margin** — Distance between the box and other objects or screen edges

---

## Actionable Concepts

### Visualizing Boxes
- Developers use a `.debug` class with `border: 1px solid red` to visualize element bounds when troubleshooting layout issues
- You can mentally (or literally) enable borders on all elements to see the bounds of every element

### Creating Clean Layouts
- Applying box-model thinking to every element you design produces clean and structured layouts
- Be intentional about the margin and padding of every element

### Margin vs. Padding Decision Rules

**When content background differs from main background:**
- Margin and padding should be roughly equal to each other

**When content background matches main background:**
- You can use 0px margin and put all spacing in padding
- Example: Instead of 12px margin + 12px padding, use 0px margin + 24px padding for the same visual result

---

## Key Takeaway

The total spacing from content to screen edge is calculated: margin + padding = total distance. Understanding this relationship gives you flexibility in how you achieve your desired spacing, depending on whether backgrounds are visible or not.

---

*Source: Shift Nudge UI Design Course — Box Model lesson*
