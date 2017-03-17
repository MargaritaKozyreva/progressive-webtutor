# Содействие

If you want to contribute to[linux-insides](https://github.com/0xAX/linux-insides), please follow these simple rules:

1. Press the fork button:

   [![](https://camo.githubusercontent.com/03f63673b11d94c44dd7d1b4c470c602c5b833a1/687474703a2f2f6f6935382e74696e797069632e636f6d2f6a6a3274726d2e6a7067 "fork")](https://camo.githubusercontent.com/03f63673b11d94c44dd7d1b4c470c602c5b833a1/687474703a2f2f6f6935382e74696e797069632e636f6d2f6a6a3274726d2e6a7067)

2. Clone the repository from your account with:

   ```
   git clone git@github.com:your_github_username/linux-insides.git

   ```

3. Create a new branch with:

   ```
   git checkout -b "linux-bootstrap-1-fix"

   ```

   You can name it however you want.

4. Make your changes.

5. Don't forget to add yourself in`contributors.md`.

6. Commit and push your changes, then make a pull request from Github.

**IMPORTANT**

Please, don't forget to update your fork. While you made your changes, the content of the`master`branch can change because other pull requests were merged and it can create conflicts. This is why you have to rebase on`master`every time before pushing your changes and check that your branch doesn't have any conflicts with`master`.

Thank you.

# Contributing to Pro Git \(2nd Edition\)

## Licensing

By opening a pull request to this repository, you agree to provide your work under the[project license](https://github.com/progit/progit2/blob/master/LICENSE.asc). Also, you agree to grant such license of your work as is required for the purposes of future print editions to @ben and @schacon. Should your changes appear in a printed edition, you'll be included in the[contributors list](https://github.com/progit/progit2/blob/master/book/contributors.asc).

## Signaling an Issue

Before signaling an issue, please check that there isn't already a similar one in the bug tracking system.

Also, if this issue has been spotted on the git-scm.com site, please cross-check that it is still present in the pdf version. The issue may have already been corrected, but the changes have not been deployed yet.

## Small Corrections

Errata and basic clarifications will be accepted if we agree that they improve the content. You can also open an issue so we can figure out how or if it needs to be addressed.

If you've never done this before, the[flow guide](https://guides.github.com/introduction/flow/)might be useful.

## Large Rewrites

Open an issue for discussion before you start. These changes tend to be very subjective, often only clarifying things for some small percentage of people and it's rarely worth the time to accept them. Professional copy editors have already reviewed this content multiple times so while you may have somewhat better taste and grammar than we do it's unlikely that your prose is going to be_so_much better that it's worth changing vast swaths of text.

## Figures

The images in this book were generated using[Sketch 3](http://bohemiancoding.com/sketch/), with the[included sketchbook file](https://github.com/progit/progit2/blob/master/diagram-source/progit.sketch).

To add a figure:

1. Add a page to the sketchbook. Try to use the included symbols wherever possible.
2. Add a "slice" to your page. Give it a name that matches the destination PNG filename, relative from the root of the source directory.
3. Make sure your slice is set to export at "800w".

## Translations

Translations to other languages are highly encouraged but handled a little differently than the first edition. We now keep each translation in a separate repository and automatically build the output files through Atlas. This was something that was really difficult in the last edition.

Since each translation is a different repository, we can also have different maintainers for each project. The Pro Git team simply pulls them in and builds them for the translation teams. To get automatic builds, translations repositories will have to be under the[`progit`organization on GitHub](https://github.com/progit).

You can find out information on all the current translations and information on how to start your own at[http://progit.org/translations](http://progit.org/translations).

