���� : ����� ���ξ�(Prefix) ���ϱ�
===============
���ٹ�
---------------------------
ù��° �ܾ��� ������ �� ���� �ݺ����� ���ٰ�
���� ����� ���ξ ������� ���� �ܾ �˻��Ǹ�
�ݺ����� �����ϰ� ���ξ��� ���̸� ����Ѵ�
***

�����ڵ�
------------------------------
```
������ Ŭ���� test ����

	main �޼ҵ� ����

		���ξ� ������ �ܾ�� : String Ÿ�� �迭 firstWordList ����, �ʱⰪ ����

		���ξ� : String Ÿ�� firstHeadWord ����, �ʱⰪ ""

		���ξ� ���� : int Ÿ�� firstHeadWordCount ����, �ʱⰪ 0

		�ݺ��� ���� ���� : boolean Ÿ�� flag ����, �ʱⰪ true

		�ݺ��� ���� - int Ÿ�� j �� 1���� firstWordList�� ù��° �ܾ� ���̱��� 1�� ����

			�ӽú��� temp : firstWordList �� ù��° �ܾ �տ��� j ���� ��ŭ �ڸ� ��

			�ݺ��� ���� - int Ÿ�� i �� 1���� firstWordList �迭�� ���� ���� �������� 1�� ����

				���ǹ� ���� - firstWordList �迭�� i ��° ��ġ�� �ִ� �ܾ temp �� �������� �ʴ´ٸ�

					flag �� ���� false

					�ݺ��� ����

				���ǹ� ��

			�ݺ��� ��
			
			���ǹ� ���� - flag ���� false �϶�

				�ݺ��� ����

			���ǹ� ��

			firstHeadWordCount �� ���� j

			firstHeadWord �� ���� temp

		�ݺ��� ��

		���س� ���ξ�� ���ξ� ���� ���

	main �޼ҵ� ����

������ Ŭ���� test ����
```
***

�ڵ� �ۼ�
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

����Ǵ� �ð����⵵
----------------------------------
n = �迭�� ����

m = �迭�� ù��° �ܾ��� ����

�ð����⵵ = O ( m * n )