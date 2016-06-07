Git update forked repo
======================

처음은 9xd 그룹의 slack 에서 작동하고 있는 9xd-bot 에서 의도치 않은 무언가가 나와 그것을 수정하려고 시작했다.

fork하고 수정하고 pull request를 날리는것까지는 좋았는데

merge된것으로 업데이트 하기위해 찾게 되었다.

1. git remote add upstream <URL>

2. git fetch upstream

3. git checkout master

4. git rebase upstream/master