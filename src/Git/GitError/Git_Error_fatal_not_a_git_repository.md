깃허브에 있는 코드를 가져다 인텔리제이에서 프로그램을 만들다보니 New Project로 프로젝트를 만드는 일은 1달만이었던 것 같다. 그렇게 아무 생각없이 깃허브와 프로젝트를 연결시키고 보니 이게 웬걸

```git
fatal: not a git repository (or any of the parent directories): .git
```

이라는 오류가 나면서 안되는 것이 아닌가...

그래서 바로 구글링을 하여 찾아본 결과...
```git
git init
```
을 안해주면 나타나는 아주 기초적인 걸 안하면 나오는 오류였다.

push를 해주기 전에 git init을 해주니 문제없이 push가 이루어졌다.

이 일로 얻은 교훈은! 꼭 git init를 해야 한다는 것이다.

> 참고 문헌:
https://velog.io/@yoon_han0/fatal-not-a-git-repository-or-any-of-the-parent-directories-.git