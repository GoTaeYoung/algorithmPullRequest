문제 : 공통된 접두어(Prefix) 구하기
===============
접근법
---------------------------
첫번째 단어의 길이의 값 까지 반복문을 돌다가
현재 적용된 접두어가 들어있지 않은 단어가 검색되면
반복문을 종료하고 접두어의 길이를 출력한다
***

수도코드
------------------------------
```
공개된 클래스 test 시작

	main 메소드 시작

		접두어 추출할 단어들 : String 타입 배열 firstWordList 선언, 초기값 주입

		접두어 : String 타입 firstHeadWord 선언, 초기값 ""

		접두어 길이 : int 타입 firstHeadWordCount 선언, 초기값 0

		반복문 실행 여부 : boolean 타입 flag 선언, 초기값 true

		반복문 시작 - int 타입 j 를 1부터 firstWordList의 첫번째 단어 길이까지 1씩 증가

			임시변수 temp : firstWordList 의 첫번째 단어를 앞에서 j 개수 만큼 자른 값

			반복문 시작 - int 타입 i 를 1부터 firstWordList 배열의 길이 보다 작을동안 1씩 증가

				조건문 시작 - firstWordList 배열의 i 번째 위치에 있는 단어가 temp 로 시작하지 않는다면

					flag 의 값을 false

					반복문 종료

				조건문 끝

			반복문 끝
			
			조건문 시작 - flag 값이 false 일때

				반복문 중지

			조건문 끝

			firstHeadWordCount 의 값을 j

			firstHeadWord 의 값을 temp

		반복문 끝

		구해낸 접두어와 접두어 길이 출력

	main 메소드 종료

공개된 클래스 test 종료
```
***

코드 작성
------------------------------------
```
public class test {

	public static void main(String[] args) {

		String[] firstWordList = { "hojin", "hoo", "how" };

		String firstHeadWord = "";

		int firstHeadWordCount = 0;

		boolean flag = true;

		for (int j = 1; j <= firstWordList[0].length(); j++) {

			String temp = firstWordList[0].substring(0, j);

			for (int i = 1; i < firstWordList.length; i++) {

				if (!firstWordList[i].startsWith(temp)) {

					flag = false;

					break;

				}

			}

			if (!flag) {

				break;

			}

			firstHeadWordCount = j;

			firstHeadWord = temp;

		}

		System.out.println("firstHeadWord = " + firstHeadWord + ", firstHeadWordCount = " + firstHeadWordCount);

	}

}
```
***

예상되는 시간복잡도
----------------------------------
n = 배열의 길이

m = 배열의 첫번째 단어의 길이

시간복잡도 = O ( m * n )