# mimelist

Discover and choose default XDG MIME applications

# Quickstart

```bash
curl "https://raw.githubusercontent.com/taylorskalyo/mimelist/master/mimelist"
chmod +x mimelist

./mimelist --help
```

## Examples

List applications that can open the file `README.md`.

```
$ ./mimelist README.md
MimeType: text/plain

Flags   Application  GenericName  Exec
-T----  nvim         Text Editor  nvim %F
```

Choose `nvim` as the default handler for files like `README.md`.

```
$ ./mimelist README.md -s nvim
MimeType: text/plain

Flags   Application  GenericName  Exec
*T----  nvim         Text Editor  nvim %F
```

Choose which columns are displayed. Any [recognized desktop entry key](https://specifications.freedesktop.org/desktop-entry-spec/latest/ar01s06.html) can be used as a column.

```
$ ./mimelist README.md -c "Default,Name,Categories,Keywords,Terminal,Comment"
MimeType: text/plain

Default  Name    Categories           Keywords      Terminal  Comment
true     Neovim  Utility;TextEditor;  Text;editor;  true      Edit text files
```
