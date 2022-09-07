# Git
## Reset branch to older commit
This will delete commits up to a certain commit like they never existed

`git reset --hard <commit-id>`

In case you are hosting the code on an other origin you need to force push the new state to the origin

`git push origin +<branch-name>`
