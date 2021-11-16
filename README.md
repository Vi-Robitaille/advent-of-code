# Advent of Code

This is an autogen for an advent of code project. We all want to just sit back and focus on actually writing the code, so this auto builds a directory structure, clones over template files, and pulls the input.

What you need to do
- Populate ```secrets/.cookie``` and ```secrets/.twilio``` following the template put there.
- Put your own templates in ```templates```. Any name is fine, any directory structure is fine.
- put these in a crontab. If you're on windows... well... **sucks to suck**.

advent-init.py
-----

Creates folder structure for your project, if it is December before the 26th (basically a valid advent day) it creates all the missing files for your project as follows.

- Copies the templates in template/ to ```source/{year}/{day}/part1.py``` and ```source/{year}/{day}/part2.py```
- Pulls the input from advent of code for that day.

There are optional cli args if you wanna test stuff or for wtv.
- ```-y``` Specify the year to pull and create for.
- ```-d``` Specify the day, this is the last day it will itterate to.
  - Ex: ```python3 advent-init.py -y 2020 -d 15``` will pull and create the structure for 2020, from the 1st to the 15th.
- ```-s``` Specify a non default path for your source. (Default: ```./source/```)
- ```-v``` Verbose mode. (Warning: very loud)
- ```-i``` Check if paths are alright before proceeding.

annoy.py
-----
This texts you if you havent started, or havent completed today's challenge yet. Get cracking.