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
    * 예) git add <file name>
* commit
* git reset HEAD <file> : stage된 파일을 unstaged로 변경
* git checkout -- <file> : stage되어 있는 파일을 수정한 후 수정 전으로 되돌림 
* branch : 여러 개발자들이 동시에 다양한 작업을 할 수 있도록 만든 기능으로, 각자 독립적인 저장소 안에서 소스코드를 변경하며 작업을 진행할 수 있음. 이렇게 분리된 작업 영역에서 변경되어 만들어진 브랜치는 다른 브랜치와 병합함으로써, 작업한 내용을 다시 새로운 하나의 브랜치를 만들 수 있음. 
    * 예) git branch : 브랜치 보기, git checkout -b testing: testing 브랜치 만들고 이동
* merge : merge는 분기했던 브랜치를 master브랜치와 합칠 때 사용
* status : 
* log : commit했던 로그 기록을 보여줄 때 사용
    * 예) git log --oneline --decorate --graph --all

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


### 강조
*single asterisks*    
_single underscores_    
**double asterisks**    
__double underscores__    
~~cancelline~~ 

### 링크

