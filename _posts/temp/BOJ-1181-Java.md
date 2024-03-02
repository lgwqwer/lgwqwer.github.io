# 백준 1181번 (단어 정렬)

**알파벳 소문자로 이루어진** 단어 N가 들어오면 조건에 맞게 정렬하는 프로그램 작성 


## 조건  
> 1. 길이가 짧은 것부터 정렬
> 2. 길이가 같다면 사전 순으로 정렬
> 3. 중복된 단어는 하나만 남기고 제거
> 4. 입력 최대 개수 2만개, 시간제한 2초

<br>

## 풀이 접근 과정

1. N개의 단어를 담을 배열 wordArr 선언 

2. 각각의 element에 대한 문자열의 길이를 담을 배열 lengthArr 선언 및 입력

3. lengthArr을 집합화하여 lengthSet 생성

4. lengthSet을 다시 List화 하여 lengthList 생성 및 sort

5. lengthList의 element와 같은 길이를 가진 단어들을 저장할 2차원 배열 wordArr2D 선언. (row: words, column: lengthSequence)

6. wordArr2D의 각 column들의 element들을 사전 순으로 sort

7. wordArr2D[0][0] ~ wordArr2D[x.length][y.length]를 출력 






