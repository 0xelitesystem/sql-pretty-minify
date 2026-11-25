# SQL Pretty Minify

Pretty-print and minify SQL in your browser. No server, no tracking, no third-party scripts.

**Live demo:** https://0xelitesystem.github.io/sql-pretty-minify/

## Use

Open `index.html` in any modern browser, or visit the GitHub Pages link in the repo description.

Paste SQL on the left. The output updates live. Options:

- **Pretty-print:** put major clauses on their own lines, break columns after commas, indent parenthesized groups, and place AND and OR on their own indented lines.
- **Minify:** collapse the statement to a single compact line with tidy spacing.
- **Uppercase keywords:** toggle to force reserved words (SELECT, FROM, WHERE, JOIN, and so on) to uppercase while leaving identifiers and string contents untouched.
- **Indent:** choose 2 spaces, 4 spaces, or a tab for pretty-print.

The tokenizer is written for this tool and handles:

- Single quoted strings, including doubled quote escaping
- Double quoted and backtick quoted identifiers
- Line comments (`--`) and block comments (`/* ... */`)
- Numbers, operators, and punctuation
- Common multi-word clauses like GROUP BY, ORDER BY, UNION ALL, and the JOIN family

Keyword casing only affects recognized SQL keywords. Content inside strings and quoted identifiers is preserved exactly.

Note: this formats SQL, it does not validate it against a specific database dialect.

## Why this exists

Formatting SQL by hand is tedious, and many online formatters run your query through a remote server. This is a single HTML file with its own tokenizer, so the query never leaves the page.

## Privacy

Everything runs in your browser. The SQL you paste never leaves your machine. Verify by viewing the page source or by opening DevTools and watching the network tab; no requests are made.

## Run locally

```bash
git clone https://github.com/0xelitesystem/sql-pretty-minify
cd sql-pretty-minify
# Open index.html in your browser, or:
python -m http.server 8000
```

## Build

There is no build. It's a single HTML file with inline CSS and JavaScript.

## More

Part of a catalog of single-file browser tools and plain-language references, all MIT licensed and dependency-free: [0xelitesystem.github.io](https://0xelitesystem.github.io/). Built by [elitesystem.ai](https://elitesystem.ai).

## License

MIT.

## Related

- [json-formatter-and-validator](https://github.com/0xelitesystem/json-formatter-and-validator)
- [csv-to-anything](https://github.com/0xelitesystem/csv-to-anything)
- [case-converter](https://github.com/0xelitesystem/case-converter)
