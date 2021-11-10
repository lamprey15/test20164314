##test20164314

---

(쉘 스크립트 관련) getopt 및 getopts 명령어

***
![getopts](https://user-images.githubusercontent.com/94046904/141101772-90c67ad7-dde5-4e11-b75e-b32c670cffe9.png)

쉘 스크립트에서 명령을 실행할 때 옵션을 사용합니다.

그때 실행 옵션을 구현을 하는 방법이 getopt 함수를 사용합니다.

또한 사용자와 개발자의 편하게 볼 수 있습니다.

사용은 while + getopts를 이용합니다.
 1) while getopts "abc" opt; do
 2) case $opt in
 3)  a) a option  
 4)  b) b option
 5)  c) c option을 줍니다
argument

![argument](https://user-images.githubusercontent.com/94046904/141102275-03837384-9f57-43bb-8968-ec7dd7009400.png)

while + getopts를 이용하면 사용할 수 있습니다.

위 코드에서 : 추가하면 됩니다.
1) while getopts "a:bc" opt; do
이렇게 추가를 하면됩니다.
- option : verbose mode
- :option: silent mode 지정하여 사용합니다.


a : verbose mode
- getopts 'a:'는 a 옵션에 콜론(:)을 추가해서 인자를 요구합니다.
그럼 인자가 없는 실행 option
- option만 정의합니다. 
- 1) while getopts "a:bc" opt; do
- "b" , "c"가 인자가 없어서 option만 설정하면 됩니다.

위에서 ":"를 통해서 인자를 설정하는데 기본적으로 getopt는 한개의 문자만을 구분하는데 ":"을 붙이게 되면

value가 추가된다는 의미를 표현합니다.

그 점은 유의하면서 사용해야 됩니다.

---

리눅스 명령어 sed 및 awk 명령어

***

sed 명령은 편집기 명령어로 생각하면 편합니다.

파일을 읽어와서 수정하고 출력한다고 생각하면 편합니다. vi편집기를 생각하면 연상하기 쉽습니다.

- sed 명령어은 vi 편집기처럼 실시간으로 편집은 안되며 sed 명령어 형태로 편집됩니다.
- 원본을 유지하면서 편집하기 때문에 sed명령어를 이용하면서 결과물을 만들어도 원본에 손상을 없습니다.
- 하지만 sed 명령어 -i option을 지정하면 원본을 바꾸게 됩니다.
- sed명령어는 저장 공간을 보유하고 있습니다. 패턴 버퍼, 홀드 버퍼

![sed](https://user-images.githubusercontent.com/94046904/141108123-ebd5260c-f764-482a-8a52-1c7a90f07440.png)

sed 명령어
- -n : 패턴 버퍼의 자동출력을 맞는 option
- -e : command를 가지고 파일을 가공합니다.
- - sed -n -e '1p' -e '4p'
- - 다중 command 사용
- -p : 특정 행을 출력
- - sed -n -e '/$/p' or sed -n -e '1,$p'
- - 전체 내용 출력
- - sed -n -e '1p'
- - 첫번재 줄 출력
- - sed -n -e '2,5p'
- - 시작점과 끝나는 점을 설정해서 출력
- - sed -n -e '8,$p'
- -  전체 내용 출력과 같은 내용으로 이것은 특정줄에서 마지막 줄까지 출력 그래서 '1,$p' 전체 내용 출력인것이다
- 특정 문자열 출력하는 명령어
- - ex) chosun을 출력할때 
- - sed -n -e '/c/p'
- -d : 특정 행 삭제
- - sed -n -e '3,6d' -e '1,$p'
- -a : 문자열 추가 아래에서 추가
- - sed -n -e '/bye/a\end' -e '1,$p'
- -i : 문자열 추가 이전 줄에 추가
- - sed -n -e '/bye/i\end' -e '1,$p'

***

명령어 awk

유닉스에서 개발된 스크립트 언어로 텍스트가 저장되어 있는 파일을 원하는 대로 필터링하거나 추가하는 기타 가공을 해서 행과 열을 출력하는 명령어

즉 데이터를 조작, 리포터 생성하는 명령어입니다.

![awk](https://user-images.githubusercontent.com/94046904/141108477-99f3b294-befa-4d2b-8f2c-3bbe700f012b.png)

awk명령어는 pettern, action을 입력합니다.

형식 :
- awk 'pettern' file
- awk '{action}' file
- awk 'pattern {action}' file




