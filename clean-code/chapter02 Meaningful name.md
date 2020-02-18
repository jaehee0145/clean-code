## 의도를 분명히 밝혀라  
`int d; // 경과 시간 (단위: 날짜)`  
이름 d는 아무 의미도 드러나지 않는다.

`int elapsedTimeInDays;`  
`int daysSinceCreation;`  
`int daysSinceModification;`  
의도가 드러나는 이름을 사용하면 코드 이해와 변경이 쉬워진다.

```java
public List<int[]> getThem() {
    List<int[]> list1 = new ArrayList<int[]>();
    for (int[] x : theList)
        if (x[0] == 4)
            list1.add(x);
    return list1;
}
```  
문제: 코드의 함축성
     단순한 코드지만 코드 맥락이 코드 자체에 명시적으로 드러나지 않는다.

```java
public List<Cell> getFlaggedCells() {
    List<Cell> flaggedCells = new ArrayList<Cell>();
    for (Cell cell : gameBoard)
        if (cell.isFlagged())
            flaggedCells.add(cell);
    return flaggedCells;
}
```
해결: 이름만 고쳤는데도 함수가 하는 일을 이해하기 쉬워졌다.


## 그릇된 정보를 피하라 
 - 널리 쓰이는 의미가 있는 단어를 다른 의미로 사용하지 말자
 - 여러 계정을 그룹으로 묶을 때, 실제 List가 아니라면 `accountList`라 명명하지 않는다. (실제 컨테이너가 List인 경우라도 컨테이너 유형을 이름에 넣지 않는 편이 바람직하다.)
 - 유사한 개념은 유사한 표기법을 사용한다. 일관성이 떨어지는 표기법은 그릇된 정보다.

 ## 의미 있게 구분하라
 - 명확한 관례가 없다면 구분하기 어렵다 
    moneyAmount vs money  
    customerIOnfo vs customer  
    accountData vs account  

## 발음하기 쉬운 이름을 사용하라 

## 검색하기 쉬운 이름을 사용하라
- 문자 하나를 사용하는 이름과 상수는 텍스트 코드에서 쉽게 눈에 띄지 않는다.  
`int WORK_DAYS_PER_WEEK = 5;`   
