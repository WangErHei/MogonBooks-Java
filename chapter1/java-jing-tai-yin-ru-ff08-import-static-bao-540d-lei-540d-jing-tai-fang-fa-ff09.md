> #### Java中的静态引入，也就是 import static 引入的目标为方法，如图有两类：TestA和TestB

![](/assets/1.png)

> #### 这两个类中都有一个printTest静态方法

![](/assets/2.png)

![](/assets/3.png)

> #### 正常情况下，通过普通导入，也就是直接通过import，调用方法是需要类名.方法名，而通过import static静态引入时，调用方法可以直接调用方法名，如下图

![](/assets/4.png)

> #### 但是需要注意的一点，import static引用的是方法，此例中的TestA后面还有.\*,同理也可以直接引入对应的方法，如import static testSource.TestA.printTestA,如果pringTestA的方法是重载方法，也可以这样引入，调用的时候可以调用任何重载的方法。



