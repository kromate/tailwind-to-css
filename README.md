# tailwind-to-css

### Intro
generate vanilla css styles from your html tailwind classes

### Install

```bash
npm  i tailwind-to-css
yarn add tailwind-to-css
```

### Usage

```js
import {createStyle} from 'tailwind-to-css'

// Input
createStyle(`
<div class="p-2 text-4xl font-bold">
        Hello World
<span class="underline text-orange-500">Yess</span>
</div>`,
     false).then((data) =>
{
    console.log(data);
})

// Output
// console --> '<style>.p-2{padding:0.5rem}.text-4xl{font-size:2.25rem;line-height:2.5rem}.font-bold{font-weight:700}.text-orange-500{--tw-text-opacity:1;color:rgb(249 115 22 / var(--tw-text-opacity))}.underline{-webkit-text-decoration-line:underline;text-decoration-line:underline}</style>'
```

### Options
The <b>createStyle</b> function takes in two parameters
```js
createStyle(HTML_STRING, withDefault)
```

| Syntax      | Description | 
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |