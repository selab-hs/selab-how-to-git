# selab-how-to-git

***
>Index
## 1. GitHub ?
> 소프트웨어 개발 프로젝트를 위한 소스코드 관리 서비스
+ 기능
    * 소스 코드 열람
    * 간단한 버그 관리
    * sns 기능 (개발자 이력서의 용도로 활용되기도 함)

+ 중요성
    *  큰 규모의 프로젝트나 더 복잡한 문제들에 일할 수 있는 능력을 제공

<br><br><br>

## 2. GitHub 기본 개념

### 1. commit
>커밋(commit) 은  파일을 추가하거나 변경 내용을 저장소에 저장하는 작업

* commit  방법은 다음을 참고
    * [commit 방법](###3.4_git_commit)

### 2. push
>푸시(push) 는 파일을 추가하거나 변경 내용을 원격 저장소에 업로드 하는 작업
* 원격 저장소?
    * [정의](###3._repositories)

<br>

    👍 작은 작업 단위로 commit
    👍 작업이 어느정도 일단락 했을때 push


### 3. repositories
> 파일이나 디렉초리를 저장하는 저장소를 뜻하며, 자신의 컴퓨터에 있는 "로컬 저장소" 와 서버에 있는 "원격저장소" 가 있다

### 4. branch
> 독립적인 개발 라인으로 작업 분리를 할 수 있다. 따라서 기존 작업의 훼손없이 미리 실행해볼 수 있다.

<br><br><br>

## 3. GitHub 사용법
* 기본적인 작업흐름
    1. GitHub에 저장소 작성 (git init)  또는 복제(git clone)
         > `1번 작업은 처음에 한번만하면 된다`
    2. 파일 작성, 편집
    3. 파일 생성/ 변경/ 삭제를 git 인덱스에 추가 (git add)
    4. 변경 결과를 로컬 저장소에 커밋(git commit)
    5. 로컬저장소를 푸시하여 원격 저장소에 반영(git push)
         > `2번~5번 작업을 반복하여 수행하며 사용한다`

<br>

### 3.1 git init (로컬 저장소 새로 만들기)
* 명령 프롬프트로 자신의 프로젝트 폴더 위치로 이동
>   ```gitignore
>      $ mkdir "폴더 이름"  /// 폴더생성
>      $ cd "폴더 이름"     /// 폴더로 이동
>      $ git init          /// (.git 파일 생성) Repository 생성
>   ```


### 3.2 git clone (원격저장소 복제하여 로컬저장소로 가져오기)

>   ```gitignore
>      $ git clone [REPO_URL] [DIR]
>   ```
* [REPO_URL]에는 복제할 저장소의 주소를 ,  [DIR]에는 복제할 위치를 지정한다.

* 원격저장소 주소는 GitHub 프로젝트 화면에 들어가서 오른쪽 상단
`Code` 버튼을 눌러 확인가능하다
    >  ![Alt text](https://github.com/selab-hs/selab-how-to-git/assets/102966279/37d0fe2e-549a-47ba-8b40-1eb56ef5ce58.png)

### 3.3 git add(인덱스에 추가)
* 저장소에 커밋하기 전 변경내용을 임시로 저장하는 위치를 "인덱스"라 한다. 인덱스에 생성/ 수정된 파일을 추가한다. 
>   ```gitignore
>      git add 파일명 
>      git add . // 전체 내용 추가
>      git add *.txt // 모든 txt 파일 업로드
>      git add project/app/*/ //디렉토리 업로드
>      git add --update // 현재 git이 추적하고 있는 파일들만 add

### 3.4 git commit
