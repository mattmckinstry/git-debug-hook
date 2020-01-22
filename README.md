# Git Pre-Commit check for certain words

Author:	Matt McKinstry
Thanks to:	Nikolaos Dimopoulos <nikos@niden.net>

# About

This is a pre-commit hook you put in your git repo.

It allows you to write comments in your code like this:

```javascript
debugger;
```

```C#
System.Diagnostics.Debugger.Launch();
```

When you try to commit this file, it bitches at you, saying:

```
These errors were found in try-to-commit files:

  user.js
```

Boom! You can't commit the file until you remove the Debug Launch line, which is a
great reminder to not commit your debug code.

# Usage

Simply copy the file `pre-commit` into the directory `.git/hooks`.  You may need to run `chmod +x .git/hooks/pre-commit;` from Bash

That's it!

# Supported languages

The hook detects language by file extension (ie, .js -> javascript, .cs ->
C#, etc).

- javascript
- C#

# Contributing

If you want support for a certain language, don't open an issue, I'll probably
just ignore it (being realistic here).

Fork the project and open a pull request. Be sure to also add your language to
the [supported language list](#supported-languages) or I'll contact the
authorities. GOOD DAY, SIR/MADAM/NON-GENDER-CONFORMING-FORMAL-TITLE.


