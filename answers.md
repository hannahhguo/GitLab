# Quiz questions

This is only a "quiz" in the loosest sense that it's asking questions whose
answers will be part of your grade. Please use *any resources you want*, as
long as you list those resources (e.g. peers, websites, etc.)

## Navigating logs

1. What is the SHA for the last commit made by Prof. Xanda on the branch
xanda_0000_movie_processing?
(For this and future questions, the first 5 characters is plenty - neither
Git nor I need the whole SHA.)
9b2571f

2. What is the SHA for the last commit associated with line 9 of this file?
d1d8331

3. What did line 12 of this file say in commit d1d83?
"I should really finish writing this."

4. What changed between commit e474c and 82045?
added int() around x["Gross"] in line 18 & changed 5 to 6 in line 20


Sources for "Making things a little messier"
Q3: 
- https://www.educative.io/answers/what-are-keyword-arguments-in-python#
Q5:
- https://www.atlassian.com/git/tutorials/using-branches/git-merge


## Predicting merges

Assume at the start of each of these three questions that your
branch for switching to a top-10 list was called `top_ten`
and your branch generalizing to any number of movies was called `top_N`.
Predict the behavior of these three possible operations - you don't
have to provide a full `diff` but you should describe at a high level
what changes would happen.

These questions are supposed to be separate paths, not cumulative;
for example, you should *not* assume that the operations of 5 were run
before 6. When testing outcomes later in the lab, you should make sure to
revert back to the state of the branch before you started these questions.

5. What do you think would happen if you ran the following commands?
What branches would change, and how?
```
git checkout test
git merge top_N
```
git would merge the branches test & top_N to become one branch; top_N I think would become obsolete (i.e. merges into test). 

6. What do you think would happen if you ran the following commands?
What branches would change, and how?
```
git checkout top_ten
git merge test
```
git would merge the branches test & top_ten to become one branch; test would become the obsolete branch (i.e. merges into top_ten).


7. What do you think would happen if you ran the following commands?
What branches would change, and how?
```
git checkout test
git rebase top_ten
git rebase top_N
```
I think the branches of top_ten and top_N will attempt to get merged into test (one at a time), but there will be a merge conflict which will need to be resolved. 