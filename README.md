Language autoselect, DE and EN are preconfigured.<br />
Just place files into Friendica root folder

# Adding another language

The Javascript autoselects whatever your browser language is set to. If it can't find the language it falls back to English. So to add another language (e.g. French) you need to do these steps:

1) Add French (fr) to the languages available in [line 22](https://github.com/vinzv/friendica-loginpage/blob/1ce7cf6bf2fa23ef23af7c90f22ae1484096725c/home.html#L22):<br />
`var known = { en: true, de: true, fr: true};`

2) Duplicate all blocks that have `lang="en"` in their opening tag. So basically copy everything from [line 72](https://github.com/vinzv/friendica-loginpage/blob/1ce7cf6bf2fa23ef23af7c90f22ae1484096725c/home.html#L72) to line 107 and paste it directly below line 107.

3) In that freshly pasted code block change every occurence of `lang="en"` to `lang="fr"`. That would be four times if I didn't miscount.

4) Furthermore in that pasted block replace the English texts with your translated French ones.

*As a side note:*<br />
If you want to change the texts per se just edit it in every language section. Especially the bits inside `<h1>…</h1>` at line 38 and line 75 are subjecty to that, as there's the name of my node stated.
