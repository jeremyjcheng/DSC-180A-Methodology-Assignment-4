---
layout: default
title: DSC 180A Methodology Assignment 4
---

**Name** Jeremy Cheng<br />
**UCSD email** jec061@ucsd.edu<br />
**Section** D21<br />
**Mentor** Armin Schwartzman

**What is the most interesting topic covered in your domain this quarter?**  
I was most interested in how language models handle corrections in long records. In our Quarter 1 project, a finance office could change a budget, cancel an earlier update, or cancel that cancellation and restore the original. Even when the arithmetic was simple, the model still had to figure out which budget updates counted.

**Describe a potential investigation you would like to pursue for your Quarter 2 Project.**  
I’d like to test whether giving a model only the relevant records helps it handle corrections in a long log. I would use our synthetic log generator to move a correction closer to or farther from the update it refers to, while keeping the correct budget the same. Then I would compare final-budget accuracy on the full log versus a shorter set of retrieved records, and check how often retrieval misses a record needed to answer correctly.

**What is a potential change you’d make to the approach taken in your current Quarter 1 Project?**  
I would ask the model to return the IDs of the budget updates it counted along with its final answer. Right now we use the final number to infer which mistakes might have happened. Comparing those IDs with the answer key would separate wrong-update mistakes from arithmetic mistakes.

**What other techniques would you be interested in using in your project?**  
I’d like to compare keyword search with retrieval based on text similarity. I’d also use record IDs to follow links between an update and its corrections. For example, if the search finds a cancellation, the system could also pull in the update it cancels so the model sees both records together.
