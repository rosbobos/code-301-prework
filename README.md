# Code 301 Pre-work: Intermediate Software Development

To get your laptop and yourself ready for the start of Code 301, there are a series of pre-work tasks to complete. 

Before completing the tasks in this document, ensure that you have completed all of the installation tasks in the [Code 201 Prework](https://github.com/codefellows/code-201-prework).

In particular, if you have tested in to Code 301 and did not take Code 201, be especially attentive to the git and GitHub portion of the Code 201 prework. Note that your future classmates who took 201 will already have a month of practice using git and GitHub; it is a common area of challenge in 301 for students who tested in to the course. 

Note that the tasks below have a corresponding assignment to submit in your Canvas course, but be aware that at the time you receive the link to this pre-work that the Canvas course may not yet be published, depending upon the timing of Admissions processes and when class begins. Typically, Canvas courses are published 5-7 days before class begins.

## Code Assignments

### jQuery

Complete all of the [Codecademy course in jQuery](https://www.codecademy.com/en/tracks/jquery). The Canvas submission is a screenshot indicating that the course is complete.

### Code Wars

Throughout Code 301 you will be completing a series of assignments at [Code Wars](https://www.codewars.com).

1. If you do not already have one, sign up for a user account at Code Wars.
2. Complete [this kata](https://www.codewars.com/kata/array-element-parity/javascript).
3. In the corresponding Canvas assignment, submit a link to your Code Wars profile page and copy/paste your solution code into the text box.

### Chocolate Pizza CSS

This assignment is optional, **if** you are coming from a Code 201 class that ended within 2 weeks of the start of your Code 301 class. 

Students in Code 201 complete a time-boxed design comp assignment, called "Chocolate Pizza". This is a revisiting of that assignment:

  - Rather than the "complete as much of the assignment as you can in the available time" approach in Code 201, the goal here is to get the HTML/CSS mockup to be pixel-perfect.
  - Create and use a 960-pixel CSS grid system to manage display of the content. Look at [this article](http://j4n.co/blog/Creating-your-own-css-grid-system) as a reference.
  - Your column of content should be centered in the window, as in the preview image.
  - Your solution does not need to be responsive in any way.
  - Do not use any negative margins, or Flexbox positioning

**Instructions:**

1. Create and clone a new GitHub repository to house the code for this project.
2. Immediately check out a new branch in which to do your work.
3. Save the contents of the [`assets` directory](https://github.com/codefellows/code-301-prework/tree/master/assets){:target="_blank"} into an `assets` directory in your project.
3. Write your code in two files: `index.html` and `style.css`. You do not need to include JavaScript.
3. Use the included `PREVIEW.png` image as a reference; your goal is to match it as closely as possible.
4. Making regular Git commits with appropriately descriptive commit messages while you are working.
5. When finished, be sure to push your final code to GitHub and merge your branch into  `master`.
6. Deploy your page using a `gh-pages` branch or via the options in the repository "Settings" tab.
7. Submit the links to your repoitory AND your deployment in the corresponding Canvas assignment.

## Setup of Your Laptop Dev Environment (Canvas assignment)

Completion of the following setup tasks are all to be submitted in a single Canvas assignment. Keep a log of any errors or difficulties you encounter, and include those with your submission.

### Install PostgreSQL Database Software
*Please note that if you have a previously installed version of PostgreSQL on any operating system, you should be aware of any username and password that you've set for that installation. If you're unsure please uninstall and reinstall a fresh copy, which will also install the latest stable version. Additionally, if you are using a version before 9.5, you should uninstall and reinstall. You will be unable to complete certain labs if you are using version 9.4 or previous!*

For both Windows and Linux users, please follow the default installation instructions taking care not to change values such as the default port numbers (You may be prompted to change them, but should also be given default values).

#### Windows

*For reference, these instructions are taken from the following documentation: http://www.postgresqltutorial.com/install-postgresql/*

**NOTE: If you are running Windows 8 or 10, you need to create a Windows user with administrator role e.g., postgres and use this user to run the installation file.**

- Your **Default** database super user is: *postgres*
- You will be asked to enter and confirm a database password.
- **Be sure you document your default user and password**, as you will need them later in the course. We are working securely on your computer, so a simple password like `1234` will suffice, and there's no need to change the default user.

**There are three steps to complete the PostgreSQL installation**:

1. Download PostgreSQL installer for Windows
1. Install PostgreSQL
1. Verify the installation

**Downloading the installer**

- Go to the PostgreSQL [official website](http://www.postgresql.org/download/windows/).
- Click on the [download installer from EnterpriseDB](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads#windows). Choose the latest version to download. It takes a few minutes to complete the download.

**Installing**

Double click on the installer file. An installation wizard will appear and guide you through multiple steps where you can choose different options that you would like to have in PostgreSQL. For now, just select default values. Once it's done installing then move to the next step.

At the time of writing, PostgreSQL does not get added to your path by default, so we will need to add it manually, but future versions may fix that. So let's check real quick:

- Open Git Bash and type `psql -U postgres` .
- If you get a prompt asking for a password then PostgreSQL was installed and added to your PATH. You can skip to the Verify Installation section below.

- If you get and error similar to `bash: psql command not found` then that means you will need to add Postgres to your path. Follow the steps below to do that.

**Adding psql to your PATH**

Normally when programs are installed ( like VScode for Windows) they are automatically added to your PATH which means you can type a quick command to execute the program ( like `code` for VScode for example). Here is how you add the psql command to your PATH which will allow you to launch PostgreSQL in Git Bash.

- Copy this line, `C:\Program Files\PostgreSQL\<version>\bin` and put the version number of PostgeSQL inside of  <version>. IE `C:\Program Files\PostgreSQL\10\bin`.
- Open your system settings. ( On windows 10 you can right click on the start menu and navigate to settings ).

- You should see a search bar. Type `env` and the search will populate with a couple options. Choose the option that says "Edit the System Enviroment Settings".
![](https://i.imgur.com/ZT7xvD9.png)

- A small window will pop-up. At the bottomm, directly above the cancel button, is another button that says Enviroment Variables. Click that.
![](https://i.imgur.com/IjkiSrk.png)

- Another window will pop-up. This is where you can see all of your enviroment variables. Click on the one that says PATH, and then click edit.
![](https://i.imgur.com/t25DE7n.png)

- Finally, this last page will show you all of the things that are attached to your PATH. If you have installed Node and VS Code you may seem them in here! Click on New and you'll see a text entry box appear in the middle of the page. Paste in the line that you copied from step 1. Hit enter and then make sure to click Okay on all 3 previous boxes!
![](https://i.imgur.com/1RmmVdh.png)
 
- Close out of all windows, restart your computer, and move to Verify Installation!


**Verify Installation**

- Open the Git  Bash terminal and type `psql -U postgres`. It should prompt you for a password. If you get the error `bash: psql command not found`, and you already followed the steps for adding psql to your path then try restarting your computer then going through the above steps again to see if PostgreSQL is still attached to your PATH. If it's not, then and add it again. Restart and try again this step again. **_If it still isn't working, then let the instructor know and skip to the Alternate Verify Installation section.

- If it did work and you were prompted to enter a password then psql has been successfully added to your PATH.  
- In the password field, enter the password that you gave when you installed PostgreSQL.
- If it works, then your terminal window will change to the PostgreSQL interface.
- In this window, you can enter SQL statements, which must end with semicolons. Congratulations,you've installed PostgreSQL correctly!

- Note: If you used a different username then you can specify that after the `-U` in `psql -U <username>`. In most cases, by default the username is postgres, but it may have been changed to the username that you're currently logged into your computer account with. 

**If you are having issues with the installation, please inform your instructor and try the Alternate Verify Installation.**



**Alternate Verify Installation**

When you installed PostgreSQL, the installer also installed some extra tools. One of them is psql (it may be called SQL Shell).

- Open the SQL shell program.
- When it prompts you for input, just hit enter to select default values until it asks for a password. You will put in the password you entered during installation.
- You should have a window that [looks like this](http://www.postgresqltutorial.com/wp-content/uploads/2012/08/psql.png).
- In this window, you can enter SQL statements, which must all end with semicolons. Congratulations, you've installed correctly!

**If you are having issues with the installation, please contact your instructor.**



#### Linux

*For reference, these instructions are taken from the following documentation: https://www.postgresql.org/download/*

- If asked to provide or set a username and password, **be sure to document the username and password**, as you will need them later in the course.
- `sudo apt-get install postgresql`
- You will be prompted with the message that a certain amount of disk space will be used and asked if this is OK. Type `y`, then hit enter.
- Several commands will automatically run, this may take a few minutes.
- **You will likely NOT be prompted for a default username or password.** You will need to set one in psql if this is the case.

**Verifying Installation And Setting A Password**
- You should be able to run the command `sudo -u postgres psql`. You will be asked for your administrator password - this is what you usually enter when you run `sudo` commands. This will log you into the psql prompt as the user postgres.
- You should now have a prompt that looks like `postgres=#`. You can run SQL commands from here, which must end in semicolons.
- If you were not prompted for a default user or password, we will set one using psql. If you type `\du`, you can get a list of users associated with PostgreSQL. You should see a single user, `postgres`. In order to give this user a password, enter the following command: `ALTER ROLE postgres PASSWORD 'your-password-here';`, replacing "your-password-here" with whatever you want it to be. Remember that your password must be wrapped in quotes. *Don't forget the semicolon*.
- If successful, you will receive the feedback `ALTER ROLE`.

**If you are having issues with installation, please contact your instructor.**

#### MacOS

You should have already verified during the Node installation that you have Homebrew installed. Please see that section above for more details if not.

To install PostgreSQL, open your Terminal, and enter:
`brew update && brew install postgresql`

This will create a user for you, that matches your logged in user account. Run the `whoami` command in the terminal if you aren't sure what that is. This user has a blank password set as the default.

*You will need to run this command whenever you first start your computer and open up the terminal in order to start your Postgres server:*

`pg_ctl -D /usr/local/var/postgres/ -l /usr/local/var/postgres/server.log start`

Since that's rather verbose, we can set it as an alias!

`alias pgstart='pg_ctl -D /usr/local/var/postgres/ -l /usr/local/var/postgres/server.log start'`

However, aliases are temporary. You would need to set that alias each time you opened up a new terminal window. Instead, we can tell our system to always set that alias whenever a terminal is opened. Find your **.bashrc** or **.bash_profile** file - it will probably be in your home (~) directory. Run `code .bashrc` or `code .bash_profile` to open it up, then on a new line, paste this in:

`alias pgstart='pg_ctl -D /usr/local/var/postgres/ -l /usr/local/var/postgres/server.log start'`

Now, whenever you first start up your computer, you just have to run `pgstart` to get your Postgres server running.

If, for some reason, the `pgstart` command is not available when you open a new window, you should be able to run `source .bashrc` or `source .bash_profile` (wherever you put the alias), then `pgstart` should be available.

#### ALL USERS: Startup and Create some databases

1. Login to psql.
  - For Mac, run your new `pgstart` alias, then type `psql`.
    - If the response is, "Can't find database *yourUserName*", run `createdb -U yourUserName`, then run `psql` again.
  - For Windows, open up your psql program (SQL Shell)
  - For Linux, run `sudo -u postgres psql`
2. You should be at a prompt that looks like `postgres=#`
3. Enter the following command: `CREATE DATABASE kilovolt;`. *Note the semicolon. If you forget it, your prompt will go to a new line and look like* `postgres-#`. *This means you have an unterminated command and the prompt will just keep going to new lines until you enter a semicolon*.
  - You should receive the feedback "CREATE DATABASE".
4. Verify that your databases were created by running `\l` (no semicolon). You should see a list of databases, including `kilovolt`. You should be able to connect to a database by running `\c DATABASE_NAME`, e.g. `\c kilovolt`.

---

Congrats! You're all done. :wink:
