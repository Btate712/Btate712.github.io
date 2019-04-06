---
layout: post
title:      "My CLI Scraper Gem Project"
date:       2019-04-06 23:54:46 +0000
permalink:  my_cli_scraper_gem_project
---


I put the (preliminary) finishing touches on my CLI Scraper Gem Project today.  I had a lot more fun writing it than I expected to.  The project scrapes thegreatestbooks.org for the title, author, and synopsis for the top 10 best books and stores the data in an array of book objects.  The CLI displays all of the book titles and authors and prompts the user to select which book they would like more data on.  When the user selects a book, the book synopsis is displayed.  The user is then prompted for whether they would like even more information.  If the user selects "yes", the program performs a google search for the book's Wikipedia page, scrapes the first paragraph from that Wikipedia page, and displays that paragraph.

Writing the gem seemed like a big task at first, but by breaking the task down into a series of small problems and solving those problems one at a time I was able to move quickly through the development.  It was a great way to excercise many of the skills I've learned along the way as a FlatIron Student.  I'm looking forward to progressing further along with my FlatIron experience.
