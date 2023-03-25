# 2023_OSS
## 2023 OSS 수업 

-----
### 3주차 git

### 이미지
![한국항공대학교 로고](../img/kau.png "한국항공대학교")


### 링크   
[LMS](https://lms.kau.ac.kr "항공대학교 강의관리시스템")

#### ProGit 링크
[ProGit](https://git-scm.com/book/ko/v2 "git 문서, 한국어")


##### 주요 git 명령어
* add : 파일을 추적 대상으로 포함시킬 때, 또는 커밋 대상으로 포함시킬 때 사용
    * 예) git add <file name>, git add .
* commit
* git reset HEAD <file> : stage된 파일을 unstaged로 변경
* git checkout -- <file> : stage되어 있는 파일을 수정한 후 수정 전으로 되돌림 
* branch : 여러 개발자들이 동시에 다양한 작업을 할 수 있도록 만든 기능으로, 각자 독립적인 저장소 안에서 소스코드를 변경하며 작업을 진행할 수 있음. 이렇게 분리된 작업 영역에서 변경되어 만들어진 브랜치는 다른 브랜치와 병합함으로써, 작업한 내용을 다시 새로운 하나의 브랜치를 만들 수 있음. 
    * 예) git branch : 브랜치 보기, git checkout -b testing: testing 브랜치 만들고 이동
* merge : merge는 분기했던 브랜치를 master브랜치와 합칠 때 사용
* status : 소스의 관리 대상 상태를 나타냄.
    * 예) git status 
* log : commit했던 로그 기록을 보여줄 때 사용
    * 예) git log --oneline --decorate --graph --all
* rm : tracked 상태의 파일을 삭제
    * 예) git rm <file name>
* mv <변경 할 파일 이름> <변경 될 파일 이름> : 파일이름을 변경할 때 사용
    * 예) git mv test3.txt test4.txt



------
### 2주차 숙제

```bash
#!/usr/bin/env bash
echo "----------"
echo "name :"

echo

echo "----------"
echo "student id :"


file_path=`find /home/kau2/ -name w2_homework.txt 2> /dev/null`
echo "----------"
echo
echo "file path :"
echo $file_path
echo

line_num=`wc -l $file_path | cut -c 1 -`
사용법: git config [<옵션>]

설정 파일 위치
    --global              공통 설정 파일을 사용합니다
    --system              시스템 설정 파일을 사용합니다
    --local               저장소 설정 파일을 사용합니다
    -f, --file <파일>     지정한 설정 파일을 사용합니다
    --blob <블롭-id>      지정한 블롭 오브젝트에서 설정을 읽습니다

동작
    --get                 값을 가져옵니다: <이름> [<값-정규식>]
    --get-all             모든 값을 가져옵니다: <키> [<값-정규식>]
    --get-regexp          정규식에 대한 값을 가져옵니다: <이름-정규식> [<값-정규식>]
    --get-urlmatch        <URL>에 특정되는 값을 가져옵니다: <섹션>[.<변수>] <URL>
    --replace-all         해당하는 변수를 모두 제거합니다: <이름> <값> [<값-정규식>]
    --add                 새 변수를 추가합니다: <이름> <값>
    --unset               변수를 제거합니다: <이름> [<값-정규식>]
    --unset-all           해당하는 항목을 모두 제거합니다: <이름> [<값-정규 식>]
    --rename-section      섹션의 이름을 바꿉니다: <옛-이름> <새-이름>
    --remove-section      섹션을 제거합니다: <이름>
    -l, --list            전체 목록을 표시합니다
    -e, --edit            편집기를 엽니다
    --get-color           설정한 색을 찾습니다: slot [<기본값>]
    --get-colorbool       색 설정을 찾습니다: slot [<표준출력이-TTY인지-여부>]

값 종류
    --bool                값이 "true" 또는 "false"입니다
    --int                 값이 십진수입니다
    --bool-or-int         값이 --bool 또는 --int입니다
    --path                값이 경로(파일 또는 디렉터리 이름)입니다
    --expiry-date         값이 만료 시각입니다

기타
    -z, --null            값을 NUL 바이트로 끝냅니다
    --name-only           변수 이름만 표시합니다
    --includes            찾아볼 때 include 지시어를 고려합니다
    --show-origin         설정의 출처를 표시합니다 (파일, 표준 입력, 블롭,  명령행)
echo "----------"
echo "line number :"
echo $line_num
echo

echo "----------"
echo "lask line :"
tail -n 1 $file_path
```

## 마크다운
### 목록
#### 번호 있는 목록 : 내림차순 정렬
1. 첫번째
3. 세번째
2. 두번째

#### 번호 없는 목록 : *, -, +
* 첫번째
- 세번째
+ 두번째
-----
* 빨강
  * 녹색
    * 파랑


### 코드블럭 
1. 마크다운에서 ```을 사용하여 코드블록을 사용할 수 있음
    예) ```python
        print ("hello world")
        ```


### 강조
*single asterisks*    
_single underscores_    
**double asterisks**    
__double underscores__    
~~cancelline~~ 


### 링크
#### 외부 링크 (External Link)
* 인라인 링크 : [링크](http://example.com" 링크 제목")
* 참조 링크 : [링크1][1] & [1]: http://example1.com/ "링크제목1"
* URL 링크 : <example.com/> & <example@example.com>

#### 내부 링크 (Internal Link)
* 내부 링크 : [링크](#id) 


### 이미지
* 이미지 삽입 : `![이미지 이름](이미지 주소)`
    *예) !(markdown_logo)(https://raw.github.com/dcurtis/markdown-mark/master/png/208x128.png)


