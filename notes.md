##Notes##

**Update our Ubuntu VM**
 - sudo apt update
 - sudo apt -y upgrade
**To exit the VM, type the exit command**
 - Typing *exit* at the prompt will always close our connection to our remote servers.
**Basic Commands**
 - list files and directories.................. ls
 - print name of current/working directory..... pwd
 - create a new directory...................... mkdir
 - remove or delete an empty directory......... rmdir
 - change directory............................ cd
 - create an empty file........................ touch
 - print characters to output.................. echo
 - display contents of a text file............. cat
 - copy a file or directory.................... cp
 - move or rename a file or directory.......... mv
 - remove or delete a file or directory........ rm
**Nano**
 - The most common text editor on many Linux systems is nano. The nano text editor is a user-friendly command line text editor. The friendliest thing about nano is that it is modeless. It means that nano can be used to enter and manipulate text without modes, like insert mode or command mode. It is also friendly because, like many graphical text editors and software, it uses control keys to perform its operations.
 - The tricky part to learning nano is that the control keys are assigned to different keystroke combinations than what many graphical editors (or word processors) use by convention today.
   - Instead of Ctrl-c or Cmd-c to copy text, in nano you press the M-6 key (press Alt, Cmd, or Esc key and 6) to copy. To paste, press Ctrl-u instead of the more common Ctrl-v. Fortunately, nano lists the shortcuts at the bottom of the screen.
   - The carat mark is shorthand for the keyboard's Control (Ctrl) key. To perform the Save As operation on a file, we write out the file by pressing Ctrl-o (although Ctrl-s will work). The M- key is important. Depending on your keyboard configuration, it may correspond to your Alt, Cmd, or Esc keys. To search for text, you press ^W or Ctrl and W; that is, Ctrl-W (lowercase w will work). Press M-6 to copy a line. Press Ctrl-U to paste.
   - We start nano simply by typing nano on the command line. This will open a new, unsaved file with no content. Alternatively, we can start nano by specifying a file name after typing nano.
     - For example, if I want to open a file called example.txt, then I type the following command: nano example.txt
       - If the file doesn't exist, this will create it. If it does exist, then the command will open it.
 - One of the other tricky things about nano is that the menu bar (really just a crib sheet, so to speak) is at the bottom of the screen instead of at the top, which is where we are mostly accustomed to finding it these days. Also, the nano program does not provide pop up dialog boxes. Instead, all messages from nano, like what to name a file when we save it, appear at the bottom of the screen.
 - Lastly, nano also uses distinct terminology for some of its functions. The most important function to remember is the Write Out function, which means to save.
   - Some quick tips:
       - nano file.txt will open and display the file named file.txt.
       - nano by itself will open to an empty page.
       - Save a file by pressing Ctrl-o.
       - Quit and save by pressing Ctrl-x.
       - Be sure to follow the prompts at the bottom of the screen.
 - You can configure nano to look and behave in certain ways, too.
   - Create a file called .nanorc in your home directory:
       - *nano ~/.nanorc*
   - You can read about how to make such settings in the man page for the nano configuration file:
       - *man nanorc*
**README.md**
 - Markdown is a simple markup language for formatting plain text, which can later be rendered as HTML or even as a PDF, DOCX, etc. It's a very popular markup language in tech industries, and it's easy to get started.
   - Create headings using the pound # symbol before your text. The number of pound # symbols indicates the level of the heading. Heading level 1 indicates the main heading and so forth.
   - Bold: To make text bold, wrap it in double asterisks or double underscores:
       - For example, **bold** or __bold__.
   - Italic: To italicize text, wrap it in single asterisks or single underscores:
       - For example, *italic* or _italic_.
   - Unordered Lists: Use asterisks, plus signs, or hyphens to create bullet point lists.
       - Use indentation to create sub-items in a list.
   - Ordered Lists: Use numbers followed by periods for an ordered list.
   - Links: To create a named link, wrap the link text in brackets [ ], and then wrap the URL in parentheses ( ).
       - For example, [GitHub](https://github.com) will be GitHub.
       - Add a link title: [GitHub](https://github.com "GitHub Code Repo").
       - Use reference-style links: [GitHub][github]. Then refer to the full URL elsewhere in the document. For example, I usually add the reference at the end: [github]:https://github.com.
   - Images: Similar to links, but start with an exclamation mark, followed by the alt text in brackets, and the URL in parentheses.
       - For example, ![Alt text](image-url.jpg).
       - In this example, the file image-url.jpg must be in the same directory as the Markdown file. It's good practice to organize project files. In this case, I would suggest creating an images directory in the project home and storing images there, with good, descriptive names. Then use a relative path to link to the image: ![Alt text](images/image-url.jpg) where images/ is the directory name and image-url.jpg is the image file name.
   - Inline Code: Use a single backtick to wrap your code in text.
       - For example: `inline code`.
   - Code Blocks: For larger sections of code, use three backticks or indent with four spaces.
   - To create a blockquote, use the greater than symbol > at the beginning of a line. For nested blockquotes, use multiple > symbols.
       > This is a blockquote.
       >> This is a nested blockquote.
   - Create a horizontal line or rule by using three or more asterisks, dashes, or underscores on a new line.
   - Whitespace and Line Breaks: In Markdown, paragraphs are automatically created when text is separated by an empty line. To create a new line without starting a new paragraph, end a line with two or more spaces.
   - Escaping Markdown: To display a Markdown character, precede it with a backslash (\). For example, \*demo italicizing\*.
---

##Notes 2##

 - The grep command is one of my most often used commands. The purpose of grep is to "print lines that match patterns" (see man grep). In other words, it searches text, and it's super powerful.
 - Grep works line by line. So when we use it to search a file for a string of text, it will return the whole line that matches the string. This line by line idea is part of the history of Unix-like operating systems, and it's important to remember that most utilities and programs that we use on the command line are line oriented.
 - **Be aware that, by default, grep is case-sensitive, which means a search for the string chrome, with a lower case c, returns no results.**
 - Grep can do inverse searching. That is, we can search for lines that do not match our string using the -v option. Options can often be combined for additional functionality. We can combine -v to inverse search with -i to ignore the case.

 - To use the package manager, we will need the sudo command. The sudo command allows us to execute a command as another user (see man sudo). By default, the sudo command executes a command as the superuser (see man 8 sudo).
 - When necessary, we use sudo by prepending it to the regular commands that we have already learned. In our home directories, for example, we don't need to use sudo to create a new directory with the mkdir command. Instead we type something like mkdir data to create a new directory/folder called data. But our regular user doesn't own the files or directories outside our home directory.
 - The sudo apt update command updates that list and compares what's available to what's installed. That is, if you have a piece of software called acme1.1 on your system, and acme1.2 is available, then running sudo apt update will let you know that you can upgrade to acme1.2. It's good practice to run sudo apt update before installing or upgrading your system. This lets your system upgrade to the most recent version of what you want to install.
 - Once the list of packages has been updated, you can upgrade with the sudo apt upgrade command if there are any upgrades. When you run this command, and if there are any upgrades, you will be prompted to proceed. You can press Y to proceed, or N to cancel.

**In order to remove a package, we use the sudo apt remove command.**
 - sudo apt update
 - sudo apt upgrade
 - apt search
 - apt show
 - sudo apt install
 - sudo apt --purge remove
 - sudo apt autoremove
 - sudo apt clean
**To locate and install software:**
 - sudo apt update
 - apt search <package_name>
 - apt show <package_name>
 - sudo apt install <package_name>
**To remove software and purge related files:**
 - sudo apt --purge remove <package_name>
 - sudo apt autoremove
 - sudo apt clean
**To keep system up to date:**
 - sudo apt update
 - sudo apt upgrade
 - sudo apt autoremove
 - sudo apt clean

 - The yaz-client is an information retrieval client that uses the Z39.50/SRU protocols to query bibliographic databases, like library catalogs and repositories. For those unfamiliar, Z39.50 is a standard protocol in libraries for sharing, querying, and retrieving bibliographic information between library databases. Its development in the 1970s pre-dates the web, and its continued use illustrates the evolution of information retrieval systems since the 1970s. The protocol is maintained by the Library of Congress.
Z39.50 is often presented as an abstract information retrieval concept even though it has played a central part of searching online catalogs and databases for nearly 50 years. The protocol, using tools like yaz, can be used to build search interfaces to bibliographic data.
