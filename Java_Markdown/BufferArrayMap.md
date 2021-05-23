StringBuffer
>线程安全，可变的字符序列 从版本JDK 5开始，被StringBuilder 替代。 通常应该使用StringBuilder类，因为它支持所有相同的操 作，但它更快，因为它不执行同步


Vector
>从Java 2平台v1.2开始，该类改进了List接口，使其成为Java Collections Framework的成员。 与新的集 合实现不同， Vector被同步。 如果不需要线程安全的实现，建议使用ArrayList代替Vector


Hashtable
>该类实现了一个哈希表，它将键映射到值。 任何非null对象都可以用作键或者值 从Java 2平台v1.2开始，该类进行了改进，实现了Map接口，使其成为Java Collections Framework的成 员。 与新的集合实现不同， Hashtable被同步。 如果不需要线程安全的实现，建议使用HashMap代替 Hashtable