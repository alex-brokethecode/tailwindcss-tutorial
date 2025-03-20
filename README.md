# Tailwind CSS Tutorial

## Overview

This tutorial covers essential Tailwind CSS utilities demonstrated in an example project. Tailwind is a utility-first CSS framework that helps build modern, responsive designs quickly.

---

## Project Setup

- Create your Vite project. Follow the [documentation](https://vite.dev/guide)

```bash
npm create vite@latest
cd project_name/
npm i
npm run dev
```

- Install TailwindCSS for Vite. Follow the [documentation](https://tailwindcss.com/docs/installation/using-vite)

- Can install the `Tailwind CSS IntelliSense` plugin
- Can use this [cheatsheet](https://www.creative-tim.com/twcomponents/cheatsheet) to have a references of classes

---

## Styling Utilities

### Breakpoints

Tailwind provides responsive utilities:

```html
<body
  class="sm:bg-amber-300 md:bg-green-300 lg:bg-red-300 xl:bg-gray-300"
></body>
```

- `sm:` → Small screens
- `md:` → Medium screens
- `lg:` → Large screens
- `xl:` → Extra-large screens

### Text & Buttons

```html
<h1 class="bg-blue-500 text-2xl text-center text-white">Hello World!</h1>
```

- `bg-blue-500` → Background color
- `text-2xl` → Font size
- `text-center` → Center-align text
- `text-white` → White text color

Button example:

```html
<button class="bg-green-500 hover:bg-green-600 text-white p-2 rounded-xl">
  Submit
</button>
```

- `hover:bg-green-600` → Change background on hover
- `p-2` → Padding
- `rounded-xl` → Rounded corners

### Gradient Text

```html
<span
  class="bg-clip-text text-transparent bg-gradient-to-r from-pink-500 to-violet-500"
  >TailwindCSS</span
>
```

- `bg-clip-text` → Clip background to text
- `text-transparent` → Transparent text color
- `bg-gradient-to-r` → Gradient from left to right

---

## Sizing

```html
<div class="bg-yellow-500 w-1/2 h-[50px]">
  <p class="w-40 bg-red-600 h-full">This is a paragraph</p>
</div>
```

- `w-1/2` → 50% width
- `h-[50px]` → Custom height
- `w-40` → Fixed width
- `h-full` → Full height of parent

---

## State & Form Utilities

```html
<input class="disabled:bg-gray-500 disabled:text-white" disabled />
```

- `disabled:bg-gray-500` → Background changes when disabled
- `disabled:text-white` → Text color when disabled

```html
<input class="invalid:focus:border-red-700 peer" />
<p class="text-red-400 hidden peer-invalid:block">Invalid email</p>
```

- `peer` → Connects elements together
- `peer-invalid:block` → Show message on invalid input

---

## Pseudo-classes

```html
<p class="selection:bg-blue-400 selection:text-white">Selected text styles</p>
```

- `selection:bg-blue-400` → Background when selecting text
- `selection:text-white` → Text color when selecting

```html
<p class="first-line:uppercase first-letter:text-7xl first-letter:font-bold">
  Text styles
</p>
```

- `first-line:uppercase` → Uppercase first line
- `first-letter:text-7xl` → Large first letter

---

## Flexbox Utilities

```html
<div class="flex gap-3 p-5 h-50 flex-wrap">
  <div class="grow shrink-0 basis-1/4">1</div>
</div>
```

- `flex` → Enables flexbox
- `gap-3` → Spacing between elements
- `grow` → Allow item to grow
- `shrink-0` → Prevent shrinking
- `basis-1/4` → Base size of 25%

---

## Grid Utilities

```html
<div class="grid grid-cols-2 grid-rows-4 gap-4">
  <div class="col-span-2">Header</div>
  <div class="row-[2/4] col-start-1">Main</div>
</div>
```

- `grid` → Enables grid layout
- `grid-cols-2` → Two columns
- `grid-rows-4` → Four rows
- `col-span-2` → Spans two columns
- `row-[2/4]` → Custom row placement

## Apply

Create custom classes to re-use Tailwind CSS classes

```css
.square {
  @apply bg-blue-400 w-10 h-10 flex justify-center items-center;
}
```

```html
<div class="square"></div>
```
