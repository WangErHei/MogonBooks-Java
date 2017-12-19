> #### 在Object类中的equals\(\)方法：

```java
public boolean equals(Object obj) {
    return (this == obj);
}
```

> #### 很明显的看出他就是用==来比较对象所占空间的地址，而我们所说的==是比较地址，equals\(\)是比较值，这种说发在严格意义上讲是不对的，equals\(\)比较值，是基于很多类根据自己的一些需要来重写Object中的equals\(\)方法，例如String中的equals\(\)：

```java
public boolean equals(Object anObject) {
    if (this == anObject) {
        return true;
    }
    if (anObject instanceof String) {
        String anotherString = (String) anObject;
        int n = value.length;
        if (n == anotherString.value.length) {
            char v1[] = value;
            char v2[] = anotherString.value;
            int i = 0;
            while (n-- != 0) {
                if (v1[i] != v2[i])
                    return false;
                i++;
            }
            return true;
        }
    }
    return false;
}
```



