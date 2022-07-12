### 代码示例

```java
public class Example {
    public static void main(String[] args) {
        List<Integer> list = new ArrayList<>();
        list.add(1);
        list.add(2);
        list.add(3);
        fun(list);
        System.out.println(list.size());
    }

    public static void fun(List<Integer> list) {
        list = new ArrayList<>();
        list.add(4);
    }
}
```
