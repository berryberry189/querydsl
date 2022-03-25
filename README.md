# querydsl

### Variable Between Col1 and Col2 
ex)
```java
  private BooleanExpression checkBetween(LocalDate today){  
        return  Expressions.booleanOperation(Ops.BETWEEN,
                Expressions.constant(today), QClass.start, QClass.end);
    }
```

### 날짜 사이의 기간(일) 구하기
ex)
```java
  NumberTemplate<BigInteger> dateNumberTemplate = Expressions.numberTemplate
        (BigInteger.class, "datediff({0}, {1})", startDateTime, endDateTime);
```
