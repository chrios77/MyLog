# Github Flow② Github push에 제약 걸기

## Github Flow② Github push에 제약 걸기
Github Flow는 기존에 하던 것처럼 메인 브랜치에 바로 로컬에 저장소 만들고 커밋, 푸시하는 것이 아니라 로컬에 브랜치를 새로 만들고 이 새로 만든 브랜치에서 작업을 한다.
즉, 메인 브랜치에 직접 커밋 금지, 무조건 PULL REQUEST 에 의해서 작업해야 한다.

### 방법①
깃허브에 레포지터리를 생성한 후, settings 클릭

### 방법②
Gerenal 칸에 Brancshes 클릭

### 방법③
Add branch protection rule 클릭

### 방법④
Branch name pattern 란에 main 입력

### 방법⑤
Require a pull request before merging 체크 => Require approvals 체크 해제

->Require approvals는 PR를 통과시키기 위해 다른 한 명의 투표를 받는 것이다. 근데 체크 해제를 해주는 이유는 혼자 진행할 것이기 때문이다. 만약 여럿이서 진행하면 체크 해제를 안하면 된다.

### 방법⑥
하단에 Create 버튼 클릭 => 깃허브 비밀번호 입력 => Branch protection rules가 나온다.

### 마무리
이제 이 레포지터리에 바로 push를 하지 못한다. 