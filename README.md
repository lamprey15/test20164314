##test20164314

---

(쉘 스크립트 관련) getopt 및 getopts 명령어

***
![getopts](https://user-images.githubusercontent.com/94046904/141101772-90c67ad7-dde5-4e11-b75e-b32c670cffe9.png)

쉘 스크립트에서 명령을 실행할 때 옵션을 사용합니다.

그때 실행 옵션을 구현을 하는 방법이 getopt 함수를 사용합니다.

사용은 while + getopts를 이용합니다.
 * while getopts "abc" opt; do
 *  case $opt in
 *  a) a option
 *  b) b option
 *  c) c option을 줍니다
argument 
