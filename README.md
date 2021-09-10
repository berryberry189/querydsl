# querydsl

### Variable Between Col1 and Col2 
ex)
```java
  private BooleanExpression checkBetween(LocalDate today){  
        return  Expressions.booleanOperation(Ops.BETWEEN,
                Expressions.constant(today), QClass.start, QClass.end);
    }
```
