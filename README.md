# Lab Assignment: Branching

In this lab, you will be contributing edits to a spreadsheet containing digital collections metadata. This lab simulates the process for contributing to a Git repository that you have "read-write" permissions using the [Git Feature Branch Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow). Your task will be to edit the spreadsheet, document your changes, and push a new version of this spreadsheet with your edits as a branch using Git and GitHub from the command line. 

> **Branch:** A branch represents an independent line of development. Branches serve as an abstraction for the edit/stage/commit process. You can think of them as a way to request a brand new working directory, staging area, and project history. ["Git Branch" by Atlassian](https://www.atlassian.com/git/tutorials/using-branches)

## Instructions

>If you're on macOS or Linux, you can use your default terminal program as your command line interface. If you're on Windows, please use Git Bash. 

1. Open your terminal to your project folder (`learn-git`) and clone this repository to your computer with SSH:

```bash
git clone git@github.com:chrisdaaz/branching.git
cd branching
```

2. Create a new branch for your edits. The following example uses my last name (`diaz`) as the new branch name. Use your own for this lab (no spaces, lowercase):

```bash
git branch diaz
```

3. Switch to your new branch:

```bash
git checkout diaz
```

4. [Download the metadata file](https://docs.google.com/spreadsheets/d/1TCcrJ3-Vx_rRb2XzoHmzHiDkz1ZWsWw8bmsXSmMPTcY/edit?usp=sharing) and add it to your repository's working directiry by saving the file to the `collaboration` folder on your computer. 

5. Add the metadata file to the repository's staging area:

```bash
git add metadata.csv
```

6. Commit the file to your repository:

```bash
git commit -m "adds metadata file"
```

7. Open the `metadata.csv` file in a spreadsheet editor (e.g. Microsoft Excel, Google Sheets, etc.) and make some edits to values within the `Title` columns (write anything you want, just make sure it's different than what's there). When you save the file, **do not change the format from CSV to anything else**.

8. Commit your changes to your repository:

```bash
# the -am flag is a shortcut for combining git add and git commit into one command
git commit -am "edits to titles"
```

9. Open the `metadata.csv` file in a spreadsheet editor (e.g. Microsoft Excel, Google Sheets, etc.) and make some edits to values within the `Dates` columns (write anything you want, just make sure it's different than what's there). 

10. Commit your changes to your repository:

```bash
# the -am flag is a shortcut for combining git add and git commit into one command
git commit -am "edits to dates"
```

11. Open the `metadata.csv` file in a spreadsheet editor (e.g. Microsoft Excel, Google Sheets, etc.) and make some edits to values within the `Descriptions` columns (write anything you want, just make sure it's different than what's there). 

12. Commit your changes to your repository:

```bash
# the -am flag is a shortcut for combining git add and git commit into one command
git commit -am "edits to descriptions"
```

13. Create a log file for your repository:

```bash
git log > log.txt
```

14. Commit the log file to your branch:

```bash
git commit -am "adds git log"
```

13. Push new branch with your to the `origin` remote on GitHub:

```bash
git push origin diaz
```

14. Visit the repository on GitHub: https://github.com/chrisdaaz/collaboration-lab

15. If you're logged in, you should see your branch available on the GitHub repository, as well as a button to compare and create a pull request. Open a pull request with your branch on the repository ([instructions](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request)). You can give your pull request a name and add a description to provide some helpful context (not necessary here, but FYI for future pull requests). 

That's it!

## Credits

This lab uses a metadata file from the [CollectionBuilder](https://collectionbuilder.github.io/) [demonstration exhibit](https://collectionbuilder.github.io/collectionbuilder-gh/data.html).
