---
title:  "x == x returns false?!"
last_modified_at: 2019-02-14T11:45:00-01:00
---

When comparing variable, let's call it `x` to itself, the result should be `true`, right? Especially in Java, language that is well designed, and doesn't behave like JS (as you can see [here](https://www.destroyallsoftware.com/talks/wat)). Or isn't it?
Consider this snippet:

```java
@Test
public void testCompareWithItself(){
    double d = Double.NaN;
    assertFalse(d == d);
}
```

The test passes! How? Check [this thread](https://stackoverflow.com/questions/8819738/why-does-double-nan-double-nan-return-false) for more information.
