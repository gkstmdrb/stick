# stick

### 문제
![image](https://github.com/gkstmdrb/stick/assets/114748816/22e96c34-2427-45d2-a38c-b9ff883ed0a0)
<br>

### 분석
이 문제는 막대기의 봉우리 수를 세야하기 때문에 막대기의 높이가 같거나 낮으면 count하지 않는다.
<br><br>
### 설계
1. 사용자로부터 배열의 크기 n을 입력받는다.
2. 크기가 n인 정수 배열 arr을 선언한다.
3. 사용자로부터 n개의 정수를 입력받아 배열 arr에 한다.
4. 배열 arr의 마지막 index 번호부터 0번째까지 내려오면서 가장 큰 숫자를 갱신하며 <br>
현재 가장 큰 값과 작거나 동일하다면 count하지 않고, 보다 더 크다면 count하여 1을 더한다.
<br><br>
### 구현
``` java
import java.util.Scanner;
import java.util.Stack;
public class Main {
	public static void main(String[] args) {
		
		Scanner sc = new Scanner(System.in);
		int i;
		int j=0;
		int n = sc.nextInt();
		int count=0;
		int height=0;
		
		
		int []arr = new int[n];
		        
		for(i=0; i<n; i++) {
			arr[i] = sc.nextInt();
		}
		
		i = n-1;
		
		while(i!= -1) {
			if(arr[i] > height) {
				height = arr[i];
				i--;
				count++;
			} else {
				i--;
			}
		}
		System.out.println(count);
	}	
}
```

### 결과
![image](https://github.com/gkstmdrb/stick/assets/114748816/be897e9d-1204-4cf7-a1cb-63705247bcbe)
<br><br>
![image](https://github.com/gkstmdrb/stick/assets/114748816/3a3f16da-2bb9-45a0-a1cc-fb92183b099c)

