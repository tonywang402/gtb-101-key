## web编程训练营的气

**培训和学校学习的不同**：学以致用，解决实际的问题，不但能够做出方案而且能够最终落地

**培训的目标**：能够对应简单的需求，创建满足需求，合乎质量要求的软件

**测试用例规则**

1. 不是通过测试的用例数目来衡量，而是以功能点的测试是否通过来衡量
2. 根据学院repository来评分，以teacher repository来评价需求的正确性
3. 如果import了未引用的package导致语法错误的，总分扣1分
   - 如果引入没有用的package不会报错，但是不建议



#### 沟通和反馈

- 及早沟通
- 在沟通时说出自己的观点，而非单纯的发问
- 通过复述来澄清



#### **技术场景**

1. 简单需求

   > 将任务根据逻辑进行拆分 :yellow_heart:

   及时澄清需求

   - 需求有问题，必须有文档作为佐证，或者能够从文档中进行推断
   - 需求问题往往由于 程序细节 造成的，如果程序细节能够完成，那就不是需求问题

2. 程序逻辑

   > 自顶向下：将一个大需求，按照逻辑拆分成小需求，需求可以先用人话写出来   :heart:  :cake: 
   >
   > 先主后次：需求里面先完成主需求，保证跑通，再完成次需求 :yellow_heart:

   > 简单需求是否要拆分  :dancer:
   >
   > 完整的理解需求，而不是为了过测试
   >
   > 最后要捋一遍测试，看是否真的通过

   1. 写出想要什么，输入是什么，以及函数名字，也就是短逻辑，先不考虑实现  :heart:  :cake: :cactus:
   2. 用Alt+shift+enter创建函数   :heart:  :cake: 

   > 严格实现需求

   - 需求只有完成和未完成两个状态，没有通过测试就是没有完成
   - 要完成文档中交待的功能
   - 可以查看方法的描述Ctrl+Q来判读此方法能否满足需要的功能 ​ ​ :yellow_heart:

3. 写成程序

   > 针对小块功能，严格按照输入和返回来写   :yellow_heart:

4. 调试bug

   > 需要使用工具调试并观测中间过程。为了在调试中找到问题，必须能够首先阅读代码，并预测执行的结果

   - 设置断点debug调试  :gift_heart:
   - 使用idea给的建议   :heart:  :cake: :cactus:



#### **规则和细节**

需要保证输出的稳定性，就要一定的规则和习惯

1. 开发中的规则

- 代码格式

  - 先全选，使用Ctrl+Alt+L进行格式化  :heart:
  - 运算符周围必须有空格，if()和for中()不需要空格  :heart:
  - 开始和结束不要用空行  :heart:  :cake: :cactus:
  - 逻辑块之间要有空行，大的逻辑块可以加入空行  :heart:
  - JS中函数名和()之间要有空格 :heart:
  - 代码超过屏幕的一半就要考虑换行 ::heart:
  - 注意缩进 :heart:

 - 代码质量：

   - Java使用Alibaba的代码格式检查插件  :yellow_heart: :green_heart:

   - JavaScript的格式参考repository中的lint设置 

     > 拿到一个仓库，要先cnpm install，使用shift+.进行quick fix  :heart:

   - JavaScript要加入disable eslint语句  :heart:

    - 不得遗留调试代码或者代码的注释  ::heart:   :cake:   

    - 及时运行测试，随时check代码静态分析的结果

   - 所有intellij中合理的警告都应该引起重视  :heart:

   - 所有ESLINT中合理警告也应该引起重视   :heart:

- 命名

  - 正确的英文单词 :heart:
  - 不要缩写，要用全称 :heart:
  - 不能拼音 :heart:
  - 应该具体  :yellow_heart:  :green_heart:

- **逻辑**

  - 解决方案中存在无效的逻辑或者变量
  - 在循环中重复执行每一次循环都会得到相同结果的代码
  - 不能存在冗余的逻辑或者雷同的实现
  - 函数命名与函数内容不符或者方法包含命名中之外的功能

 - **Git小步提交代码**

   - 提交的功能点是否单一 :提交有没有问题 :walking:
   - commit message和文件是否匹配  :heart:

 - **语义化commit message**

   - 尤其是注意前缀是否得当
     - refactor 用来描述不修改功能前提下，优化代码  :heart:
   - 必须用英文，而且信息不要太详细，动词加名词就行 :heart:  :cake:
   - 必须包含姓名



2. 开发中程序细节

   **通用**

   - 代码嵌套不能超过三层 :heart:

   - for循环中的if 用continue防止多层嵌套   :heart:

   - 不要使用否定的函数逻辑

   - 不要重写JDK和JS中原生的方法

   - 不要使用标记为obsolete的方法或函数

   - 不要对简单问题使用复杂方法

   - 不能大部分使用public，这会疯狂暴露可见性

   - 表示逻辑或时，建议使用 ||， 不要使用 |，因为||有短路运算 ​ ​ :heart: :cake:

   - 表示逻辑与时。建议使用&&， &&具有短路运算    :heart:

     

   **变量与常量**

   -    - 对于对象引用的变量声明，也应该使用final声明    :heart:
        - 变量声明为接口，不要声明具体的类型，hashmap建议用Map arrayList应该用list，方便以后的扩展 :heart:
   -    对于直接出现的数字，没有明确意义，叫做magic number，要用final type声明为常量 :heart::heart:  :cake:
   -    不会改变的变量，包括可能会改变，但是在自己作用域里面不变的话，都要用final或const声明为常量 :heart:  :cake:

   -    对于重复的常量初始化是否可以抽出静态常量的field  :question:
   -    变量声明之处应该尽可能贴近使用它的地方  :heart:
        - 变量是不要有冗余的初始化
        - 对于变量声明之后，如果简单操作，就可以用 `Arrays.asList()`  :question:
   -    在field的标准下，如果将primitive变量用作常量，要使用final或者static final	

   

   **数字和字符串**

      - 不能使用==比较double或者float的值 ，更不能去检测字符串 :heart:
      - == 与 ===区别：:heart_eyes:
      - 
      - 判断字符串是否既不是""也不是null​ ​  ​  :heart:

   ```java
   if (text == null || "".equals(text)) 
   ```

      - 大量循环的字符串拼接应使用**StringBuilder** 或者 **String.format** 
      - 同样重复在string上使用**replace**也属于这种情况
      - 如果没有同步要求，不要使用**stringbuffer**
   - 迭代字符串不需要将其转化为数组  :grey_question:
   - 格式化指定宽度的字符串 :heart:  :cake:  
     - JavaScript   padEnd()方法
     - Java             “-” + width + “s”

   

   **数组和集合**

      - 集合选择合适
      - 而且使用方法要正确
      - 创建一个空数组 :heart:  :cake:
        - String[]  result = {};
        - String[] result = new String[0];
        - Collections.emptyList();

   

   **stream**

      - stream处理过程中不应存在无效的termination
      - 对用使用stream解决的map、filter、reduce等问题就不要使用传统的循环
   - 对于应当使用optional的场景，就不要使用null推断

   

   **异常处理**   :heart_eyes:

   - JS抛出异常 throw new Error("");  





##### 快捷键

- Java
  - Ctrl + \                        快速多行注释
  - Shift + F6                    批量修改变量名
  - Alt + shift + enter      使用idea建议
  - Ctrl + B                       访问方法
  - Ctrl + Q                      渲染注释
  - Ctrl + Alt + L              格式化
  - 长按 Ctrl + Shift + F  全文搜索
- shift +  F10                 运行刚才的测试 :heart:
  - Ctrl + Alt + m             抽取方法  :heart:
  
- JavaScript

  - Ctrl + ？                单行快速注释

  - Ctrl + F2                批量修改变量名  :heart:
  - shift + .                  quick fix   :heart:
  - Ctrl + 方向键         在单词之间移动  :heart:
  - shift + 方向键       逐个选择code   :heart:
  - Ctrl + shift + 方向键  按单词选择code    :heart:

- git

  - 配置别名 :heart:
    - git config --global alias.a "add ."
    - git config --global alias.cm "commit -m"
    - git config --global alias.s status
    - git config --global alias.d diff
    - git config --global alias.last "log -1 HEAD"
    - git config --global alias.lo "log --oneline -n 10"



##### **有意义的命名**

- 名副其实

  - 变量要说明它为什么会存在
  - 函数要说明它做什么事情
  - 类要说它怎么用

- 避免误导

  - 不要使用于本意相悖的词，如果accountList不是list类型，就会产生歧义
  - 不同之处较小的词语，很容易误导
  - 不要用小写字母I和大写字母O作为变量名

- 做有意义的区分

  同一作用范围内两样不同的东西要做有意义区分

  - 不能添加数字系列

    a1、a2，...aN

  - 不要说废话

    Product类、ProductInfo类、ProductData类没有意义 

    不要在变量里面用variable、Name加上NameString，表名里面加table

- 使用读的出来的名称

  不要自造字，要用完整的英语单词

- 使用可搜索的名称

  - 单字母名称仅用于短方法中的本地变量
  - 名称的长度应与其作用域大小相对应
  - 单字母和数字不容易搜索

- 避免使用编码

  

- 避免思维映射

  不应该名称容易误解成熟知的名称

- 类名

  大驼峰

  类名和对象名应该是名词或名词短语，不能是动词。而且应该具体，不要没有意义

- 方法名

  小驼峰

  方法名应该是动宾短语。:cake:

  属性访问器、修改器和断言应该根据其值命名，并加上get、set和is前缀

- 变量名

  小驼峰命名

- 常量名

  全部大写，用_分割

- 不要使用适用俗语或狸语，能够标准表达 意思就行时

- 要检查拼写



**花费20%的精力理解内部原理，80%的时间用来做上述工作**，**已经完成可以应付一般的编程需求**



