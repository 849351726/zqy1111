# 计181  赵擎宇 2018310731
## 实验四 字符串实验

### 一、实验目的
掌握字符串String及其方法的使用
掌握异常处理结构
### 二、实验要求
内容：利用已学的字符串处理知识编程完成《长恨歌》古诗的整理对齐工作，写出功能函数，并运行。达到如下功能：
#### 1.每7个汉字加入一个标点符号，奇数时加“，”，偶数时加“。”
#### 2.允许提供输入参数，统计古诗中某个字或词出现的次数
#### 3.考虑操作中可能出现的异常，在程序中设计异常处理程序
输入：汉皇重色思倾国御宇多年求不得杨家有女初长成养在深闺人未识天生丽质难自弃一朝选在君王侧回眸一笑百媚生六宫粉黛无颜色春寒赐浴华清池温泉水滑洗凝脂侍儿扶起娇无力始是新承恩泽时云鬓花颜金步摇芙蓉帐暖度春宵春宵苦短日高起从此君王不早朝承欢侍宴无闲暇春从春游夜专夜后宫佳丽三千人三千宠爱在一身金屋妆成娇侍夜玉楼宴罢醉和春姊妹弟兄皆列士可怜光采生门户遂令天下父母心不重生男重生女骊宫高处入青云仙乐风飘处处闻缓歌慢舞凝丝竹尽日君王看不足渔阳鼙鼓动地来惊破霓裳羽衣曲九重城阙烟尘生千乘万骑西南行
### 三、实验过程
#### 1.输入文本，将文本转化为string格式。
#### 2.将string改为stringbuffer计算出字符串长度。
#### 3.建立循环每隔7个字加入“，”，14个字加入“。”。
#### 4.接收输入的字符并统计出该字符出现的次数，若为空格或符号则报错。
### 四、流程图
![image](https://github.com/849351726/zqy1111/blob/master/123.jpg)
### 五、核心代码
#### 1.加入标点符号
int all=a.length();
	  for(int i=all;i>0;i-=7) {
		if(i%14==0) {
			a.insert(i,'。');
			a.insert(i+1, '\n');
		}
		else a.insert(i, ',');
	}
#### 2.统计次数和报错
Scanner sc=new Scanner(System.in);
System.out.println("请输入要查找的字符：");{
char ch=sc.next().charAt(0);
if(sc.equals("+")||sc.equals("-")||sc.equals("*")||sc.equals("/")) {
	throw new wrong("不能输入符号");}
else if(sc.equals(" ")) {
	throw new wrong("不能输入空值");
}
sc.close();

int j,sum=0;

for(j=0;j < str.length();j++) {
	if(str.charAt(j)==ch)
		++sum;
}
System.out.print( ch+ "出现的次数"+sum+"次");
}
### 六、运行截图
![image](https://github.com/849351726/zqy1111/blob/master/1573988451(1).png)
### 七、实验心得






