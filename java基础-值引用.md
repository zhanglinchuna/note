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
最后打印出的结果是 3。
解释如下：
1. 在 main 方法中，我们创建了一个 ArrayList，并添加了三个元素（1, 2, 3）。
2. 然后调用 fun 方法，传入这个 list 作为参数。
3. 在 fun 方法中，list = new ArrayList<>() 这行代码创建了一个新的 ArrayList 对象，并将局部变量 list (fun方法中的list)指向这个新对象。这不会影响原始的 list(main方法中的list)。
4. fun 方法中对新 list 的操作（添加元素 4）不会影响原始的 list。
5. 当 fun 方法结束后，原始的 list 保持不变，仍然包含 3 个元素。
6. 因此，当执行 System.out.println(list.size()) 时，输出的是原始 list 的大小，即 3。

这个例子展示了 Java 中方法参数传递的特性：对于对象类型的参数，传递的是引用的副本。在方法内部重新赋值不会影响原始引用，但是通过引用修改对象的内容会影响原始对象。
