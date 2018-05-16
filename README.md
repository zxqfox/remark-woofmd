# Woof MD

## Usage

```js
const remark = require('remark');
const { vis, remark: remarkWoofmd } = require('.');
const processor = remark().use(remarkWoofmd);
const go = s => vis(processor.parse(s));

go(`
# Best addon for your pluphone

Perfecto is real!

Text Before formatter block.
%%(prettify align=center)
Text inside
formatter with //emphasis// and **bold**.
%%
Text just after the formatter block.

<{ Big quote block here

## With headings

}>


<{ Cut string **Bold here** and !!(green) Apple text !! too.
    🍏🍎🍏🍎🍏🍎🍏🍏🍏🍏🍏🍒🍏🍒🍏🍒.

    Yep.
}>

##+Rolled section

This part is hidden for the first look

## Usual heading

Hey boys, it's the end!
`);
```
