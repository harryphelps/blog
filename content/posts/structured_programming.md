---
title: "Octopus Book Club: Structured Programming"
date: 2021-10-08T14:26:38+01:00
draft: false
---

There are 3 programming paradigms:
1. Structured programming
2. Object orientated programming
3. Functional programming

> Structured programming imposes discipline on direct transfer of control.

Edsger Wybe Dijkstra is credited with the discovery that unrestrained `goto` statements are harmful to programming structure. His original aim was to apply the mathematical discipline of proof to programming, thereby giving programmers a suite of proven structures to string together.  Unrestricted `goto` statements prevented the programme from being divided into smaller and smaller units which is a requirement for reasonable mathematical proofs. 

Böhm and Jacopini had worked out years earlier that all programmes could be constructed from just three base structures of sequence, selection and iteration. Dijkstra deduced that the same three control structures could be always be subdivided into provable units, and so always be mathematically provable with the divide and conquer technique. By constructing programmes using only these three control structures _sequentially_ you can write absolutely correct, provable programmes. 

However, writing proofs for every thing is really long. Instead programming turned away from a mathematical approach and adopted a scientific one. In science you can’t prove something to be true, you can only disprove it. But if you do enough tests without disproving your hypothesis you can be sure that to a reasonable degree of confidence, your hypothesis is correct within the parameters of the tests you have carried out.

This is the programming approach we use today. Big programmes are made up of smaller falsifiable units all constructed from the three basic control structures that we know can be subdivided into mathematically provable units.  Whilst we don’t have time to mathematically prove everything we write, if we have enough test coverage we can be sure that our programme will work well in all reasonable scenarios so long as we have tested them.
