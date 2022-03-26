# querydsl

### Variable Between Col1 and Col2 
ex)
```java
  private BooleanExpression checkBetween(LocalDate today){  
        return  Expressions.booleanOperation(Ops.BETWEEN,
                Expressions.constant(today), QClass.start, QClass.end);
    }
```

### 날짜(LocalDateTime) 사이의 기간(일) 구하기
ex)
```java
  NumberTemplate<BigInteger> dateNumberTemplate = Expressions.numberTemplate(
        BigInteger.class, "datediff({0}, {1})", startDateTime, endDateTime);
```

### 날짜(LocalDateTime) 숫자로 변환
ex)
```java
  NumberTemplate<Long> nowLongNumberTemplate = Expressions.numberTemplate(
        Long.class, "UNIX_TIMESTAMP({0})", LocalDateTime.now());
```
