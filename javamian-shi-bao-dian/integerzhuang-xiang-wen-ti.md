```java
public class Demo {
    public static void main(String[] args) {
        Integer a = 100, b = 100, c = 200, d = 200;
        System.out.println(a == b);
        System.out.println(c == d);
    }
}
```

> #### 对于将int赋值给Integer，会直自动用Integer下的valueOf\(\);方法，属于自动装箱过程，而valueOf\(\);中是这样写的：

```java
public static Integer valueOf(int i) {
	if (i >= IntegerCache.low && i <= IntegerCache.high)
		return IntegerCache.cache[i + (-IntegerCache.low)];
	return new Integer(i);
}
```



