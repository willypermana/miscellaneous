Just put the font size command before \makecell.

Like so:

`{\small\makecell{SOME\\LONG\\TEXT}}`

In a multicolumn or multirow command:

`\multicolumn{c}{2}{\multirow{2}[0]{*}{\small\makecell{SOME\\LONG\\TEXT}}}`
