# N으로 표현

```javascript
function solution(N, number) {
    let nearestNumber = '';
    let nCount = 1;
    
    do {
        nearestNumber = nearestNumber + N;
    } while (parseInt(nearestNumber + N, 10) <= number * N);
    
    nCount += nearestNumber.length;
    nCount += (number * N - parseInt(nearestNumber, 10)) / N;
    
    return nCount > 8 ? -1 : nCount;
}
```

1. N과 number가 주어지면 N으로 만들어지는 수에서 N으로 나누고 number가 나올 때 N의 최소 개수를 구하는 문제
2. N + N (문자열)로 N * number 보다 작을 때까지 구한 후
3. N * number - (N + N )(숫자) / N의 값을 구한다.
4. 그럼 N의 개수와 3번의 개수를 합하고 마지막에 나눌 N을 합치면 최소 개수가 나온다고 생각하는데...
5. 2개 맞았네?

