---
title: miscellaneous git ethics
categories:
  - general programming
date: 2024-09-12T18:30:00.000Z
---

### use a .gitignore

a .gitignore file is a specification you put in the root directory of your application to tell which files should and should not be tracked by git. there are other ways to implement this (some people might suggest using allowlists instead of blocklists, or nested gitignores, but if you've reached that level of complexity this message probably isn't helpful for you).

a lot of small projects start with just five or ten files. a few hundred lines of code, an alpha commit on the dev branch, usual stuff. at this point, one might think that you already have track of all the files in your repository. why would you need to mention these when you're already specifying files in each commit?

for one, a lot of files are sneaky. .vscodeand .idea directories can sneak into the repository undetected, and this may or may not be intended. while syncing per-project editor configs is nice if you know what you're doing, a lot of people don't. .DS\_STORE files are also nasty for going undetected into repositories. of course, in this case the harm is mostly just a mild annoyance.

another pollutant is build artifacts / binaries. depending upon your language of choice, these may or may not be isolated to their own directory automatically. regardless, architecture-specific binaries should not be committed to your repository, not only because they make for terrible diffs, but also because they might mislead the user. VSCode's auto-generated debug binaries can also end up being committed if you're not careful.

additionally, contributors might find themselves wanting to have local configuration files for their repositories. .envs are the simplest example, but it's also nice to have a TODO checklist in your repository, other configurations, and maybe even some documentation that shouldn't be on the repository. you might prefer keeping those inside your project directory for convenience and then gitignoring them.

search one from [here](here "https://github.com/github/gitignore"), and have it in your code. gitignores are essential from the first commit of your project.

### respect the diffs

not a lot of thought is given to diffs when making a commit. different languages have different protocols, but both Python and Go use trailing commas for multi-line lists. these are nifty because adding / removing a line from the list only shows up that line in the diff. 

diffs give a surface-level overview of what you have done. the red is what you have removed, the green is what you have added. whoever looks at and reviews your code will immediately draw their attention to those things. avoid rearranging components, renaming them, or reorganising code blocks unless it is necessary.

### auto-format your code

more of a practice now than in the past, formatting your code before committing is important for reducing merge conflicts / unnecessary diffs. maybe you like tabs and your coworker likes spaces. in the age of the IDE, this doesn't really matter. i entered Go with certain preferences about formatting from Python, but i still let gofmt handle everything. in fact, i also recommend organising your imports to be a deterministic order (see gci), which isn't a thing in default Go formatters for some reason.

line endings may or may not matter. sometimes tools are line ending dependent, most of the time your editor manages them for you. chances are, you won't ever have to think about line endings of your code files. but normalising them is a good idea regardless, especially if your team works in multiple operating systems.

 
