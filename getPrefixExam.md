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

		���ξ� ���� ���ϴ� �޼ҵ��, �Էµ� �ܾ���� ���ξ� ���� ���ϰ� ���

	main �޼ҵ� ����

	���ξ� ���� ���ϴ� �޼ҵ� ����

		���ξ� ������ �ܾ�� : String �迭 ����, �ʱⰪ ����

		���ξ� : String ����, �ʱⰪ ""

		���ξ� ���� : int ����, �ʱⰪ 0

		�ݺ��� ���� ���� : boolean ����, �ʱⰪ true

		�ݺ��� ���� - int �� 1����, �迭�� ù��° �ܾ� ���̱��� 1�� ����

			�ӽú��� : �迭�� ù��° �ܾ �տ��� int �� ��ŭ �߶� ����

			�ݺ��� ���� - int �� 1����, �迭�� ���� ���� �������� 1�� ����

				���ǹ� ���� - �迭�� int ��° ��ġ�� �ִ� �ܾ �ӽú����� �������� �ʴ´ٸ�

					�ݺ��� ���� ������ ���� false

					�ݺ��� ����

				���ǹ� ��

			�ݺ��� ��
			
			���ǹ� ���� - �ݺ��� ���� ���� ���� false �϶�

				�ݺ��� ����

			���ǹ� ��

			���ξ� ������ ���� j

			���ξ��� ���� temp

		�ݺ��� ��

		���س� ���ξ� ���

		���س� ���ξ� ���� ��ȯ

	���ξ� ���� ���ϴ� �޼ҵ� ����

������ Ŭ���� test ����
```
***

�ڵ� �ۼ�
------------------------------------
```
public class test {

	public static void main(String[] args) {

		System.out.println("wordPrefixCnt = " + Solve(args));

	}

	public static int Solve(String[] args) {

		String[] wordArray = args;

		String wordPrefix = "";

		int wordPrefixCnt = 0;

		boolean flag = true;

		for (int j = 1; j <= wordArray[0].length(); j++) {

			String temp = wordArray[0].substring(0, j);

			for (int i = 1; i < wordArray.length; i++) {

				if (!wordArray[i].startsWith(temp)) {

					flag = false;

					break;

				}

			}

			if (!flag) {

				break;

			}

			wordPrefixCnt = j;

			wordPrefix = temp;

		}

		System.out.println("wordPrefix = " + wordPrefix);

		return wordPrefixCnt;

	}

}
```
***

����Ǵ� �ð����⵵
----------------------------------
n = �迭�� ����

m = �迭�� ù��° �ܾ��� ����

�ð����⵵ = O ( m * n )