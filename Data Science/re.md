정규표현식을 활용할 때 사용하는 라이브러리
import re
(1)match, search로 패턴 찾기
re.match('Hello', 'Hello, world!') 
출력: <re.Match object; span=(0, 5), match='Hello'> (맨 처음에 있는 hello의 위치가 span에 나옴)
re.search('Hello', 'Hello, world!') 
출력: <re.Match object; span=(0, 5), match='Hello'> (match와 동일함)
(2)정규표현식
숫자를 [0-9]
영어소문자 [a-z]
영어대문자 [A-Z]
한글 [가-힣]
자음 모음 [ㄱ-ㅎ] [ㅏ-ㅣ]
^ not 표현으로 제외하고 전부다 라는 것
+, * : 0개 이상 또는 1개 이상의 패턴을 모두 찾는 것!
re.search('[0-9]','1231243134123,asdfasdf!@3121')
출력: <re.Match object; span=(0, 1), match='1'>
+가 없어서 맨 앞에 있는 숫자만 인식함
re.search('[0-9]+','1231243134123,asdfasdf!@3121')
출력: <re.Match object; span=(0, 13), match='1231243134123'> 
+라서 연속된 걸 전부 찾는데, 맨 처음부터 13번째까지가 숫자라서 span이 13까지
re.search('[가-힣]+','12345/홍길동/asdfa@naver.com/010-111-1111')
출력: <re.Match object; span=(6, 9), match='홍길동'>
search니까 중간에 있어도 당연히 찾을 수 있다

