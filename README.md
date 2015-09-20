<h1>Declarative programming course</h1>
<p>Labs on declarative programming KPI course </p>
<h2>Setup Common Lisp </h2
<b>Install interpreter:</b>
- Install [Steel Bank Common Lisp](http://www.sbcl.org/platform-table.html).
- Setup system path with "C:\Program Files (x86)\Steel Bank Common Lisp\1.2.15\"

<b>Setup Sublime Text 2: </b>
- Install SublimeREPL repository
- Open menu "Tools > Build System > New Build System..." and create SBCL build system: <br> <i>
{
	"cmd": "C:/Program Files (x86)/Steel Bank Common Lisp/1.2.15/sbcl --disable-debugger --load $file",
    "working_dir": "$file_path"
}</i>
- Open menu "Preferences > Key Bindings - User" and put new key binding:  <br>
<i>[
{
"keys": ["ctrl+j"],
"command": "repl_open",
"args": {
"type": "subprocess",
"encoding": "utf8",
"cmd": ["sbcl", "-i"],
"cwd": "$file_path",
"external_id": "lisp",
"syntax": "Packages/Lisp/Lisp.tmLanguage"
}
}
]</i>
- [Sublime + Common Lisp Guide](https://marktrapp.com/blog/2014/01/20/lisp-with-os-x-sublime-text/) for more information
