# fix margin usage

This CSS file attempts to solve two issues with the usage of margin in browser styles.

1\. Instead of using vertical padding for text-based elements browsers use vertical margin. this is not what margin was designed for. It, therefore, raises other layout issues:

- Background and borders go directly up against the text instead of going around its whitespace.

- While not an actual issue. This often creates [collapsing margins](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Mastering_margin_collapsing), which is quite complex and can lead to other layout issues.
  
Some uses of margin seem reasonable including `dd` and `fieldset`.

`dd` stands out in that the margin is only on the left and is just used for indentation.

`fieldset` stands out in that it also has padding. This one was probably done correctly because it has a default border making it visually obvious if margin was used in place of padding.

2\. Instead of adding sensible horizontal padding to text elements (eg: p, h1, blockquote) browsers add 8 pixels of margin to the body. This causes all non-text-based elements (eg: images) to also have 8px of whitespace on its sides and the body background to not reach the edges of the viewport.

---

This is based off The list of defaults from [w3schools.com/cssref/css_default_values.asp](https://www.w3schools.com/cssref/css_default_values.asp).
