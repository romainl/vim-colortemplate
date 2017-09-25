# Vim Colorscheme Template

This is a proposal for an “official” colorscheme template that might be used to
create colorschemes suitable for inclusion in Vim distribution.

See also [this discussion](https://github.com/vim/vim/issues/1665).

## Requirements

These are the requirements that a modern colorscheme should satisfy:

- support 256 colors and true color terminals, and GUI Vim.
- Support transparent backgrounds.
- Be minimal: no options, no documentation required (besides what Vim provides),
  no anti-hacking design (quoting @romainl).
- Efficient loading. Avoid or minimize `execute` statements, complex logic, etc…
  Colorschemes should not take half a second to load!
- Consistent structure to help your grandchildren maintain your colorscheme when
  you will have become dust (because Vim will still be there).

Besides, to be included in Vim distribution, a colorscheme should be released
under the Vim license.

Using this template will help you meet the requirements above. Just follow the
instructions below.

## How to use this template

Clone this repo and edit `colortemplate.txt`. Editing consists of three
steps:

1. Fill out the “Mandatory information” section of the file.
2. Define your color palette in the corresponding section of the file.
3. Update the highlight group definitions as you like.

To generate the colorscheme, save the template and give this command:

```vim
:Colortemplate
```

## Options

The colorschemes generated by this template support only one option:

```
let g:<colorscheme_name>_transp_bg = 0
```

Set this to `1` if you want to use a transparent background.
