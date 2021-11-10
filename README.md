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
