## 词法结构 ##
- JavaScript程序是用Unicode字符集编写的。Unicode是ASCII和Latin-1的超集，并支持地球上几乎所有的语言。
- JavaScript中除了数字，字符串，布尔值，null和undefined之外的就是对象了。数组是特殊的对象。
- JavaScript五个核心类：Array，Function，RegExp，Date，Error。
- 从技术上讲，只有JavaScript对象才能拥有方法。然而，数字，字符串和布尔值也可以拥有自己的方法。在JavaScript中，只有null和undefined是无法拥有方法的值。
- JavaScript采用UTF-16编码的Unicode字符集，JavaScript字符串是由一组无符号的16位值组成的序列。
- JavaScript定义的格式字符串操作方法均作用于17位值，而非字符，而不会对代理项做单独处理，同样JavaScript不会对字符串做标准化的加工，甚至不能保证字符串是合法的UTF-16格式。