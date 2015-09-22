## Handy stuff and tools for a faster, better workflow | Sublime | Composer | Laravel

After watching some tutorials from Laracasts I added a lot of snippets and packages


## Installation
- Origami : Out of the box, Sublime Text offers a handful of "split modes." However, if you want more control, then the Origami package is right up your alley.
	I've added these keybindings to my user settings:

```js
	{ "keys": ["super+ctrl+up"], "command": "create_pane", "args": {"direction": "up"} },
	{ "keys": ["super+ctrl+right"], "command": "create_pane", "args": {"direction": "right"} },
	{ "keys": ["super+ctrl+down"], "command": "create_pane", "args": {"direction": "down"} },
	{ "keys": ["super+ctrl+left"], "command": "create_pane", "args": {"direction": "left"} },

	{ "keys": ["super+ctrl+backspace"], "command": "destroy_pane", "args": {"direction": "self"} },
```

- advancedNewfile : Finding a folder and left/right clicking takes time, use the shortcut instead.

- laravel5Artisan : using artisan commands in sublime instead of opening a command prompt.

- phpCompanion : very useful, doesn't use any keybindings so you have to add them

in user keybindings:
```js
{"keys":["f9"],"command":"expand_fqcn"},
{"keys":["f10"],"command":"find_use"},
{"keys":["f7"],"command":"insert_php_constructor_property"},
```

- php getters and setters : generate getters and setters quickly.

- htmlBeautify : I've spend too much time on making my html look readable, this formats it in a blink.
- Html / css / js prettify : same as above

- phpfmt : format your php code to PSR2
for mamp pro users copy paste this in the user settings

```js
in your user settings:
if you use mamp pro the php_bin path is : "/Applications/MAMP/bin/php/php5.6.10/bin/php"
{
	"format_on_save": true,
	"php_bin":"/usr/local/bin/php",
	"psr2": true,
}
```

-SublimeLinter
-SublimeLinter-php
in user settings
```js
{
    "user": {
        "linters": {
            "php": {
                "@disable": false,
                "args": [],
                "excludes": []
            }
        },
        "show_errors_on_save":true,
    }
}
```

## Shortcuts
Windows
```js
Sublime
	["shift+ctrl+p"] 		Command palette
	["ctrl+p"] 				go to file
	["ctrl+p"] 				go to file + @ + find and jump to this

advancedNewfile
	[ctrl+alt+n]			new file
	["shift+ctrl+alt+n"]	advanced new file

php companion:
	[F9]					get classpath after clicking on classname
	[F10]					imports classname on top when clicking on classname in __construct()
	[F7]					generates a constructor on the fly

Origami
	["super+ctrl+up"] 			splits horizontal up
	["super+ctrl+right"] 		splits vertical to right
	["super+ctrl+down"]			splits horizontal down
	["super+ctrl+left"]			splits vertical to left

	["ctrl+c+d"] remove this splits and merge with other panel
```

Other useful keybindings
```js
{ "keys": ["super+shift+right"], "command": "indent" },
{ "keys": ["super+shift+left"], "command": "unindent" },
{ "keys": ["shift+super+up"], "command": "swap_line_up" },
{ "keys": ["shift+super+down"], "command": "swap_line_down" },
{ "keys": ["super+k", "super+f"], "command": "indentxml" },
{ "keys": ["super+shift+d"], "command": "duplicate_line" },
{ "keys": ["super+e"], "command": "run_macro_file", "args": {"file": "Packages/Default/Delete Line.sublime-macro"} },
{ "keys": ["super+k", "super+d"], "command": "diffy" },
{ "keys": ["super+k", "super+c"], "command": "diffy", "args": {"action": "clear"} },
{ "keys": ["super+v"], "command": "paste_and_indent" },
{ "keys": ["super+shift+v"], "command": "paste" },
```

## snippets
-[Migration snippets](https://github.com/jonasvanderhaegen/Handy-for-sublime-and-a-faster-better-workflow/blob/master/snippets-for-migrations.md)

-[Model snippets](https://github.com/jonasvanderhaegen/Handy-for-sublime-and-a-faster-better-workflow/blob/master/snippets-for-modelclasses.md)

-[Route snippets](https://github.com/jonasvanderhaegen/Handy-for-sublime-and-a-faster-better-workflow/blob/master/snippets-for-routes.md)
