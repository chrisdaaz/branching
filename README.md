# Lab Assignment: Branching

> Make sure the instructor has your GitHub username either by submitting the `Your First Repository` lab assignment via Moodle or messaging him with your username. 

In this lab, you will be contributing edits to a spreadsheet containing digital collections metadata. This lab simulates the process for contributing to a Git repository that you have "read-write" permissions using the [Git Feature Branch Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow). This is a common workflow for teams who work together on a specific project, where each team member has `push` access to the git repository. Your task will be to edit the spreadsheet, document your changes, and push a new version of this spreadsheet with your edits as a branch using Git and GitHub from the command line. 

> **Branch:** A branch represents an independent line of development. Branches serve as an abstraction for the edit/stage/commit process. You can think of them as a way to request a brand new working directory, staging area, and project history. ["Git Branch" by Atlassian](https://www.atlassian.com/git/tutorials/using-branches)

## Instructions

> If you're on macOS or Linux, you can use your default terminal program as your command line interface. If you're on Windows, please use Git Bash. If you'd not comfortable with command line Git, you can also use [GitHub Desktop](https://desktop.github.com/). 

1. Open your terminal (you might want to create a directory for git projects, `mkdir learn-git && cd learn-git`) and clone this repository to your computer and change directories into it:

```bash
git clone https://github.com/chrisdaaz/branching.git
cd branching
```

2. Create a new branch for your edits. The following example uses my last name (`diaz`) as the new branch name. Use your own for this lab (no spaces, lowercase):

```bash
git branch diaz
```

3. List your available branches with the `git branch` command and switch to your new branch with the `git checkout <branch-name>` command:

```bash
git branch
git checkout diaz
```

4. We're going to be working with a spreadsheet in CSV format. CSV is a plain text format for data, where as Excel files (like `.xlsx`) are proprietary files. Git is able to track the _specific_ differences between versions of CSV files (down to the character) but not proprietary file formats like Microsoft Excel. [Download the metadata file](https://docs.google.com/spreadsheets/d/1TCcrJ3-Vx_rRb2XzoHmzHiDkz1ZWsWw8bmsXSmMPTcY/edit?usp=sharing) and add it to your repository's working directory by saving the file to the `branching` folder on your computer. You can use your File Explorer application to move the file from the "Downloads" folder to the `branching` repository folder.

5. Once it's been added. Git knows about it. Run the `git status` command to verify that the file is "untracked" within your working directory. Now, add the metadata file to the repository's staging area:

```bash
git status
git add metadata.csv
```

6. Commit the file to your branch:

```bash
git commit -m "adds metadata file"
```

7. Open the `metadata.csv` file in a spreadsheet editor (e.g. Microsoft Excel, Google Sheets, etc.) and make some edits to values within the `Title` columns (write anything you want, just make sure it's different than what's there). When you save the file, **do not change the format from CSV to anything else**. You can keep the file open as we'll be saving and committing multiple versions of this file to your branch's history.

8. Commit your changes to your repository. The `-am` flag in place of the usual `-m` is a shortcut for combining `git add` and `git commit` into one command:

```bash
git commit -am "edits to titles"
```

9. Make some edits to values within the `Dates` columns (write anything you want, just make sure it's different than what's there). Save the file. 

10. Commit your changes to your repository:

```bash
git commit -am "edits to dates"
```

11. Make some edits to values within the `Descriptions` columns (write anything you want, just make sure it's different than what's there). Save the file.

12. Commit your changes to your repository:

```bash
git commit -am "edits to descriptions"
```

13. Create a log file for your repository:

```bash
git log > log.txt
```

14. Commit the log file to your branch:

```bash
git add log.txt
git commit -m "adds git log"
```

13. Push your new branch with your to the `origin` remote on GitHub. You'll have to replace `<name of your branch>` with whatever you named your branch in step 2:

```bash
git push origin <name of your branch>
```

14. Visit the repository on GitHub: https://github.com/chrisdaaz/branching

15. If you're logged in, you should see your branch available on the GitHub repository, as well as a button to compare and create a pull request. 

> A Pull Request is a method of contributing changes from one branch to another. If the changes are accepted by the repository administrator, the Pull Request is merged to the target branch. Pull Requests are a good opporunity to test code and request feedback from collaborators. The GitHub interface allows team members to comment and highlight specific changes within the code to discuss the changes.

Open a pull request with your branch on the repository ([instructions](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request)). You can give your pull request a name and add a description to provide some helpful context (not necessary here, but FYI for future pull requests). 

That's it!

## Credits

This lab uses a metadata file from the [CollectionBuilder](https://collectionbuilder.github.io/) [demonstration exhibit](https://collectionbuilder.github.io/collectionbuilder-gh/data.html).
