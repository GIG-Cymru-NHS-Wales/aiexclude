# aiexclude file for Google Gemini AI

<https://firebase.google.com/docs/studio/set-up-gemini#exclude-files>

You can control which files in your codebase should be kept hidden from Gemini
by including `.aiexclude` files in your project. This lets you granularly
control the project context you share with Gemini.

Much like a `.gitignore` file, an `.aiexclude` file tracks files that shouldn't
be shared with Gemini, including the chat experience as well as AI features that
operate in the editor. An `.aiexclude` file operates on files at or below the
directory that contains it.

Note: Files ignored by `.gitignore` files in your repository are automatically
excluded, even if they're not listed in an `.aiexclude` file.

Files covered by `.aiexclude` won't be indexed by Gemini when Codebase Indexing
is enabled. Additionally, `.aiexclude` will affect inline assistance for covered
files in the following ways:

- Chat assistance: Gemini won't be able to answer questions or offer suggestions
  about files covered by `.aiexclude`.

- Code completion: Suggested code completions will not be available when editing
  covered files.

- Inline assistance: You'll be able to generate new code, but not modify
  existing code when editing covered files.

## How to write .aiexclude files

An .aiexclude file follows the same syntax as a .gitignore file, with these
following differences:

- An empty .aiexclude file blocks all files in its directory and all
  sub-directories. This is the same as a file that contains **/*.

- .aiexclude files don't support negation (prefixing patterns with !).
