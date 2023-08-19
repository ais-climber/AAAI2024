# Submission 12181
## What do Hebbian Learners Learn?

### Installation Instructions

This directory contains the Lean code for our submission.  The actual proof code 
is contained in the file `proofs.lean`.  If you would like to run `proofs.lean`, 
you will need to install Lean 4 on your own machine (you can just read the source 
code, too, but Lean has interactive features). 

The easiest way to do this is to follow the instructions at
    https://leanprover.github.io/lean4/doc/quickstart.html

This guide walks you through installing Lean 4 by way of Visual Studio Code, the 
text editor and enviromnment we used to develop our code. This will install the 
most recent nightly release of Lean 4 (this may take a long time). 

Lean is in rapid development, but new versions should be backwards-compatible with 
older ones. We recommend using the version of Lean that is installed. We have 
checked that our code works with the 2023-03-17 and 2023-08-18 releases.


### System Details

We developed and ran this code on a personal laptop, i.e., a Dell XPS-15 with a 
20 × 12th Gen Intel Core i7 processor (5.0 GHz) and 32GB of RAM. But this is 
overkill — we recommend using a machine with at least a 1.6GHz processor and
4.0GB RAM.  Lean 4 and Visual Studio Code are available on all major plat-
forms (our code is platform-independent), but we developed in the Kubuntu 22.04 
operating system (with KDE Plasma version 5.24.7). We used Visual Studio Code 
version 1.77.3.


### Running and Reading our Lean Proofs

After you have successfully installed Lean 4, open ‘proofs.lean’ in Visual Studio 
Code. When Lean has finished loading the file (this may take a few minutes), you 
should see text buffer split into two. On the left is the source code, containing 
defnitions, theorems, proofs, and propositions. On the right you will see the Lean 
Infoview, which will output all messages, including errors, ‘printed’ `#eval` 
statements, and warnings (these can be found in the "All Messages" drop-down menu).

The Lean Infoview may also show the current context of a proof.  The included image
`infoview-before.png` shows an example of this. The proof on the left shows by 
induction that if there is a path from `u` to `v` in a graph, and a path from `v` 
to `w`, then there is a path from `u` to `w`. If we place our cursor on line 135, 
then on the right we see the context of the proof at line 135. This shows all 
variables `u`, `v`, `w`, `g` defined in scope, as well as any assumptions we’ve 
made so far `h1`, `h2`. Finally, `⊢ hasPath g u w` indicates that our goal at this
point is to prove that there is a path from `u` to `w`.

If we move our cursor to line 140 (shown in image `infoview-after.png`), the Lean 
Infoview tells us that there are no goals left. This means that the proof is done 
and  formally checked! Note that proofs that are not finished are easily 
spotted — the keyword `sorry` indicates a goal with no proof. (We intend to fill in 
all `sorry`’s by the AAAI-24 author feedback window.)