---
layout: post
title:      "Debugging without pry"
date:       2017-12-14 18:41:50 +0000
permalink:  debugging_without_pry
---

It took me a while to really understand the use of pry.  So, I used to debug my codes using irb instead; and without knowing exactly what went wrong with tests, debugging process has been painstaking, and sometimes impossible.

Sometimes, the program would run as designed when played with CLI; but little tests would just keep failing.  For example, during the tictactoe AI project, although the program was functioning, I would get errors saying that the game doesn't allow player1 to play or doesn't run for few rounds.
Only after going through pry debugging process, I was able to figure out what the ruby was seeing after running each step of the tests and fix the problem.

Also for the scraping projects, without pry, it was impossible to figure out which line of css codes was not importing the correct line of data/string.  

While debugging is still not easy with pry, it is definitely much more difficult without it.  

