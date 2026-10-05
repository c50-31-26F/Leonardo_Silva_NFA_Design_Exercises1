# NFA Design Exercises

This repository contains my JFLAP NFA designs for Problems 6, 7, 8, 9, and 12 from the N/DFA/RE Design exercises.

# Learning summary

Problem 8 gave me the most trouble because the NFA must remember both the required beginning `01` and the required ending `10`. Problem 12 also required careful counting because the accepting state cannot have a transition on `1`; otherwise strings with four or more `1`s could be accepted.

I used JFLAP's multiple-run feature to test the strings. I also used step-by-step mode for Problems 8, 9, and 12 to understand how multiple possible state paths can exist at the same time.

The most surprising strings were `01010` for Problem 8, `1101` for Problem 9, and `10101` for Problem 12. These strings show why an NFA may keep several possible paths and why a path that reaches an accepting state is not enough unless the entire input has been consumed.

In future work, I will write the language condition first, list the required states, and test the shortest strings and boundary cases before testing longer strings. I will also check the transitions after every symbol instead of assuming that only one path exists.
