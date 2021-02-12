# SublimeText Syntax highlighting for textual BBC BASIC files

A SublimeText syntax definition for BBC BASIC text files to enable syntax highlighting.
Although the keywords are complete for the BASIC V/VI versions used by RISC OS, it should also
be suitable for earlier versions, as well as versions for other platforms.

## Colouring

The syntax colouring recognises the keywords, and some of the language features.

The coloured features are:

* Comments, prefixed by `REM`.
* Function and procedure declarations (and their end).
* Function and procedure invocations.
* Control and loop structures.
* Line number prefixes.
* BASIC style hex (`&xxx`) and binary (`%bbb`) numbers.
* CLI commands, prefixed by `*` at the start of a line.

Unsupported features:

* Inline assembly blocks.
* Understanding of the context.


## File recognition

BBC BASIC files are usually given names with a suffix `,fd1` when stored on non-RISC OS filesystems. `fd1` is the filetype number for Textual BASIC code. Non-RISC OS versions of
BBC BASIC use the extension `.bbc` which is recognised by the syntax mode.

To force the use of the BBC BASIC mode for these files, it is recommended that the ApplySyntax package (or similar) be used to select the syntax mode.

The following configuration is suitable for use within `ApplySyntax.sublime-settings`:

```
        {
            // BBC Basic using RISC OS naming convention and extension
            "syntax": "BBCBASIC/BBCBASIC",
            "rules": [
                {"file_path": ".*(,fd1|\\.bbc)$"},
            ]
        },
```


## Install manually

* Place the `BBCBASIC.sublime-syntax` file inside the Sublime Text packages User folder (`Preferences | Browse Packages...`)
* Restart Sublime Text


## Install with Package Control

* Install [Package Control](http://wbond.net/sublime_packages/package_control)
* Run “Package Control: Install Package” command, find and install `BBC BASIC` package.
* Restart Sublime Text if necessary

## License
This package is licensed under the MIT License.
