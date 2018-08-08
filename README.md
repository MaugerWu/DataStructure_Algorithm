[一、数据结构（Data Structure）](https://github.com/MaugerWu/DataStructure_Algorithm/blob/master/README.md#%E4%B8%80%E6%95%B0%E6%8D%AE%E7%BB%93%E6%9E%84data-structure)

[二、算法（Algorithm）](https://github.com/MaugerWu/DataStructure_Algorithm/blob/master/README.md#%E4%BA%8C%E7%AE%97%E6%B3%95algorithm)

[三、线性表（Linear List）](https://github.com/MaugerWu/DataStructure_Algorithm/blob/master/README.md#%E4%B8%89%E7%BA%BF%E6%80%A7%E8%A1%A8linear-list)

[四、栈与队列（Stack And Queue）](https://github.com/MaugerWu/DataStructure_Algorithm/blob/master/README.md#%E5%9B%9B%E6%A0%88%E4%B8%8E%E9%98%9F%E5%88%97stack-and-queue)

[五、串（String）](https://github.com/MaugerWu/DataStructure_Algorithm/blob/master/README.md#%E4%BA%94%E4%B8%B2string)

[六、树（Tree）](https://github.com/MaugerWu/DataStructure_Algorithm/blob/master/README.md#%E5%85%AD%E6%A0%91tree)

[七、图（Graph）](https://github.com/MaugerWu/DataStructure_Algorithm/blob/master/README.md#%E4%B8%83%E5%9B%BEgraph)

[八、查找（Search）](https://github.com/MaugerWu/DataStructure_Algorithm/blob/master/README.md#%E5%85%AB%E6%9F%A5%E6%89%BEsearch)

[九、排序（Sort）](https://github.com/MaugerWu/DataStructure_Algorithm/blob/master/README.md#%E4%B9%9D%E6%8E%92%E5%BA%8Fsort)



---




## 一、数据结构（Data Structure）

+ **数据（Data）** 是描述客观事物的符号，是计算机中可以操作的对象，是能被计算机识别，并输入给计算机处理的符号集合。

+ **数据元素（Data Element）** 是组成数据的、有一定意义的基本单位，在计算机中通常作为整体处理。也被称为 **记录（Record）**。

+ **数据项（Data Item）** 指一个数据元素可以由若干个数据项组成。

+ **数据对象(Data Object)** 是性质相同的数据元素的集合，是数据的子集。

+ **数据结构（Data Structure）** 是指相互之间存在一种或多种特定关系的数据元素的集合。

+ **逻辑结构（Logical Structure）** 是指数据对象中数据元素之间的相互关系。
  1. 集合结构（Collection）： 集合结构中的数据元素除了同属一个集合外，它们之间没有其他的关系。
  2. 线性结构（Linear）： 线性结构中的数据元素之间是 **一对一** 的关系。
  3. 树形结构（Tree）： 树形结构中的数据元素之间存在一种 **一对多** 的层次关系。
  4. 图形结构（Graphical）： 图形结构的数据元素是 **多对多** 的关系。

+ **物理结构（Physical Structure）** 是指数据的逻辑结构在计算机中的储存形式。
  1. 顺序储存结构（Sequential Storage）： 是把数据元素存放在地址连续的存储单元里，其数据间的逻辑关系和物理关系是一致的。
  2. 链式储存结构（Chained Storage）： 是把数据元素存放在任意的存储单元里，这组存储单元可以是连续的，也可以是不连续的。

## 二、算法（Algorithm）

+ **算法（Algorithm）** 是解决特定问题求解步骤的描述，在计算机中表现为指令的有限序列，并且每条指令表示一个或多个操作。

+ 算法的5个特性
  1. 输入
  2. 输出
  3. 有穷性
  4. 确定性
  5. 可行性

+ 算法设计的要求
  1. 正确性
  2. 可读性
  3. 健壮性
  4. 时间效率高和储存量低

+ 算法时间复杂度（Time Complexity） T(n)=O(f(n))
  1. 常数阶 O(1)
  2. 线性阶 O(n)
  3. 对数阶 O(logn)
  4. 平方阶 O(n^2)
  5. O(1) < O(logn) < O(n) < O(nlogn) < O(n^2) < O(n^3) < O(2^n) < O(n!) < O(n^n)

+ 算法空间复杂度（Space Complexity） S(n)=O(f(n))

  &emsp;&emsp;算法的空间复杂度通过计算算法所需的存储空间实现，算法空间复杂度的计算公式记作: S(n)= O(f(n))，其中，n 为问题的规模， f(n) 为语句关于 n 所占存储空间的函数。

## 三、线性表（Linear List）

+ **线性表：** 

  &emsp;&emsp;零个或多个数据元素的有限序列。在较复杂的线性表中，一个数据元素可以由若干个数据项组成。（如：班级同学点名册）

+ 线性表的操作：

  1. InitList(L) // 初始化操作，建立一个空的线性表 L 
  2. DestroyList(L) // 线性表存在了，消耗一个线性表
  3. ClearList（L） // 将线性表清空
  4. ListEmpty（L） // 若线性表为空，返回 true；否则返回 false
  5. ListLength（L） // 返回线性表的长度
  6. GetElem（L, i, e） // 将线性表 L 中的第 i 个位置上的元素值返回给 e    
  7. PriorElem（L, cur_e, pre_e） // 如果 cur_e 是线性表中的元素，而且不是第一个，那么返回该元素前一个元素的值
  8. NextElem（L, cur_e, next_e） // 如果 cur_e 是线性表中的元素，而且不是最后一个，就返回它下一个元素的值
  9. Listinsert(L, i, e) // 如果线性表 L 存在了，而且 i 符合条件，则在 i 位置插入一个元素
  10. ListDelete（L, i） // 删除 i 位置上的元素
  11. ListDelete_data(L, e, order) // 删除指定的元素 e，order 决定是删除一个，还是全部
  12. Connect_two_List(L_a, L_b, L_c) // 连接两个线性表，除去重复的内容    
  13. print(L) // 打印线性表 L

+ **单链表：** 

    &emsp;&emsp;链表的定义是递归的，它或者为“空”（通常用 NULL 或 “^” 表示），或者指向另一个节点 Node 的引用，这个节点含有下一个节点或链表的引用。与顺序存储相比，允许存储空间不连续，插入删除时不需要移动大量的元素，只需修改指针即可，但查找某个元素，只能从头遍历整个链表。

  - 结点由存放数据元素的数据域和存放后继结点地址的指针域组成。
  - 链表中第一个结点的存储位置叫做头指针；在单链表的第一个节点前附设一个结点，称为头结点。
  - 无论链表是否为空，头指针均不为空。
  - 头结点不一定是链表的必须元素。

+ 单链表的操作：

  1. 头插法

  &emsp;&emsp;始终让新结点都插在第一的位置，如图：

  ![头插法](https://github.com/MaugerWu/DataStructure_Algorithm/blob/master/images/1.png)

  ```java
  public void headInsert(T item) {
      Node old = first;
      first = new Node();
      first.item = item;
      first.next = old;
      count++;
  }
  ```

  2. 尾插法

  &emsp;&emsp;把每次新结点都插在终端结点的后面，如图：

  ![尾插法](https://github.com/MaugerWu/DataStructure_Algorithm/blob/master/images/2.png)

  ```java
  public void tailInsert(T item) {
      Node old = last;
      last = new Node();
      last.item = item;
      last.next = null;
      if (isEmpty()) {
          first = last;
      } else {
          old.next = last;
      }
      count++;
  }
  ```

  &emsp;&emsp;节点的插入和删除，要点是先断后连，关键就是不要断链了，以插入为例（把s插入 p 和 q 之间），先断意思是先把 p->q 断了，变成 s->q，后连，最后再把 p 和 s连接起来。

  3. 插入节点

  &emsp;&emsp;待插入节点为s，一般采用后插法，即先找到插入位置节点的前驱节点，然后插入，时间复杂度O(n)。如图：

  ![插入结点](https://github.com/MaugerWu/DataStructure_Algorithm/blob/master/images/3.png)

  ```java
  p=getNodeByIndex(i-1);
  s.next = p.next;
  p.next = s;
  ```

  &emsp;&emsp;还有一种方法是，直接插入到位置的后面（前插法），然后交换两个节点的值，插入的节点到了指定位置，时间复杂度 O(1)：

  ```java
  s.next = p.next;
  p.next = s;
  temp = p.item;    // 交换内容
  p.item = s.item;
  s.item = temp;
  ```

  4. 删除节点

  &emsp;&emsp;待删除节点为 q，也是先找到前驱节点，修改指针域即可，时间复杂度 O(n)。如图：

  ![删除结点](https://github.com/MaugerWu/DataStructure_Algorithm/blob/master/images/4.png)

  ```java
  P = getNodeByIndex(i-1);
  q = p.next;
  p.next = q.next;
  q = null;
  ```

  &emsp;&emsp;删除节点也能直接删除其后继节点，然后将后继节点的内容赋给自己即可，时间复杂度为 O(1)：

  ```java
  q = p.next;
  p.item = p.next.item;
  p.next = q.next;
  q = null;
  ```

+ 线性表与单列表的区别：

  |存储类别|顺序存储结构|单链表（链式存储结构）|
  |:--:|:--|:--|
  |存储分配方式|用一段地址连续的存储单元依次存储线性表的数据元素|采用链式存储结构，用一组任意的存储单元存放线性表的元素|
  |时间性能|查找O（1）、插入和删除O（n）|查找O（n）、插入和删除O（1）|
  |空间性能|需要预分配存储空间，分大了浪费，小了容易发生上溢|不需要分配存储空间，只要有就可以分配，元素个数不受限制|

+ **静态链表：**

  &emsp;&emsp;用数组描述的链表叫做静态链表。这种链表在初始时必须分配足够的空间，也就是空间大小是静态的，在进行插入和删除时则不需要移动元素，修改指针域即可，所以仍然具有链表的主要优点（快速插入和删除）。

+ **静态单链表的结构：**

  ```java
  #define MAXSIZE 1000;

  typedef struct {
    ElemType data; // 数据域
    int cur; // 游标
  }component,SLinkList[MAXSIZE];
  ```

+ **静态链表优缺点：**

  |优点|缺点|
  |:--:|:--:|
  |在插入和删除操作时，只需要修改游标，不需要移动元素，从而改进了在顺序存储结构中的插入和删除操作需要移动大量元素的缺点|没有解决连续存储分配带来的表长难以确定的问题；失去了顺序存储结构随机存取的特性。|

+ **循环链表：**

  &emsp;&emsp;循环链表（Circular Linked List）是指将单链表中终端结点的指针端由空指针改为指向头结点，使整个单链表头尾相接形成一个环。

  &emsp;&emsp;循环链表和单链表的主要差异就在于循环的判断条件上，原来是判断 p->next 是否为空，现在则是 p->next 等于头结点，则循环结束。

+ **双向链表：**

  &emsp;&emsp;双向链表（Double Linked List）是在单链表的每个结点中，再设置一个指向其前驱结点的指针域。所以在双向链表中的结点都有两个指针域，一个指向直接后继，另一个直接指向直接前驱。

## 四、栈与队列（Stack And Queue）

+ **栈：**

  &emsp;&emsp;栈（stack）是限定仅在表尾进行插入和删除操作的线性表。将允许插入和删除的一端称为 **栈顶（top）**，另一端称为 **栈底（bottom）**，不含任何数据元素的栈称为 **空栈**。栈又称为后进先出（Last In First Out）的线性表，简称 **LIFO** 结构。

+ **栈的操作：**

    1. 栈的插入操作：叫做进栈 / 压栈 / 入栈（push）。

    2. 栈的删除操作：叫做出栈（pop）。

+ **栈的顺序存储结构：**

&emsp;&emsp;既然栈是线性表的特例（简称：顺序栈），以数组下标为 0 的一端作为栈底，因为首元素都存在栈底，变化最小。

+ **栈的链式存储结构：**

&emsp;&emsp;栈的链式存储结构（简称：链栈），将栈顶放在单链表的头部，通常对于链栈来说，是不需要头结点的。

+ **栈的应用：**

&emsp;&emsp;递归：斐波拉契数列的实现（Fibonacci）。

&emsp;&emsp;后缀（逆波兰 Reverse Polish Notation）表示法 — 四则运算表达式求值。

&emsp;&emsp;比如**中缀表达式：** `9 + （3 - 1） * 3 + 10 / 2`，**后缀表达式为：** `9 3 1 - 3 * + 10 2 / +`。

+ **递归：**

&emsp;&emsp;把一个直接调用自己或通过一系列的调用语句间接地调用自己的函数，称为递归函数。

+ **队列：**

  &emsp;&emsp;队列（Queue）是只允许在一端进行插入操作，而在另一端进行删除操作的线性表。队列是一种先进先出（First In First Out）的线性表，简称： **FIFO**。允许插入的一端叫做队尾，允许删除的一端称为队头。

+ **循环队列：**

&emsp;&emsp;将队列的这种头尾相接的顺序存储结构称为循环队列。

+ **队列判空/满：**

&emsp;&emsp;当 front = rear 时，队列为空；

&emsp;&emsp;当 （rear + 1） % QueueSize == front 时，队列为满；

&emsp;&emsp;计算队列长度：（rear - front + QueueSize）% QueueSize

+ **链队列：**

&emsp;&emsp;队列的链式存储结构 —— 链队列。

&emsp;&emsp;入队操作时，其实就是在链表尾部插入结点；

&emsp;&emsp;出队操作时，就是头结点的后继节点出队。

## 五、串（String）

+ **串**

&emsp;&emsp;串是由零个或多个字符组成的有限序列，又名叫字符串。一般记为：s = "a1a2a3a4...an"（n > 0）

+ **回文诗： 宋代-李禺**

  > 枯眼望遥山隔水，往来曾见几心知？

  > 壶空怕酌一杯酒，笔下难成和韵诗。

  > 途路阻人离别久，讯音无雁寄回迟。

  > 孤灯夜守长寥寂，夫忆妻兮父忆儿。

  &emsp;&emsp;反过来读一遍：

  > 儿忆父兮妻忆夫，寂寥长守夜灯孤。

  > 迟回寄雁无音讯，久别离人阻路途。

  > 诗韵和成难下笔，酒杯一酌怕空壶。

  > 知心几见曾来往？水隔山遥望眼枯。

+ **串的顺序存储结构：**

  &emsp;&emsp;串的顺序存储结构是用一组地址连续的存储单元来存储串中的字符序列的。按照预定义的大小，为每个定义的串变量分配一个固定长度的存储区。一般是用定长数组来定义。

+ **串的链式存储结构：**

&emsp;&emsp;串的链式存储结构与线性表是相似的，由于串结构的特殊性，一个结点可以存放一个字符，也可以存放多个字符。

+ **串的匹配算法：**

&emsp;&emsp;朴素模式匹配算法：串的定位操作通常称为串的模拟匹配。

&emsp;&emsp;KMP 模式匹配算法

## 六、树（Tree）

+ **树** 是 n（n>=0）个结点的有限集。n=0 时称为 **空树**。在任意一棵树中：

1. 有且仅有一个称为 **根（Root）** 的结点；
2. 当 n>1 时，其余的结点可分为 m（m>0）个互不相交的有限集 T1、T2、T3、....、Tm，其中每一个集合本身又是一棵树，并且称为根的子树（SubTree）。

+ **结点的分类：**

  &emsp;&emsp;结点拥有的子树数称为结点的 **度（Degree）**。度数为 0 的结点称为 **叶节点（Leaf）** 或终端结点；度数不为 0 的结点称为非终端结点或分支结点。除根节点外，分支节点也称为内部节点。

&emsp;&emsp;结点的层次（Level）从根开始定义起，根为第一层，根的孩子为第二层。

&emsp;&emsp;树中结点的最大层次称为树的 **深度（Depth）**。

&emsp;&emsp;**森林（Forest）** 是 m（m>=0）颗互不相交的树的集合。

  |线性结构|树结构|
  |--|--|
  |第一个数据元素：无前驱|根节点：无双亲，唯一|
  |最后一个元素：无后继|叶节点：无孩子，可以多个|
  |中间元素：一个前驱一个后继|中间结点：一个双亲多个孩子|

+ **树的存储结构：**

1. 双亲表示法

&emsp;&emsp;以一组连续空间存储树的结点，同时在每个结点中，附设一个指示器指示其双亲结点在数组中的位置。

&emsp;&emsp;由于根节点是没有双亲的，所以我们约定根节点的位置域设置为 -1。

  |下标|data|parent|
  |--|--|--|
  |0|A|-1|
  |1|B|0|
  |2|C|0|
  |3|D|1|
  |4|E|2|
  |5|F|2|
  |6|G|3|
  |7|H|3|
  |8|I|3|
  |9|J|4|

2. 孩子表示法

  &emsp;&emsp;由于树中每个结点可能有多棵子树，可以考虑用多重链表，即每个结点有多个指针，其中一个指针指向一棵树的根节点，我们把这种方法叫做 **多重链表表示法**。

|方案一|指向该结点的孩子结点||||||方案二|该结点的孩子结点个数|指向该结点的孩子结点||||
|--|--|--|--|--|--|--|--|--|--|--|--|--|
|data|child1|child2|child3|......|childn||data|degree|child1|child2|......|childn|

  &emsp;&emsp;方案一：一种是指针域的个数就等于树的度，其中 data 是数据域，child1 到 childn 是指针域，用来指向该结点的孩子结点。缺点：可能会浪费空间。

  &emsp;&emsp;方案二：每个结点指针域的个数等于该结点的度，专门用一个位置来存储结点指针域的个数。其中 data 为数据域，degree 为度域，也就是存储该结点的孩子的孩子结点的个数，child1 到 childn 是指针域，用来指向该结点的各个孩子的结点。

3. 孩子兄弟表示法

  &emsp;&emsp;任意一棵树，它的结点的第一个孩子如果存在就是唯一的，它的右兄弟如果存在也是唯一的。因此，我们设置两个指针，分别指向该结点的第一个孩子和此结点的右兄弟。|data|firstchild|rightsib|，优点：查找某个结点的某个孩子很方便；缺点：不能快速找出该结点的双亲。（改进：利用二叉树的特性和算法来处理）

+ **二叉树（Binary Tree）**

  &emsp;&emsp;二叉树是 n（n>=0）个结点的有限集合，该集合或者为空集（称为空二叉树），或者由一个根节点和两颗互不相交的、分别称为根节点的左子树和右子树的二叉树组成。

+ **二叉树的特点**

  1. 每个结点最多有两棵子树；
  2. 左子树和右子树是有顺序的，次序不能任意颠倒；
  3. 即使树中某个结点只有一棵子树，也要区分它是左子树还是右子树。

+ **二叉树具有的五种基本形态**

  1. 空二叉树；
  2. 只有一个根结点；
  3. 根结点只有左子树；
  4. 根结点只有右子树；
  5. 根结点既有左子树又有右子树。

+ **特殊二叉树**

1. 斜树

&emsp;&emsp;所有的结点都只有左子树的二叉树叫 **左斜树**。所有的结点都只有右子树的二叉树叫 **右斜树**。

2. 满二叉树

&emsp;&emsp;在一棵二叉树中，所有分支结点都存在左子树和右子树，并且所有叶子都在同一层上。

3. 完全二叉树

    &emsp;&emsp;对一棵具有 n 个结点的二叉树 **按层序编号**，如果编号为 i（1 <= i <= n）的结点与同样深度的满二叉树中编号为 i 的结点在二叉树中位置完全相同，则这棵树称为 **完全二叉树**。

+ **完全二叉树的特点**

  1. 叶子结点只能出现在最下两层；
  2. 最下层的叶子一定集中在左部连续位置；
  3. 倒数第二层，若有叶子结点，一定都在右部连续位置；
  4. 如果结点度数为 1 ，则该结点只有左孩子，即不存在只有右子树的情况；
  5. 同样结点数的二叉树，完全二叉树的深度最小。

+ **二叉树的性质**

  1. 性质1：在二叉树的第 i 层上最多有 **2 的 i-1 次方** 个结点（i>=1）
  2. 性质2：深度为 k 的二叉树最多有 **2 的 k次方减去 1** 个结点（k>=1）
  3. 性质3：对任何一棵二叉树 T，如果其终端结点数为 n0，度数为 2 的结点数为 n2,则 **n0 = n2 + 1**。
  4. 性质4：具有 n 个结点的完全二叉树的深度为 **log2n + 1**。
  5. 性质5：如果对一棵具有 n 个结点的完全二叉树（其深度为 **log2n + 1**）的结点按层2序编号（从第 1 层到第 **log2n + 1** 层，每层从左到右），对任一结点 i（1 <= i <= n）有：
    1. 如果 i=1，则结点 i 是二叉树的根，无双亲；如果 i>1，则双亲是结点 i/2。
    2. 如果 2i > n，则结点 i 无左孩子（结点 i 为叶子结点）；否则其左孩子是结点 2i。
    3. 如果 2i+1 > n，则结点 i 无右孩子；否则其右孩子是结点 2i+1。
  
+ **二叉树顺序存储结构**

&emsp;&emsp;二叉树的顺序存储结构就是用 **一维数组** 存储二叉树中的结点。顺序存储结构一般只用于 **完全二叉树**。

+ **二叉链表**

&emsp;&emsp;lchild，data，rchild。二叉树每个结点最多有两个孩子，所以为它设计一个数据域和两个指针域。

+ **二叉树的遍历**

  &emsp;&emsp;二叉树的遍历（Traversing Binary Tree）是指从根结点出发，按照某种**次序**依次**访问**二叉树中所有结点，使得每个结点被访问一次且仅被访问一次。

+ **前序遍历**

&emsp;&emsp;规则是若二叉树为空，则空操作返回；否则先访问根结点，然后前序遍历左子树，再前序遍历右子树。

+ **中序遍历**

  &emsp;&emsp;规则是若二叉树为空，则空操作返回；否则从根结点开始（注意并不是先遍历根结点），中序遍历根结点的左子树，然后访问根结点，最后中序遍历右子树。

+ **后序遍历**

&emsp;&emsp;规则是若二叉树为空，则空操作返回；否则从从左到右先叶子后结点的方式遍历访问左右子树，最后是访问根结点。

+ **层次遍历**

  &emsp;&emsp;规则是若二叉树为空，则空操作返回；否则从树的第一层，也就是从根结点开始访问，从上而下逐层遍历，在同一层中，按从左到右的顺序对结点逐个访问。

+ **线索二叉树**

  &emsp;&emsp;指向前驱和后继的指针称为线索，加上线索的二叉链表称为线索链表，相应的二叉树就称为线索二叉树（Threaded Binary Tree）。

  &emsp;&emsp;其实线索二叉树，等于是把一棵二叉树转变成了一个**双向链表**，这样对我们的插入删除结点、查找某个结点都带来了方便。

  &emsp;&emsp;lchild，ltag，data，rtag，rchild。

+ **树转换为二叉树**

  1. 加线。在所有兄弟结点之间加一条连线。
  2. 去线。对树中每个结点，只保留它与第一个孩子结点的连线，删除它与其他孩子结点之间的连线。
  3. 层次调整。以树的根结点为轴心，将整棵树顺时针旋转一定的角度，使之结构层次分明。

+ **森林转换为二叉树**

  1. 把每棵树转换为二叉树（森林是由若干棵树组成）。
  2. 第一棵二叉树不动，从第二颗二叉树开始，依次把后一棵二叉树的根结点作为前一棵二叉树的根结点的右孩子，用线连接起来。当所有的二叉树连接起来后就得到了由森林转换来的二叉树。

+ **二叉树转换为树**

  1. 加线。
  2. 去线。
  3. 层次调整。

+ **二叉树转换为树**

  1. 从根结点开始，若右孩子存在，则把与右孩子结点的连线删除，再查看分离后的二叉树，若右孩子存在，则删除连接线...，直到所有右孩子连接线都删除为止，等到分离的二叉树。
  2. 将每棵树分离的二叉树转换为树即可。

+ **树的遍历**

1. 先根遍历。先访问树的根结点，然后依次先根遍历根的每棵子树。
2. 后根遍历。先依次后根遍历每棵子树，然后再访问根结点。

+ **森林的遍历**

  1. 前序遍历。先访问森林中的第一棵树的根结点，然后再依次先根遍历根的每棵子树，再依次用同样方式遍历除去第一棵树的剩余树结构的森林。
  2. 后序遍历。先访问森林中的第一棵树，后根遍历的方式遍历每棵子树，然后再访问根结点，再依次用同样方式遍历除去第一棵树的剩余树结构的森林。

+ **哈夫曼树**

&emsp;&emsp;**路径长度：**从树中一个结点到另一个结点之间的分支构成两个结点之间的路径，路径上的分支数目称作路径长度。

&emsp;&emsp;树的路径长度就是从树根到每一结点的路径长度之和。

&emsp;&emsp;带权路径长度 WPL 最小的二叉树称作**哈夫曼树**。


## 七、图（Graph）

+ **图**

  &emsp;&emsp;是由顶点的有穷非空集合和顶点（Vertex）之间边（Edge）的集合组成，通常表示为：G（V，E），G 表示一个图，V 是图 G 中顶点的集合，E 是图 G 中边的集合。

+ **无向图**

&emsp;&emsp;图中任意两个顶点之间的边都是无向边。

+ **有向图**

&emsp;&emsp;图中任意两个顶点之间的边都是有向边。

+ **有向边 / 无向边**

&emsp;&emsp;有向边用`<>`表示，无向边用`()`表示。

+ **无向完全图**

&emsp;&emsp;在无向图中，任意两个顶点之间都存在边。含有 n 个顶点的无向完全图有`n(n-1)/2`条边。

+ **有向完全图**

&emsp;&emsp;在有向图中，任意两个顶点之间都存在方向互为相反的弧（Arc）。

+ **稀疏图 / 稠密图**

&emsp;&emsp;有很少条边或弧的图称为稀疏图，反之称为稠密图。

+ **权（Weight） / 网（Network）**

&emsp;&emsp;图的边或弧具有与它相关的数字叫做**权（Weight）**。这种带权的图通常称为**网（Network）**。

+ 图的存储结构

  1. 邻接矩阵（Adjacency Matrix）

    &emsp;&emsp;图的邻接矩阵存储方式是用两个数组来表示图。一个一维数组存储图中的顶点信息，一个二维数组（称为邻接矩阵）存储图中的边或弧的信息。

  2. 邻接表（Adjacency List）

    &emsp;&emsp;考虑到对于边数相对顶点较少的图，邻接矩阵存在对存储空间的极大浪费。由此诞生了邻接表：图中顶点用一个一维数组存储，对于顶点数组中，每个数据元素还需要存储指向第一个邻接点的指针，以便于查找该顶点的边信息。图中每个顶点的邻接点构成一个线性表，由于邻接点的个数不确定，所以用单链表存储。

  3. 十字链表（Orthogonal List）

    &emsp;&emsp;十字链表（有向图的一种存储方法）：重新定义顶点表结构为：|data|firstin|firstout|，其中`firstin`表示入边表头指针，指向该顶点的入边表中第一个结点，`firstout`表示出边表头指针，指向该顶点的出边表中的第一个结点。

    &emsp;&emsp;重新定义边或弧表结构为：|tailvex|headvex|headlink|taillink|，其中`tailvex`是指弧起点在顶点表的下标，`headvex`是指弧终点在顶点表中的下标，`headlink`是指入边表指针域，指向终点相同的下一条边，`taillink`是指边表指针域，指向起点相同的下一条边。如果是 **网**，还可以增加一个`weight`域来存储权值。

  4. 邻接多重表

    &emsp;&emsp;邻接多重表（无向图存储结构的优化——边的操作）：重新定义边表结点结构：|ivex|ilink|jvex|llink|，其中`ivex`和`jvex`是与某条边依附的两个顶点在顶点表中的下标。`ilink`指向依附顶点`ivex`的下一条边，`jlink`指向依附顶点`jvex`的下一条边。

  5. 边集数组

    &emsp;&emsp;边集数组是由两个一维数组构成。一个是存储顶点的信息；另一个是存储边的信息，这个边数组每个元素由一条边的起点下标（begin）、终点下标（end）和权（weight）组成。

    &emsp;&emsp;重新定义边数组结构为：|begin|end|weight|，其中`begin`是存储起点下标，`end`是存储终点下标，`weight`是存储权值。

+ 图的遍历

  &emsp;&emsp;从图中某一顶点出发访问图中其余顶点，且使每一个顶点仅被访问一次，这一过程就叫做图的遍历（Traversing Graph）。

  1. 深度优先遍历（Depth First Search **DFS**）

  2. 广度优先遍历（Breadth First Search **BFS**）

+ 最小生成树

  1. Prim 算法

  2. Kruskal 算法

+ 最短路径

  1. Dijkstra 算法

  2. Floyd 算法

+ 拓扑排序

  &emsp;&emsp;在一个表示工程的有向图中，用顶点表示活动，用弧度表示活动之间的优先关系，这样的有向图为顶点表示活动的网，称为 **AOV 网（Activity On Vertex Network）**

+ 拓扑排序算法


+ 关键路径


## 八、查找（Search）

+ 顺序表查找

  1. 顺序查找又称线性查找

  ``` java
  int Sequential_Search(int[] a, int n, int key)
  {
    int i;
    for (i=1; i<=n; i++)
    {
      if (key == a[i])
      {
        return i;
      }
    }
    return 0;
  }
  ```

  2. 顺序表查找优化（优化每次循环时都需要对 i 是否越界，即是否小于等于 n 做判断）

  ``` java
  int Sequential_Search2(int[] a, int n, int key)
  {
    int i;
    a[0] = key;
    i = n;
    while (a[i] != key)
    {
      i--;
    }
    return i; // 返回 0 则查找失败
  }
  ```

+ 有序表查找

  1. 折半查找（Binary Search）又称二分查找

  &emsp;&emsp;前提是线性表中的记录必须是关键码有序，线性表必须采用顺序存储。

  ```java
  public int Binary_Search(int[] arr, int key)
  {
      int low = 0;
      int high = arr.length - 1;
      int mid;

      while (low <= high)
      {
          mid = (low + high) / 2;
          if (key < arr[mid])
          {
              high = mid - 1;
          } else if (key > arr[mid])
          {
              low = mid + 1;
          } else
          {
              return mid;
          }
      }

      return -1; // 表中不存在 key
  }
  ```

  2. 插值查找

  &emsp;&emsp;插值查找是根据折半查找（二分查找）来优化，由折半查找中代码 mid=(low+high)/2;
  变换后得到：mid=low+(high-low)/2;
  改进后为：
  low + (high - low) * (key - arr[low]) / (arr[high] - arr[low]);

  ```java
  public int Interpolation_Search(int[] arr, int key)
  {
    int low = 0;
    int high = arr.length - 1;
    int mid;

    while (low <= high)
    {
      mid = low + (high - low) * (key - arr[low]) / (arr[high] - arr[low]); // 优化的部分
      if (key < arr[mid])
      {
        high = mid - 1;
      } else if (key > arr[mid])
      {
        low = mid + 1;
      } else
      {
        return mid;
      }
    }
    return -1; // 表中不存在 key
  }
  ```

  3. 斐波那契查找（Fibonacci Search）


  * 前提：
  
  &emsp;&emsp;斐波那契查找的前提是待查找的查找表必须顺序存储并且有序。

  * 核心：
  
    1）当key=a[mid]时，查找成功；
    2）当key<a[mid]时，新的查找范围是第low个到第mid-1个，此时范围个数为F[k-1] - 1个，即数组左边的长度，所以要在[low, F[k - 1] - 1]范围内查找；
    3）当key>a[mid]时，新的查找范围是第mid+1个到第high个，此时范围个数为F[k-2] - 1个，即数组右边的长度，所以要在[F[k - 2] - 1]范围内查找。

    &emsp;&emsp;关于斐波那契查找， 如果要查找的记录在右侧，则左侧的数据都不用再判断了，不断反复进行下去，对处于当众的大部分数据，其工作效率要高一些。所以尽管斐波那契查找的时间复杂度也为O(logn)，但就平均性能来说，斐波那契查找要优于折半查找。可惜如果是最坏的情况，比如这里key=1，那么始终都处于左侧在查找，则查找效率低于折半查找。

    &emsp;&emsp;还有关键一点，折半查找是进行加法与除法运算的（mid=(low+high)/2），插值查找则进行更复杂的四则运算（mid = low + (high - low) * ((key - a[low]) / (a[high] - a[low]))），而斐波那契查找只进行最简单的加减法运算（mid = low + F[k-1] - 1），在海量数据的查找过程中，这种细微的差别可能会影响最终的效率。

  ```java
  public class FibonacciSearch
  {
    /** 斐波那契数列长度 */
    private static final int MAX_SIZE = 20;

    /**
     * 斐波那契查找
     * @param arr 顺序表有序数列
     * @param key 将要查找的数
     * @return
     */
    public static int Fibonacci_Search(int[] arr, int key)
    {
      int len = arr.length;
      if (arr == null || len == 0)
      {
        return -1;
      }

      int low = 0;
      int high = len - 1;
      int k = 0;
      int[] fb = new int[MAX_SIZE];
      createFibonacci(fb);
      while (len > fb[k] - 1)
      {
        k++;
      }

      int[] temp = Arrays.copyOf(arr, fb[k] - 1); // 构造一个长度为 F[k] - 1 的新数列
      for (int i = len; i < fb[k] - 1; i++)
      {
        temp[i] = arr[high];
      }

      while (low <= high)
      {
        int mid = low + fb[k - 1] - 1;
        if (key < temp[mid])
        {
          high = mid - 1;
          k = k - 1;
        } else if (key > temp[mid])
        {
          low = mid + 1;
          k = k - 2;
        } else
        {
          if (mid <= high)
          {
            return mid;
          } else
          {
            return high;
          }
        }
      }

      return -1;
    }

    private static void createFibonacci(int[] fb)
    {
      int len = fb.length;
      fb[0] = 1;
      fb[1] = 1;
      for (int i = 2; i < len; i++)
      {
        fb[i] = fb[i - 1] + fb[i - 2];
      }
    }

    public static void main(String[] args)
    {
      int[] arr = { 0, 11, 22, 33, 54, 65, 76, 88, 98, 119, 1110 };
      System.out.println(FibonacciSearch.Fibonacci_Search(arr, 88));
    }
  }
  ```

+ 线性索引查找

  &emsp;&emsp;索引就是把一个关键字与它对应的记录相关联的过程，线性索引就是将索引项集合组织为线性结构，也称为索引表。

  1. 稠密索引

  &emsp;&emsp;对于稠密索引这个索引表来说，索引项一定是按照关键码有序排列。（下标|关键码|指针、关键码|其他数据）

  2. 分块索引

  &emsp;&emsp;分块有序，是把数据集的记录分成了若干块，并且这些块需要满足两个条件：

  1）块内无序； 2）块间有序

  &emsp;&emsp;对于分块有序的数据集，将每块对应一个索引项，这种索引方法称为分块索引。（最大关键码|块长|块首指针）

  3. 倒排索引

  &emsp;&emsp;Books and friends should be few but good.

  &emsp;&emsp;A good book is a good friend.

  &emsp;&emsp;索引项通用结构：（次关键码 | 记录号表），其中记录号表存储具有相同次关键字的所有记录的记录号（可以是指向记录的指针或是该记录的主关键字）。这样的索引方法就是倒序索引（Inverted Index）。

+ 二叉排序树

  &emsp;&emsp;二叉排序树（Binary Sort Tree **BST**）又称为二叉查找树。它或者是一颗空树，或者是具有下列性质的二叉树：

  1）若它的左子树不空，则左子树上所有结点的值均小于它的根结构的值。

  2）若它的右子树不空，则右子树上所有结点的值均大于它的根结点的值。

  3）它的左、右子树也分别为二叉排序树。
  
  - 二叉排序树的构建
  
  - 二叉排序树的增加
  
  - 二叉排序树的删除
  
  - 二叉排序树的查找
  
  - 二叉排序树的遍历
  
   ```java
      /**
       * 递归实现前序遍历
       * 前序遍历：访问根，按先序遍历左子树，按先序遍历右子树
       */
      static void preOrder(Node p) {
          if (p != null) {
              visit(p);
              preOrder(p.getLeft());
              preOrder(p.getRight());
          }
      }

      /**
       * 递归实现中序遍历
       * 中序遍历：按中序遍历左子树，访问根，按中序遍历右子树
       */
      static void inOrder(Node p) {
          if (p != null) {
              inOrder(p.getLeft());
              visit(p);
              inOrder(p.getRight());
          }
      }

      /**
       * 递归实现后序遍历
       * 后序遍历：按后序遍历左子树，按后序遍历右子树，访问根
       */
      static void postOrder(Node p) {
          if (p != null) {
              postOrder(p.getLeft());
              postOrder(p.getRight());
              visit(p);
          }
      }

      /**
       * 层次遍历
       * 通常用队列来做。先访问根节点，访问子女，再访问子女的子女（越往后的层次越低）（两个子女的级别相同）
       */
      static void levelOrder(Node p) {
          if (p == null) {
            return;
          }
          Queue<Node> queue = new LinkedList<Node>();
          queue.offer(p);
          while (queue.size() > 0) {
              Node temp = queue.poll();
              visit(temp);
              if (temp.getLeft() != null) {
                  queue.offer(temp.getLeft());
              }
              if (temp.getRight() != null) {
                  queue.offer(temp.getRight());
              }
          }
      }
  ```

+ 平衡二叉树（AVL 树）

&emsp;&emsp;平衡二叉树（Self-Balancing Binary Search Tree 或 Height-Balancing Binary Search Tree），是一种二叉排序树，其中每一个节点的左子树和右子树的高度差至多等于1。（两位俄罗斯数学家 G.MAdelson-Velskii 和 E.M.Landis 在 1962 年共同发明一种解决平衡二叉树的算法，也称 AVL 树。）

&emsp;&emsp;一棵 AVL 树是其每个结点的左子树和右子树的高度最多相差 1 的二叉查找树(空树的高度为 -1)，这个差值也称为平衡因子（其取值可以是1，0，-1，平衡因子是某个结点左右子树层数的差值）。

&emsp;&emsp;AVL 树只是实现平衡二叉树的一种方法，它还有很多的其他实现方法如`红黑树`、`替罪羊树`、`Treap`、`伸展树`等。

  + 二叉排序树结点结构

  ```c++
  /* 二叉树的二叉链表结点结构定义 */
  typedef struct BitNode /* 结点结构 */
  {
    int data; /* 结点数据 */
    int bf; /* 结点的平衡因子 -1、0、1 */
    struct BitNode *lchild, *rchild; /* 左右孩子指针 */
  }
  ```

  + 右旋操作

  ```c++
  /* 对以 P 为根的二叉排序树作右旋处理 */
  void R_Rotate(BiTree *P)
  {
    BiTree L;
    L = (*P) -> lchild; /* L 指向 P 的左子树根结点 */
    (*P) -> lchild = L -> rchild; /* L 的右子树挂接为 P 的左子树 */
    L -> rchild = (*P); 
    *P = L; /* P 指向新的根结点 */
  }
  ```

  + 左旋操作

  ```c++
  /* 对以 P 为根的二叉排序树作左旋处理 */
  void L_Rotate(BiTree *P)
  {
    BiTree R;
    R = (*P) -> rchild; /* L 指向 P 的右子树根结点 */
    (*P) -> rchild = L -> lchild; /* L 的左子树挂接为 P 的右子树 */
    L -> lchild = (*P); 
    *P = R; /* P 指向新的根结点 */
  }
  ```

  + 左平衡旋转处理函数

  ```c++
  void leftBalance(BiTree *T)
  {
    BiTree L, Lr;
    L = (*T) -> lchild; /* L 指向 T 的左子树根结点 */
    switch(L -> bf)
    {
      /* 检查 T 的左子树的平衡度，并作相应平衡处理 */
      case LH:
        (*T) -> bf = L -> EH;
        R_Rotate(T);
        break;
      case RH:
        Lr = L -> rchild;
        switch(Lr -> bf)
        {
          case LH:
            (*T) -> bf = RH;
            L -> bf = EH;
            break;
          case EH:
            (*T) -> bf = L -> bf = EH;
            break;
          case RH:
            (*T) -> bf = EH;
            L -> bf = LH;
            break;
        }
        Lr -> bf = EH;
        L_Rotate(&(*T) -> lchild);
        R_Rotate(T);
    }
  }
  ```
  
  + 主函数

  ```c++
  Status InsertAVL(BiTree *T, int e, Status *taller) /* 待插入数据元素 e, taller 反映 T 长高与否 */
  {
    if(!*T)
    {
      /* 插入新结点，树“长高”，置 taller 为 TRUE */
      /* malloc() 为一个对象在堆中分配一个 sizeof(BiTNode) 大小的内存空间,并且返回一个指向这块内存的指针；free() 为释放内存。 */
      *T = (BiTree)malloc(sizeof(BiTNode));
      (*T) -> data = e;
      (*T) -> lchild = (*T) -> rchild = NULL;
      (*T) -> br = EH;
      *taller = TRUE;
    }
    else
    {
      if(e == (*T) -> data) /* 树中已存在和 e 有相同关键字的结点则不再插入 */
      {
        *taller = FALSE;
        return FALSE;
      }
      if(e < (*T) -> data) /* 应继续在 T 的左子树中进行搜索 */
      {
        if(!InsertAVL(&(*T) -> lchild, e, taller)) /* 未插入 */
        {
          return FALSE;
        }
        if(*taller) /* 已插入到 T 的左子树中且左子树“长高” */
        {
          switch((*T) ->bf) /* 检查 T 的平衡度 */
          {
            case LH: /* 原本左子树比右子树高，需要作左平衡处理 */
              LeftBalance(T);
              *taller = FALSE;
              break;
            case EH: /* 原本左右子树等高，现因左子树增高而树增高 */
              (*T) -> bf = LH;
              *taller = TRUE;
              break;
            case RH: /* 原本右子树比左子树高，现左右子树等高 */
              (*T) -> bf = EH;
              *taller = FALSE;
              break;
          }
        }
      }
      else /* 应继续在 T 的右子树中进行搜索 */
      {
        if(!InsertAVL(&(*T) -> rchild, e, taller)) /* 未插入 */
        {
          return FALSE;
        }
        if(*taller) /* 已插入到 T 的右子树中且左子树“长高” */
        {
          switch((*T) ->bf) /* 检查 T 的平衡度 */
          {
            case LH: /* 原本左子树比右子树高，现左右子树等高 */
              (*T) -> bf = EH;
              *taller = FALSE;
              break;
            case EH: /* 原本左右子树等高，现因右子树增高而树增高 */
              (*T) -> bf = RH;
              *taller = TRUE;
              break;
            case RH: /* 原本右子树比左子树高，需要作右平衡处理 */
              RightBalance(T);
              *taller = FALSE;
              break;
          }
      }
    }
    return TRUE;
  }
  ```

  + 测试：构建一颗平衡二叉树

  ```C++
  int i;
  int a[10] = {3,2,1,4,5,6,7,10,9,8};
  BiTree T = NULL;
  Status taller;
  for(i=0; i<10; i++)
  {
    InsertAVL(&T, a[i], &taller);
  }
  ```

4. 多路查找树（B树）

  &emsp;&emsp;多路查找树（Muitl-Way Search Tree），其每一个结点的孩子数可以多于两个，且每一个结点处可以存储多个元素。由于它是查找树，所有元素之间存在某种特定的排序关系。（如：2-3树、2-3-4树、B树、B+树。）

  + 2-3树(B-树)

  &emsp;&emsp;2-3树是一棵多路查找树，其中的每一个结点都具有两个孩子（称为2个结点）或三个孩子（称为3个结点）。

  &emsp;&emsp;**一个2结点包含一个元素和两个孩子（或没有孩子）**，且与二叉排序树类似，左子树包含的元素小于该元素，右子树包含的元素大于该元素。不过，与二叉排序树不同的是，**这个2结点要么没有孩子，要么就有两个孩子，不能只有一个孩子。**

  &emsp;&emsp;**一个3结点包含一大一小两个元素和三个孩子（或没有孩子），** 一个3结点要么没有孩子，要么具有3个孩子。如果某个3结点有孩子的话，左孩子包含小于较小元素的元素，右孩子包含较大元素的元素，中间子树包含介于两元素之间的元素。

  &emsp;&emsp;**并且2-3树中所有的叶子都在同一层次上。** 2-3树复杂的地方就在于新结点的插入和已有结点的删除。

                ||8||

       ||4||              ||12||14||

    ||1|| ||6||7||  ||9||10|| ||13|| ||15||
  
  + 2-3-4树

  &emsp;&emsp;2-3-4树其实就是2-3树的扩展，包括了4结点的使用。一个4结点包含小中大三个元素和四个孩子（或没有孩子），一个4结点要么没有孩子，要么具有4个孩子。

  + B树

  &emsp;&emsp;B 树（B-Tree）是一种平衡的多路查找树，2-3 树和 2-3-4 树都是B树的特例。结点最大的孩子数目称为 B 树的阶（order），因此，2-3 树是 3 阶 B 树，2-3-4 树是 4 阶 B 树。在 B 树上查找的过程是一个顺时针查找结点和在结点中查找关键字的交叉过程。

   + B+树

  &emsp;&emsp;B+ 树是应文件系统所需而出的一种 B 树的变形树，在 B 树中，每一个元素在该树中只出现一次，有可能在叶子结点上，也有可能在分支结点上。而在 B+ 树中，出现在分支结点上的元素会被当作它们在该分支结点位置的中序后继者（叶子结点）中再次列出。另外，每一个叶子结点都会保存一个指向后一叶子结点的指针。如：
  
            |3|5|8|
  
    |1|2|3| |4|5| |6|7|8| |9|
  

  &emsp;&emsp;一棵 m 阶的 B+ 树和 m 阶的 B 树的差异在于：

    + 有 n 棵子树的结点中包含有 n 个关键字；

    + 所有的叶子结点包含全部的关键字的信息，及指向含这些关键字记录的指针，叶子结点本身依关键字的大小自小而大顺序链接；

    + 所有分支结点可以看成是索引，结点中仅含有其子树中的最大（或最小）关键字。

  &emsp;&emsp;B+ 树的结构特别适合带有范围的查找。B+ 树的插入、删除过程也都与 B 树类似，只不过插入和删除的元素都是在叶子结点上进行而已。


5. 散列表查找（哈希表）

  &emsp;&emsp;**存储位置 = f(关键字)** 散列技术是在记录的存储位置和它的关键字之间建立一个确定的对应关系 f，使得每个关键字 key 对应一个存储位置 f(key)。我们把这种对应关系 f 称为散列函数，又称为哈希（Hash）函数。采用散列技术将记录存储在一块连续的存储空间中，这块连续存储空间称为散列表或哈希表（Hash Table）。
  
  &emsp;&emsp;**散列技术既是一种存储方法，也是一种查找方法。**
  
  &emsp;&emsp;**散列技术最适合的求解问题是查找与给定值相等的记录。**

  &emsp;&emsp;**散列技术不适合一对多的存储，不适合范围查找。**
  
  + 散列函数的构造方法
  
  &emsp;&emsp;**好的散列函数：** （1）计算简单； （2）散列地址分布均匀。
  
    1. 直接定址法

    &emsp;&emsp;**f(key) = a x key + b （a、b 为常数）**，这样的散列函数优点就是简单、均匀，也不会产生冲突，但问题是要事先知道
    关键字的分布情况，适合查找表较小且连续的情况。（不常用）。
    
    2. 数字分析法
    
    &emsp;&emsp;手机号（其中前三位为接入号，如：联通、移动、电信；中间四位是 HLR 识别号，表示用户归属地；后四位才是真正的用户号。）
    抽取后四位数字再进行反转（1234 -> 4321）、右环移位（1234 -> 4123）、左环移位（1234 -> 2341）、前后相加（1234 -> 12 + 34 = 46）
    等。**数字分析法（关键字 —— 抽取）通常适合处理关键字位数比较大的情况，如果事先知道关键字的分布且关键字的若干位分布较均匀，就可以
    考虑用这个方法。**
    
    3. 平方取中法
    
    &emsp;&emsp;假设关键字是 1234，那么它的平方就是 1522756，再取中间三位为 227，用做散列地址。**平方取中法比较适合于不知道关键字
    的分布，而位数又不是很大的情况。**
    
    4. 折叠法
    
    &emsp;&emsp;折叠法是将关键字从左到右割成位数相等的几部分（最后一部分位数不够时可以短些），然后将这几部分叠加求和，并按散列表
    表长，取后几位作为散列地址。如关键字为 9876543210，散列表长为三位，则将其分为四组 987|654|321|0，然后叠加求和 
    987 + 654 + 321 + 0 = 1962，取后三位得到散列地址为 962。**折叠法事先不知道关键字的分布，适合关键字位数较多的情况。**
    
    5. 除留余数法
    
    &emsp;&emsp;
    
    6. 随机数法
    
    &emsp;&emsp;
    
    
    + 处理散列冲突的方法
    
    1. 开放地址法
    
    &emsp;&emsp;
    
    2. 再散列函数法
    
    &emsp;&emsp;
    
    3. 链地址法
    
    &emsp;&emsp;
    
    4. 公共溢出区法
    
    &emsp;&emsp;
    
    
    + 散列表查找实现
    
    


## 九、排序（Sort）


