## Handy stuff and tools for a faster, better workflow | Sublime | Composer | Laravel

After watching some tutorials from Laracasts I added a lot of snippets and packages


## Installation
- Origami : Out of the box, Sublime Text offers a handful of "split modes." However, if you want more control, then the Origami package is right up your alley.
	I've added these keybindings to my user settings:

```js
{ "keys": ["ctrl+c+up"], "command": "create_pane", "args": {"direction": "up"} },
{ "keys": ["ctrl+c+right"], "command": "create_pane", "args": {"direction": "right"} },
{ "keys": ["ctrl+c+down"], "command": "create_pane", "args": {"direction": "down"} },
{ "keys": ["ctrl+c+left"], "command": "create_pane", "args": {"direction": "left"} },

{ "keys": ["ctrl+c+d"], "command": "destroy_pane", "args": {"direction": "self"} },
```

- advancedNewfile : Finding a folder and left/right clicking takes time, use the shortcut instead.

- laravel5Artisan : using artisan commands in sublime instead of opening a command prompt.
- phpCompanion : very useful 

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

```js
in your user settings:
	windows:
	{
		"format_on_save": true,
		"php_bin": "C:/xampp/php/php.exe",
		"psr2": true,
		"version": 1
	}

	mac:
	{
	"format_on_save": true,
	"php_bin":"/usr/local/bin/php",
	"psr2": true,
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
		["ctrl+c+up"] 			splits horizontal up
		["ctrl+c+right"] 		splits vertical to right
		["ctrl+c+down"]			splits horizontal down
		["ctrl+c+left"]			splits vertical to left

		["ctrl+c+d"] remove this splits and merge with other panel
```

## snippets
-[Migration snippets](https://github.com/jonasvanderhaegen/Handy-for-sublime-and-a-faster-better-workflow/blob/master/snippets-for-migrations.md)

-[Model snippets](https://github.com/jonasvanderhaegen/Handy-for-sublime-and-a-faster-better-workflow/blob/master/snippets-for-modelclasses.md)

-[Route snippets](https://github.com/jonasvanderhaegen/Handy-for-sublime-and-a-faster-better-workflow/blob/master/snippets-for-routes.md)
