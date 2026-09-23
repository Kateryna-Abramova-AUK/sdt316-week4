SDT 316

Homework 4 | Abramova Kateryna

Github link https://github.com/Kateryna-Abramova-AUK/sdt316-week4.git  

**Part 1**
<img width="1400" height="262" alt="image" src="https://github.com/user-attachments/assets/6ff6b5db-3e95-4811-99c0-35a5b30336c5" />
Here, on the left, we can see a graph with a merge on top.
The merge commit:  d90bcd3 (HEAD -> main, origin/main) Merge branch 'feature-merge'

It has two parents, from original branch (main) and added one for the merge (feature-merge), since in history we see both `main` and `feature-merge`.

We see that it forked after initial commit, because we dont have on line, instead it splits into 2 separate lines `main: update line 2` and `feature: update line 2`. Then it rejoins at the merge commit `d90bcd3`, where both branches joins to one and we see that one asterisk on top.

**Part 2**
SHA 1
<img width="1548" height="100" alt="image" src="https://github.com/user-attachments/assets/710a3f43-7691-4227-b875-a70ff9d55fdd" />
SHA 2
<img width="1102" height="100" alt="image" src="https://github.com/user-attachments/assets/bba0b90b-b583-4084-992b-3b57d73177a1" />
3 (after force oush)
<img width="1954" height="346" alt="image" src="https://github.com/user-attachments/assets/f0961c4c-cf24-471c-8042-558eb865df58" />
(fast foward)<img width="1014" height="196" alt="image" src="https://github.com/user-attachments/assets/818c30c8-9d0b-4728-a758-60502c509e51" />

_The SHA changed even though the file contents did not — why?_
Because it creates a new commit with a different parent commit, so even if content is the same,new parent made a commit so SHA itself is different.

_Why did GitHub reject the normal push?_
Because after the rebase, local branch history didnt match with remote (local one was changed and didnt macth remote), so Git prevented the push since it doesnt match. 
Actually, the system itself gives us the message that explains why it happened:
<img width="1688" height="302" alt="image" src="https://github.com/user-attachments/assets/46f6a5fe-abc9-42eb-a49c-a176ae4f1dc8" />

_How does this graph differ from Task 1's?_
We dont have merges here, just straight sequence of asterisks with no splits.

_And in one sentence: why is rebasing a branch a teammate has already pulled risky?_
Because it changes commit SHA and there may be differences between local history and rebased one.

**Part 3**
<img width="1032" height="530" alt="image" src="https://github.com/user-attachments/assets/d93ba620-5785-47ac-a37d-eabd4e315fd8" />
<img width="1270" height="1008" alt="image" src="https://github.com/user-attachments/assets/dc2757a3-ba83-478a-9b82-4a930edd290e" />
<img width="1556" height="558" alt="image" src="https://github.com/user-attachments/assets/1bf74f8a-fe14-406f-9663-14e8d56b9496" />

3.2
<img width="2478" height="646" alt="image" src="https://github.com/user-attachments/assets/5f718606-43ff-46d2-a1ca-921cfab84f4b" />
<img width="2542" height="1266" alt="image" src="https://github.com/user-attachments/assets/c9a76954-b991-47eb-8665-768ee339d1ac" />

3.3
What does each do to main's history? 
So we got 3 of them.
Create a merge commit - main get new merge commit with two parents + preserves indiviadual commits.
Squash and merge - combines all commits into one new commit so intermidediate commit history will be dropped into one.
Rebase and merge - adds the individual commits to the top of main without creating a merge commit

Two of these three shapes you have already built by hand — say which task produced which. 
Create and Rebase. In the part 1 - created a merge commint history, and in part 2 - rebase and merge history.

Which option would destroy the three commits you just curated, and why?
Squash and merge because as i mentioned it will drop all commits into 1, so instead 3 i will have a single one.

You removed two commits with fixup but kept three. What made those two disposable and these three worth preserving?
Because those two werent that valuable. Three i kept had important information like setting up,ect but removed ones had minor fixes, as for me it more what we consider valuabled and informative.

<img width="2062" height="572" alt="image" src="https://github.com/user-attachments/assets/0ef36a60-1854-4667-9bbe-11c4cd276df2" />

