# creative-constraints
An evergreen list of creative constraints for modern research in physical science based on best practices and accumulated wisdom.

1. **Use YYYYMMDD format when including dates in filenames.**  
We often are in a situation where we want to sort a list of files in chronological order, usually to get to the newest or oldest file for example.  Including the date in the filename with `YYYYMMDD` format will automatically achieve this goal, since operating systems sort alphanumerically.   The `MMDDYYYY` and `DDMMYYYY` formats will sort them out of date order, which is usually not useful.


2. **Use pandas' `read_csv` to read in `.csv` files in Python.**  
Lots of data files get stored as [.csv files](https://en.wikipedia.org/wiki/Comma-separated_values).  There is no standard for `.csv` files and so they can be annoying to read in.  The [pandas](https://pandas.pydata.org) library offers the `.read_csv(filename, ...)` function that takes in a `filename` and reads it into an easy-to-use format.  The method supports dozens of optional keyword arguments `...` that can handle virtually any of the bizarre-albeit-common ways that `.csv` files can be malformed.


3. **Pad numbers-destined-for-filenames with leading zeros.**  
You often want to sort a bunch of files with different running numbers: `file1`, `file2`, `file10`.  If you are creating those files, you should pad the numbers with zeros: `file01`, `file02`, `file10`.  Think of the largest value the running number could plausibly be and pad the filename with that number of zeros: `file0001` or `file00000001`.


4. **Each project should be a repository on GitHub.**  
Each project should be its own standalone repository on GitHub.  A project is essentially any research program that could one day become a published paper.  Default to making the repository private for its early stages, and make it public when you publish a paper.  

5.  **Your project should have a short code name.**  
Your project should have a distinctive one-to-three word code name, which will serve as its GitHub repository name.  The code name may also become used for its Python package name, environment variables, file basenames, and other places, so pick a name you are comfortable seeing a lot.  A creative constraint is to pick a category (song name, bird name, location) and scan through lists of them for something that tangentially resonates with your project.


6.  **Your project should have `code/`, `data/`, `paper/`, and `notebooks/` directories.**  
The top-level directory of your project is what you see when you go to GitHub.com--- it should have a `README.md` file, a LICENSE, and typically three-to-six directories:`code/`, `data/`, `paper/`, and `notebooks/`.  Some projects may have, say, `models/` instead of `data/`, or `document/` instead of `paper/`, but the key idea is to organize the project into these different parts.  Documentation, configuration files, and other directories are common too.


7. **Use GitHub Issues to track problems and goals for your research project.**  
The GitHub Issue tracker may seem like overkill if it's just you working on a project.  But it has a few long-term benefits: it co-habitates with your project, so if you ever make the project public, the thought process and timeline behind it will become part of the public project history.   That history may be useful to others and is certainly useful to your future self.  It will make it possible for others to see (and you to remember) the rationale and internal monologue behind changes to the project.  If you are working with other people, the Issue tracker is even more valuable--- it houses conversations and deliberations about changes to the project and provides a searchable one-stop-shop for anyone added to the project later.  


8. **Constantly use shift-tab within methods in Jupyter-notebooks.**  
If you hit `shift`-`tab` inside the parentheses of a Python method in Jupyter Notebook, it shows you the method's [docstring](https://en.wikipedia.org/wiki/Docstring), a "how-to" guide of the method's inner workings.  Some other tools like VSCode show this too, but the one in Jupyter is great.  I simply cannot imagine coding without using this, it borders on life-changing.  There is also the ability to hit `[tab]` directly after an object's `.` to show what attributes and methods are available.  You should constantly be using these conveniences.

9. **Backup your computer.**  
You should have an automated way of backing up your computer.  Most universities and workplaces will offer a free service for backups nowadays.  If you do it right, you only have to set this up once and don't have to think about it again unless something goes wrong.


10.  **Set up a git workflow to show you what has changed in your project, at a glance.**  
One of the misconceptions of version control is that it is just for large projects that release monolithic downloadable versions of their Apps.  False!  One of the most useful aspects of version control comes even if you work alone.  It's the ability to see what's changed in your project at a glance, *while you are changing it*.  Imagine you are making a complicated change to a codebase.  You spend a while making changes and pause to reflect--- "Where did I leave off yesterday?  What did I just do for the last hour?  Where did I change that section for formatting the file output?".  Tools like git, [GitKraken](https://www.gitkraken.com), [SourceTree](https://www.sourcetreeapp.com), and others allow you to see the *diff* of your live, changed version.  You should set up your workflow to have this live view of your progress.  It's liberating!  It allows you to be more experimental, knowing you can roll back changes if they are deleterious.  It guides you to internalize and reflect on what you did, and summarize it in a sentence.

11.  **Run LaTeX papers through grammar-and-spell-checking, even if it's strange**  
Working with LaTeX has its pluses and minuses.  One demerit of LaTeX is that it usually doesn't have high-quality grammar checking like Microsoft Word, Grammarly.com, or other [WYSIWYG](https://en.wikipedia.org/wiki/WYSIWYG) text editors.  It's still possible, but slightly annoying, to grammar-check your LaTeX files.  You can copy and paste the entire manuscript---equations tables and all---into [Grammarly.com](https://www.grammarly.com/), and use their `skip` button for any LaTeX-specific red herrings, there will be many of these.  You'll probably still find a bunch of grammar issues this way, and while it's not perfect, it works.  When you're done, copy-and-paste back into your manuscript.  If you're following rule 10 (*Set up a git workflow to show you what has changed in your project, at a glance.*), you will be able to see exactly what changed between the last copy-paste, so you'll know the process didn't mess up the LaTeX formatting.  Pro Tip: use `git diff --word-diff ms.tex` to the word-by-word changes since your last commit.
