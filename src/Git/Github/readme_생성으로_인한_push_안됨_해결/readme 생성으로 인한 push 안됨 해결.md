# readme 생성으로 인한 push 안됨 해결

readme를 깃허브 리포지터리를 만들 때 생성하기를 체크하여 생성한 경우 puah가 안될 때가 있다.

그런 경우 git pull origin main --allow-unrelated-histories를 입력한 후, 푸시를 하면 푸시를 할 수 있다.

이렇게 해도 안되면 git pull origin main --allow-unrelated-histories --rebase도 입력해보면 된다.