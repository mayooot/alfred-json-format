# Alfred-Json-Format

# Overview

🤘An Alfred workflow that formatting a copied json string to the pasteboard using `jq`.

![Alfred.png](docs%2FAlfred.png)

# Install

You must first install `jq`.

~~~
brew install jq
~~~

And You can get `Alfred-Json-Format` via [release](https://github.com/mayooot/alfred-json-format/releases) or `git clone`
this repo.

~~~
git clone https://github.com/mayooot/alfred-json-format
~~~

# Usage

You need to copy the json string that needs to be formatted and invoke the Alfred shortcut, type `json` and enter.

The formatted json will then appear on your pasteboard.

![screenshot.png](docs%2Fscreenshot.png)

# Example

Once we have copied the json string, call the Alfred shortcut, type `json` and enter.

~~~json
{"foo":0,"bar":1}
~~~

Your pasteboard will then append a formatted json string that looks like this:

~~~json
{
  "foo": 0,
  "bar": 1
}
~~~

Of course, if you copy an error json string, it looks like this:

~~~json
{"foo":0,"bar":1,}
~~~

There will then be a message telling you that this json formatting failed, and you can use `⌘ + v` to view the error
message.

![alert.png](docs%2Falert.png)

~~~
jq: parse error: Expected another key-value pair at line 1, column 18
~~~

# Contribute

Feel free to open issues and pull requests. Any feedback is highly appreciated!