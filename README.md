# CogSite

Content for the Website of Cognitive Science Students at Aarhus University.

## ANNOUNCEMENTS
A1: Added TODO tasks - refer to those to choose a random task you want to take up 

**WORK IN PROGRESS**

You can host the site locally by running the HostSiteLocally.Rmd, after what, you can 
edit the website's content and see all changes made dynamically. Additionally, you 
can download `hugo-extended` with `choco install hugo-extended` if you have 
`chocolatey` downloaded. Then it's possible to use `hugo server` in the root 
folder and the website is hosted on port 1313 (by default).

## Current state

The technical elements are basically finished. The basic architecture is ready.

Some sub-pages under "reinforced learning" and "the data frame" still needs to 
be created but beyond that, they are mostly created (from the CogSite SideStruktur document)

## How to build the site locally

1. Clone this reposititory, `git clone git@github.com:AUcogseers/CogSite.git`
2. In the newly cloned folder (`cd CogSite`), download the theme with `git submodule update --init --recursive`
3. Install the blogdown package in R: `install.packages("blogdown")`
4. Download the hugo files from within R with `blogdown::install_hugo()`
5. Build the webpages in R with `blogdown::build_site()`
6. Optionally, host a local webserver with `blogdown::serve_site()` and take it back down with `servr::daemon_stop(1)`

### Structure

[THIS IS DEPRECATED, SEE THE "COGSCI SIDESTRUKTUR" DOCUMENT]

## TO DO

A lot of the current goals are oriented around content:

- [ ] Write a nice front page
- [ ] Rewrite the structure of the online courses list
 - Categories on the right side
 - 2 lines for each course [hyperlink title] ([publisher]) -> [description]
- [ ] Reinforced learning front page: Introduction and massive lists of resources
- [ ] Remove the Attention Spotlight and replace with the Blog (keep the neural network calendar)
- [ ] Move book market and AU environment to Social System
- [ ] Create a level 1 called formal stuff
- [ ] The data frame (Library) is for old data things
- [ ] University courses list under formal stuff
- [ ] Add the Study Café
- [ ] Set up the blog structure (categories, tags, etc.)
- [ ] Simplify simplify simplify on the left side - remove third level and reduce reduce
- [ ] Create designs for the page (e.g banner images on the front page or in the neural network page)
- [ ] Write the markdown tutorial
- [ ] Write the github tutorial for contributing to the website
- [ ] Specificize the contribution pages so it's _very easy_ to contribute
- [ ] The Time of Content is Upon Us
- [ ] Write all the teachers: Favorite books etc.
- [ ] Embedding the calendar
- [x] Decide a good file structure for the Amazing Lists Of Everything
- [x] Implement one list as a prototype
- [x] Implement the hugo-book theme
- [x] Implement a basic hierarchical structure
- [ ] Write an example blog post in the "posts" folder
- [x] Write instructions on shortcodes
- [x] Write instructions on writing a blog post
- [x] Write instructions on page settings
- [x] Merge the esben branch and delete esben branch
- [x] Write a sample list in the list of everything (online courses list)

## Links and possible implementations

- [x] Initial collection of R packages: https://docs.google.com/spreadsheets/d/10a2JWhNXYrrt1N-kNr0LB8fGvKwHcWhf6VdUBz8wCCE/edit#gid=0
- [ ] The IV-fag list from Anna Stuckert (LINK)
- [x] Online courses lists from Esben Kran (LINK)
- [ ] YouTube video list by Peter (LNK)
- [ ] Data Elixir (EPIIC)
