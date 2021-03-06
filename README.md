## web编程训练营的气

**培训和学校学习的不同**：学以致用，解决实际的问题，不但能够做出方案而且能够最终落地

**培训的目标**：能够对应简单的需求，创建满足需求，合乎质量要求的软件

**测试用例规则**

1. 不是通过测试的用例数目来衡量，而是以功能点的测试是否通过来衡量
2. 根据学院repository来评分，以teacher repository来评价需求的正确性
3. 如果import了未引用的package导致语法错误的，总分扣1分

   > 要检查引入的包，如果引入了没有用的包，要删掉    Ctrl + Alt + o    :accept:



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

   完整了解需求 :accept:

   - 读清楚需求，了解所有的需求
   - 将需求进行拆解，一步步拆解成有价值的最小场景

2. 程序逻辑

   > 自顶向下：将一个大需求，按照逻辑拆分成小需求，需求可以先用人话写出来   :heart:  :cake: 
   >
   > 先主后次：需求里面先完成主需求，保证跑通，再完成次需求 :yellow_heart:

   > 简单需求是否要拆分  :dancer:
   >
   > 先不择手段通过测试，再思考和重构，完整的理解需求，而不是为了过测试 :question:
   >
   > 最后要捋一遍测试，看是否真的通过

3. 写成程序

   > 针对小块功能，严格按照输入和返回来写   :yellow_heart:

   > 尽快的让代码编译，保证没有其他的错误  :accept:

   > 不要过早地进行性能优化

   确认函数  :accept:

   1. 写出想要什么，输入是什么，以及函数名字，也就是短逻辑，先不考虑实现  :heart:  :cake: :cactus:
   2. 用Alt+shift+enter创建函数   :heart:  :cake: 

   寻找可以实现需求的方法 :rabbit:

   - 通过idea来查找合适的方法，通过关键词过滤，通过阅读Javadoc确认
     - Ctrl  +  F12 查看源代码中所有的方法，可以搜索关键词过滤
     - 通过搜索首字母会更快
   - 通过Google搜索
   - 当不知道方法需要提供什么参数时，尝试new 然后得到提示

   

   > 严格实现需求

   - 需求只有完成和未完成两个状态，没有通过测试就是没有完成
   - 要完成文档中交待的功能
   - 可以查看方法的描述Ctrl+Q来判读此方法能否满足需要的功能 ​ ​ :yellow_heart:

4. 调试bug

   > 需要使用工具调试并观测中间过程。为了在调试中找到问题，必须能够首先阅读代码，并预测执行的结果

   - 设置断点debug调试  :gift_heart:
   - 使用idea给的建议   :heart:  :cake: :cactus:
     - 波浪线
     - 黄色方块



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

   - Intellij使用插件

     - Alibaba的代码格式检查插件  :yellow_heart: :green_heart:
     - SpotBugs  :accept:
     - SonarLint  :accept:

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

   - 每个方法的长度不要超过10行

   - 类的长度不要超过80到100行

   - for循环中的if 用continue防止多层嵌套   :heart:

   - 不要使用否定的函数逻辑

   - 不要重写JDK和JS中原生的方法

   - 不要使用标记为obsolete的方法或函数

   - 不要对简单问题使用复杂方法

   - 不能大部分使用public，这会疯狂暴露可见性

   - 表示逻辑或时，建议使用 ||， 不要使用 |，因为||有短路运算 ​ ​ :heart: :cake:

   - 表示逻辑与时。建议使用&&， &&具有短路运算    :heart:

   - 将复杂的对象抽象为类  :heart:

   - 方法中不要有多余的临时变量，该返回就return  :heart:

   - 方法中没有用的形参要删掉  :heart:

     
   
   **变量与常量**
   
   - 对于对象引用的变量声明，也应该使用final声明    ​ ​ :heart:
   
   - 变量声明为接口，不要声明具体的类型，hashmap建议用Map arrayList应该用list，方便以后的扩展 :heart:
   
   - 对于直接出现的数字，没有明确意义，叫做magic number，要用final type声明为常量 :heart::heart:  :cake:

   - 不会改变的变量，包括可能会改变，但是在自己作用域里面不变的话，都要用final或const声明为常量 :ice_cream:

   - 对于重复的常量初始化，包括调用一些方法得到值，可以抽出静态常量的field  :question:

   - 变量声明之处应该尽可能贴近使用它的地方  :heart:
   
   - 变量是不要有冗余的初始化
   
   - 对于变量声明之后，如果简单操作，就可以用 `Arrays.asList()`  :question:
   
   - 在field的标准下，如果将primitive变量用作常量，要使用final或者static final	
   
   - 使用 new int[array.length].var 就会生成 int[] ints = new int[array.length]  :accept:
   
    
   
   **数字和字符串**
   
   - 不能使用==比较double或者float的值 ，更不能去检测字符串 :heart:
      - == 与 ===区别   :heart:
          - == 会转换比较的类型
        - === 不会转换比较的类型
          - 两者都会对一些特殊值比较
      - 判断字符串是否既不是""也不是null​ ​  ​  :heart:
   
   ```java
if (null == textxxxxxx || "".equals(text)) 
   
   if (Object.isNull(text) || text.isEmpty())
   ```
   
      - 大量循环的字符串拼接应使用**StringBuilder** 或者 **String.format** 
   - 同样重复在string上使用**replace**也属于这种情况
      - 如果没有同步要求，不要使用**stringbuffer**
   
   - 迭代字符串不需要将其转化为数组	
   
   - 格式化指定宽度的字符串 :heart:  :cake:  
     - JavaScript   padEnd()方法
     - Java             “-” + width + “s”
   - Number.isNaN 要比全局的isNaN 更合适

 

 **数组和集合**


- 集合选择合适

 - 而且使用方法要正确
    - 创建一个空数组 :heart:  :cake:
      - String[]  result = {};
      - String[] result = new String[0];
      - Collections.emptyList();
    
 - JS中find和filter的比较

 - JS中可以用Array.isArray()方法

 - map方法可以有索引

 - js中正则要/\w/

    

 

 **stream**


- stream处理过程中不应存在无效的termination
- 对用使用stream解决的map、filter、reduce等问题就不要使用传统的循环

 - 对于应当使用optional的场景，就不要使用null推断

 

 **异常处理**   :heart_eyes:


 - JS抛出异常 throw new Error("");  
 - Java抛出的异常最好写上message



##### 重构方法

**流水线 pipeline** 

- 需要整体上需要做的是：

  \n分隔的文本    =>    input line list   => slection line list =>    barcode          =>     product           =>    product group       =>         receipt line   =>   receipt

- 现在这段代码做的是

  `String[]  =>   list<String> =>  list<String>  =>  list<String>  => list<Product> => List<ProductGroup>  => List<String> => String  `



**异常处理框架**

Ctrl+Alt+T 

```java
try {
    if (products.isEmpty()) {
        throw new EmptyProductListException();
    }
} catch (EmptyProductListException e) {
    return e.getmessage();
}
```

```java
package com.tw.exception;

public class EmptyProductListException extends ReceiptPrinterException {
    public EmptyProductListException() {
        super("Empty Product List");
    }
}
```

```java
package com.tw.exception;

public class ReceiptPrinterException extends RuntimeException {
    public ReceiptPrinterException(String message) {
        super(message);
    }
}
```

```java
products.stream()
    .filter(selectionLine -> {
        if (selectionLine.matches("^[0-9A-Z]+$")) {
            return true;
        }
        throw new InvalidInputException();
    })
```


collectingAndThen()可以对结果进行附加整理，在有异常处理时，就可以合并进去，增加代码的整洁性

```java
return selectionLines.stream()
    .collect(Collectors.collectingAndThen(Collectors.tolist(), list -> 		requireNonEmptyList(list)));

private List<Product> requireNonEmptyList(List<Product> list) {
    if (list.isEmpty()) {
        throw new EmptyProductListException();
    }
    return list;
}
```

```java
List<Product> productList = selectionLines.stream()
    .collect(Collectors.tolist());

if (productList.isEmpty()) {
    throw new EmptyProductListException();
}

return producList;
```



**return 两个结果的方法**

1. 利用map

   1. 统计一个list当中item的count

   ```java
   Map<Product, long> productGroups = products.stream().
       collect(Collectors.groupingBy(product -> product, Collectors.counting()));
   ```

   2. 将list变成map后进行排序

   ```java
   productGroups.keySet().stream()
       .sorted(new Comparator);
   
   productGroups.keySet().stream()
       .sorted(Comparator.comparing(Product::getBarcode));
   ```

   3. 获取map中的count

   ```java
   productGroups.keySet().stream()
       .map(product -> formatProduct(product, productGroups.get(product)));
   ```

2. 利用Map.Entry

   ```java
   Map.Entry<Product, Integer> entry = new AbstractMap.SimpleImmutableEntry<>(count, product);
   ```

3. 利用class

4. 通过输出参数

   ```java
   foo.setCount(count);
   ```

5. 通过数组

   ```java
   return Collections.nCopies(count, product);
   
   list.flatMap(products -> products.stream());
   ```

6. `List<Pair<product, count>>`



*在冗长的类抽取出一个独立的类**

> 梳理这个方法中的关系依赖图，要构成有向无环图。首先提取叶子节点，然后提取直接依赖叶子节点的方法，然后依次向上，直到提完。

1. extract 字段 

   - 在要提取的字段，Ctrl+shift+Alt+T 选择其中的encapsulate fields 设置get 和 set access

2. extract 方法，并创建类

   - 在要提取的方法，Ctrl+shift+Alt+T 选择其中的extract delegate，选择要抽取的东西，并创建新的类

3. move instance method  F6

   - visibility 一般选择默认的escalate就行，不行的话一层层往上提高级别

4. extract 方法时，遇到循环依赖

   - 通过F6进行抽取方法

   - 把依赖的变量提取出来，并通过Ctrl+Alt+F抽取字段
   - 然后在字段处，用构造器进行初始化
   - 然后去它的上层调用，进行初始化
   - 继续往上，解决参数问题
   - 向下解决没有用到的参数

**注意**：写代码时要调整合适的方法顺序以及名字，方便抽取



**根据不同的状态，抽取相似的子类**

1. 所有用构造函数的地方用factory method 进行创建
2. 添加subclass
3. 每处用到状态的判断的地方，提出最小范围的方法，在子类中实现
4. 要把之前的状态判断，现在不用的删除掉
5. 要调整方法位置，可以把子类放到一个文件夹里 F6

- 使用Ctrl+Shift+Alt+T 选择replace constructor with factory method
  
- name一般用create，创建静态方法，调用这个方法，就会创建类
  
- 创建subclass，先在父类class前添加abstract ,将构造函数改为protected,create constructor matching super

  - 可以用快捷键添加子类
  
  - 也可以手动添加

```java
public class ParserV1 extends Parser {
    protected ParserV1(ProductRepository repository) {
        super(repository);
    }
}
```


- 对于判断状态，进行操作的部分，抽取成函数

  1. 将函数内容剪切，函数类型改为protected abstract
  2. 将子类中进行重载
  3. 在重载函数中添加对应的处理


```java
public class ParserV1 extends Parser {
    protected ParserV1(ProductRepository repository) {
        super(repository);
    }

    @Override
    public boolean isV2() {
        return false;
    }
}
```


- 把create不要写死

  在父类中，把Crete也抽到ParserFactory

  然后在ParserFactory中的create方法 Ctrl+Alt+shift+T 中选convert to instance menthod 选this/new Parse Factory()

  把new ParseFactory Ctrl+Alt+F抽取字段，要注入
  
  在构造函数中初始化
  
  在调用地方，修改参数
  
- 判断条件要改为

```java
public static Parser create(String productSelection, ProductRepository repository) {
    if (productSelection.startsWith("-v2-\n")) {
        return new ParserV2(repository);
    }
    return new ParserV1(repository);
}
```







##### 快捷键

- Intellij

  - 窗口区域
    - Ctrl + shift +  F12      只显示代码编辑区
    - Alt + 数字                    隐藏或显示窗口
    - Alt+3 切换到find面板  Alt+4 切换到run面板  F4可以看没有通过的测试
    - 在测试结果的配置项 可以选择select first failed test when finished，就会每次打开失败的测试
    - Alt + 左右键              在打开的文件之间切换
    - Ctrl + F4                    关闭现在打开的文件
  - 切换文件

    - 长按 Ctrl + Shift + F    全文搜索
    - Alt + 1                          调出文件树
    - Ctrl + shift + 左键    返回编辑的位置
    - Ctrl + E                      最近访问的文件的列表

  - 移动光标与选取代码

    - Ctrl  + Shift +enter    光标跳到这段代码之后
    - shift + enter               光标跳到这行代码之后
    - Ctrl  +  左右键             光标在单词之间跳转
    - shift  + 左右键             挨个选择代码
    - Ctrl  +  shift + 左右键   选择单词代码
    - shift  + 上下键             按行来选中代码
    - Alt  + shift  + 方向键   移动代码

  - 测试

    - Ctrl + shift + T             在测试与主程序之间切换
    - shift + F10                    运行之前的测试
    - Ctrl + shift  + F10         运行测试

  - 方法

    - Ctrl  +  F12                  查看源代码中所有的方法
    - Ctrl + B                       访问方法
    - Ctrl + Q                      渲染注释
    - Alt + shift + enter      使用idea建议
    - F2                                 获取idea建议

    - logical condition.if          快速生成if判断语句
    - new int[].var                    快速声明变量
    - .for                                     快速生成for循环语句

  - 格式

    - Shift + F6                    批量修改变量名
    - Ctrl + Alt + L              格式化
    - Ctrl  + Alt + o             删除没有用到的import
    - Ctrl+Shift+J                能够join lines

  - 抽取

    - Ctrl + Alt + m             抽取方法  
    - Ctrl +  Alt  + c             抽取常量
    - Ctrl +  Alt  + v             抽取变量

  - 注释

    - Ctrl + \                        快速多行注释

  - 快捷键 

    - Ctrl  +   shift  +  A       可以找actions搜索操作
    - Ctrl  +  Alt  +  S        找到keymap   找到相应快捷键进行设置

  

- VS Code

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
  - 打tag



##### **有意义的命名**

- 类名  对象名

  使用大驼峰，要是名词或名词短语，而且要具体，不要没有意义

- 方法名

  使用小驼峰，要是动宾短语，可以使用get、set、is、calc前缀，要使用恰当 :heart:

- 变量名

  使用小驼峰，要是名词或名词短语，要有具体意义

- 常量名

  全部大写，用_分割

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

  - 不能添加数字系列,，尤其是在for循环里面

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

- 不要使用适用俗语或狸语，能够标准表达 意思就行时

- 要检查拼写



**花费20%的精力理解内部原理，80%的时间用来做上述工作**，**已经完成可以应付一般的编程需求**



