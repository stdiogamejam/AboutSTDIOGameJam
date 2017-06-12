# AboutSTDIOGameJam
Documents about the STDIO Game Jam, including rules &amp; guidelines.

# About

The STDIO Game Jam is a weekend-long hackathon to create a large set of small, fun, text-based games that beginner programmers can study. These games use only “standard io” text-streams for input and output, making for easy-to-understand source code that beginners can study. Every language and operating system supports stdio text, so running these games isn’t hindered by platform differences or frustrating framework installation processes.

# Upcoming Game Jam

The next STDIO Game Jam will take place the weekend of August 19th and 20th at the Museum of Art and Digital Entertainment, Oakland’s video game museum and globally through the Internet.
More info about this at: https://www.themade.org/stdio-game-jam-2017/

You do not have to be at the MADE in Oakland, CA to participate. Online contributers follow the same submission process as MADE attendees. You can also submit games after the game jam (see the Submission Process section).

Also, the STDIO Game Jam will be [streaming live from the museum on Twitch](https://www.twitch.tv/themadeoakland).

# Rules

The purpose of the game jam is produce a large compilation of varied, simple, text-based games and art programs whose source code beginner programmers can examine to learn from. The point system is set up to encourage this.

Submitted programs are **required** to:

* Be under 256 “significant lines of code”, as measured by [CLOC](http://cloc.sourceforge.net/).
* Only use stdio text streams (i.e. only print() and input() in Python). This means no graphics and programs can’t move the text cursor to X, Y coordinates on the screen. Keyboard input will block program execution until the player presses Enter. (e.g. Games can’t respond to single key presses like roguelikes do.)
* Use only the language’s standard library and not require installing additional frameworks, libraries, or modules.
* Ideally use UTF-8 for the source files, but only output characters compatible with the [Latin-1 (CP-1252) charset](https://en.wikipedia.org/wiki/Windows-1252) so programs can run on Windows. This means many accented characters are okay, but not unicode snowman.
* Be released under an open license, preferably [MIT License](https://en.wikipedia.org/wiki/MIT_License). (These games are to be used to help others create programming tutorials and courses,
including commercially.)
* Run on Linux, Mac, and Windows without modification.
* Include a file named readme.txt with the names (or handles) of each team member, with a short description (a few paragraphs at most) of the game. Put this file in only when the game is complete and ready to be judged.

Submitted programs are **encouraged** to:

* BE ORIGINAL! :D
* Have the game be runnable in a “Try [language]” website, such as [PythonAnywhere](https://www.pythonanywhere.com/), [TryRuby.org](http://tryruby.org/levels/1/challenges/0), or [Execute PERL Online](https://www.tutorialspoint.com/execute_perl_online.php).
* Fit into one file (except for “data files”).
* Have “data files” for, say, level data in plaintext and ideally JSON files. (Plaintext makes games more hackable for beginners.) Data files don’t count towards the 256 SLOC limit.
* Use a modern language that runs on Linux, Mac, and Windows.
* Be “well-commented” so that beginner programmers can understand them.
* Avoid advanced programming techniques like threads, reflection, self-modifying code, etc. Keep it simple.
* Use full names (e.g. “stringCompare” instead of “strcmp”).
* Follow a standard style guide, or at least have a consistent code style.
* Be reasonably bug free.
* Handle errors reasonably and not have empty `catch` blocks.
* Do reasonable input validation: don’t let the program crash just because the player entered the wrong kind of text.
* Have in-game “how to play” help screens as part of the program, rather than documented elsewhere.
* Assume the terminal is 80 x 25 characters.
* Remove any unused variables and functions before submitting.
* Not require an internet connection, or at least not rely on the player to set up a server.
* List in the source which license the game uses, rather than the full license text.

Points are awarded according to the following rubric:

* 1 point for each submitted program that meets the requirements.
* +2 for programs under 128 SLOC or +3 for under 64 SLOC, as measured by [CLOC](http://cloc.sourceforge.net/).
* +1 if the game is “well-commented”. (This is subjective, but in general maybe 1 useful comment for every 6 to 10 lines of code.) Comments won’t add to the SLOC count.
* +2 for original game mechanics. (This is subjective, but we want to encourage new programs, not just another rehash of “guess the number”.)
* +10 “Spotlight Award” for an exceptional game. This is awarded at most once per team. (This is subjective, see the “Ideas, Tips, and Best Practices” for details.)
* +2 points to other teams for refactoring this program.

Further, teams can get two points for refactoring other teams’ code or providing bug fixes. The refactoring must be more than just style changes and the original team must accept the PR. A team can only get two points per game they refactor, no matter how many PRs are accepted.

It is considered completely fair game for teams to reimplement other teams’ game ideas, especially to port it to a different programming language. However, these games won’t be eligible for the +2 original game mechanic or +10 Spotlight Award points. Please credit the original team in the source code.

But of course, the objective of the game jam is to produce a large compilation of readable programs for beginners to learn from and try to create for themselves. This is truly more valuable than points.


# Submission Process

Both game jam attendees and online participants first must sign up for a (free) GitHub account and clone this git repo on their GitHub account: https://github.com/stdiogamejam/2017STDIOGameJam

Add your game using the following folder layout in the repo:

/[team_name]/[game_name]/[your_program.py]
/[team_name]/[game_name]/readme.txt
/[team_name]/[game_name]/refactors.txt

Submissions are made on the master branch (this is the default branch). Game jam staff can help attendees with git. [GitHub also has a short tutorial.](https://try.github.io/levels/1/challenges/1) You won’t need to know anything about branching and merging to submit.

The [team_name] should be the GitHub username that will make pull requests against the STDIOGameJam repo, regardless of what the team calls itself or who is in it.

The [game_name] should contain a readme.txt file when it is ready to be judged. Judges will add an X-points.txt file where X is the number of points it was given and contain any notes. Judges will be awarding points throughout the game jam, not just at the end. You may appeal the points awarded if you feel they were tallied incorrectly.

The folder can also have a refactors.txt listing teams that contributed accepted Pull Requests for refactoring the code or bug fixes. These teams will be awarded two points.

Look at the sample programs under the asweigart folder for examples.

# Ideas

The wiki for this repo has an ideas page where game jam attendees can find (and add) ideas for games to make: https://github.com/stdiogamejam/AboutSTDIOGameJam/wiki/Ideas

Working with only stdio text introduces several constraints:

* Programs have no graphics beyond ASCII-art.
* The text cursor cannot be moved back up or to arbitrary XY coordinates on the screen.
* Programs are necessarily turn-based, waiting on the player to finish typing and press Enter.
* Programs are single-threaded.

But these constraints can also drive creativity. Text streams might be old-school, but your game design can be completely modern: if you can create a text-version of Portal 2, go for it!

There will be a board with post-its at the game jam where attendees can help each other with tips and best practices they’ve discovered, such as:

* Remember: There’s plenty of types of games you can make with just text besides Zork-style text adventure games.
* If the player must enter coordinates, display an ascii-art board with coordinate numbers running along the four sides.
* Try to make games based on simple game mechanics, rather than spending time on scripted stories or elaborate level design.
* Present numbered menu items so players don’t have to type full commands in.
* Let players enter multiple moves at once. For example, instead of redrawing a maze after each move, let the player type “uurd” to move up, up, right, and down in one go.
* Make input short and case-insensitive.
* You can create cool ASCII-art text with Figlet
* Making two-player games is probably easier than making computer AI opponents.
* (This list will be updated during the game jam as new ideas come up.)

# Spotlight Award

The 10-point “Spotlight Award” is given to games that have game mechanics that are simple, original, and compelling. The prime example of this is Hamurabi [sic] from David Ahl’s Basic Computer Games book. Hamurabi is a bare bones city management game with mechanics that connect three resources: population, grain, and land. The three resources have simple interactions but create an original and compelling game that became a classic:

* Grain is used to maintain the population and prevent starvation.
* Growing grain requires a balance of both land and population for best efficiency.
* Land can be bought or sold with grain at a price that randomly fluctuated each turn.
* Population slowly grows each turn with a random number of immigrants.
* Rare, random plagues cut the population in half. Rats randomly eat grain stores.
* The player can’t let more than 45% of the population starve in one turn.
* The goal is to have as large of a population as possible at the end of 10 turns.
* The game had random elements but didn’t rely on luck, avoided straight-forwarded strategy (as in rock-paper-scissors), and had a playtime of a few minutes. Repeated plays allowed the player to figure out how the mechanics worked and form new strategies. This is ideally what a “Spotlight Award” game would have.

# Game Program Compilation Book

[The MADE is a 501c3 nonprofit](https://themade.org/what-are-we) and will be producing a book compilation of the games made at the game jam. The book will be freely available online under a [Creative Commons license](https://creativecommons.org/licenses/by-nc-sa/4.0/), while copies are also sold for the benefit of the museum.
