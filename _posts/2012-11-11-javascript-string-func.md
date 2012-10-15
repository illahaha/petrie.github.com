---
layout: post  
title: "JavaScript中String类的函数"  
description: "JavaScript中String类的函数"  
category: JavaScript
tags: [JavaScript, String]  
---
## JavaScript中String类的函数 ##
- var s="hello,world";
- s.charAt(0)			//"h",第一个字符
- s.charAt(s.length-1)	//"d",最后一个字符
- s.substring(1,4)		//"ell":第2~4个字符
- s.slice(1,4)			//"ell":同上
- s.slice(-3)			//"ell":最后三个字符
- s.indexOf("l")			//2:字符l首次出现的位置
- s.lastIndexOf("l")		//10：字符l最后一次出现的位置
- s.indexOf("l",3)		//3:在位置3及之后首次出现字符l的位置
- s.split(", ")			//["hello", "world"]分割成子串
- s.replace("h","H")		//全字符替换
- s.toUpperCase()		//"HELLO,WORLD"

在JavaScript中字符串是固定不变的，类似replace和toUpperCase()的方法都返回新字符串，原字符本身并没有发生变化。