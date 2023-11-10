# selab-how-to-git

***

# 1. GitHub ?
> 소프트웨어 개발 프로젝트를 위한 소스코드 관리 서비스
+ 기능
    * 소스 코드 열람
    * 간단한 버그 관리
    * sns 기능 (개발자 이력서의 용도로 활용되기도 함)

+ 중요성
    *  큰 규모의 프로젝트나 더 복잡한 문제들에 일할 수 있는 능력을 제공 

<br><br><br>

# 2. GitHub 기본 개념

## 1. commit
>커밋(commit) 은  파일을 추가하거나 변경 내용을 저장소에 저장하는 작업

* commit  방법은 다음을 참고
    * [commit 방법](#35-git-commit)

## 2. push
>푸시(push) 는 파일을 추가하거나 변경 내용을 원격 저장소에 업로드 하는 작업
* 원격 저장소?
    * [정의](#3-repositories)

<br>

    👍 작은 작업 단위로 commit
    👍 작업이 어느정도 일단락 했을때 push


## 3. repositories
> 파일이나 디렉초리를 저장하는 저장소를 뜻하며, 자신의 컴퓨터에 있는 "로컬 저장소" 와 서버에 있는 "원격저장소" 가 있다

## 4. branch
> 독립적인 개발 라인으로 작업 분리를 할 수 있다. 따라서 기존 작업의 훼손없이 미리 실행해볼 수 있다.

<br><br><br>

# 3. GitHub 사용법
* 기본적인 작업흐름
    1. GitHub에 저장소 작성 (git init)  또는 복제(git clone)
         > `1번 작업은 처음에 한번만하면 된다`
    2. 파일 작성, 편집
    3. 파일 생성/ 변경/ 삭제를 git 인덱스에 추가 (git add)
    4. 변경 결과를 로컬 저장소에 커밋(git commit)
    5. 로컬저장소를 푸시하여 원격 저장소에 반영(git push)
         > `2번~5번 작업을 반복하여 수행하며 사용한다`

<br>

## (GitBush 사용시)
### 3.1 repository 생성
* 초록색 *new*를 클릭한다. 
>  ![repository생성(2)](https://github.com/BINNNNNY/test/assets/102966279/6e9828e3-469d-40d6-a14a-dc0b1fa6e76f.png)

* *Repository name* 을 정하고 공개범위를 설정한다.
>  ![repository생성(3)](https://github.com/BINNNNNY/test/assets/102966279/5c490f58-afe8-4e66-92aa-307bd2307ead.png)

* repository가 생성되면 다음과 같이 가이드 코멘드와 repository의url을 확인할 수 있다.
>  ![[Alt text](repository생성(1)](https://github.com/BINNNNNY/test/assets/102966279/706376e8-fe84-4272-bbbc-ea2e4a93a6b7.png)

### 3.2 git init (로컬 저장소 새로 만들기)
* 명령 프롬프트로 자신의 프로젝트 폴더 위치로 이동
>   ```gitignore
>      $ mkdir "폴더 이름"  /// 폴더생성
>      $ cd "폴더 이름"     /// 폴더로 이동
>      $ git init          /// (.git 파일 생성) Repository 생성
>   ```

>  ![git_init_screenshot](https://github.com/BINNNNNY/test/assets/102966279/f1e6e694-f06e-47b4-86ba-fb4b7c1dbee2.png)

### 3.3 git clone (원격저장소 복제하여 로컬저장소로 가져오기)

>   ```gitignore
>      $ git clone [REPO_URL] [DIR]
>   ```
* [REPO_URL]에는 복제할 저장소의 주소를 ,  [DIR]에는 복제할 위치를 지정한다.

* 원격저장소 주소는 GitHub 프로젝트 화면에 들어가서 오른쪽 상단
`Code` 버튼을 눌러 확인가능하다
    >  ![project_screenshot](https://github.com/BINNNNNY/test/assets/102966279/f5570cfb-ae4a-400d-bf64-2b3c57d7ddc4.png)

### 3.4 git add(인덱스에 추가)
* 저장소에 커밋하기 전 변경내용을 임시로 저장하는 위치를 "인덱스"라 한다. 인덱스에 생성/ 수정된 파일을 추가한다. 
>   ```gitignore
>      git add 파일명 
>      git add . // 전체 내용 추가
>      git add *.txt // 모든 txt 파일 업로드
>      git add project/app/*/ //디렉토리 업로드
>      git add --update // 현재 git이 추적하고 있는 파일들만 add

### 3.5 git commit
* 의미 있는 변화를 뜻하는 "버전"을 기록하는 것을 git commit이라 하고 작업이 완결된 상태여야 한다.
>   ```gitignore
>   git commit -m "커밋메세지를 이곳에 작성" 
* -s => 개발자의 싸인
* -m => 커밋메시지를 작성
* -a => 커밋을 하기 전에 자동으로 모든 파일을 등록하는 과정을 미리 수행함

### 3.6 git push
* GitHub repository에 파일을 업로드하는 것을 말한다.
>   ```gitignore
>   $ git push origin(원격저장소) main(브랜치이름)
