# flutter阅读笔记  

Flutter是Google的UI工具包，可通过单个代码库为移动，网络和台式机构建漂亮的，本机编译的应用程序 。  

#### widgets  
Flutter小部件是使用从React汲取灵感的现代框架构建的。中心思想是使用小部件构建UI。小部件描述了给定其当前配置和状态的视图外观。当窗口小部件的状态发生变化时，窗口小部件将重新构建其描述，框架会将其与之前的描述进行区分，以便确定在底层渲染树中从一种状态转换到另一种状态所需的最小更改。  

##### 常用widget  
Flutter有一套丰富、强大的基础widget，其中以下是很常用的：  
* Text：该 widget 可让创建一个带格式的文本  
* Row、 Column： 这些具有弹性空间的布局类Widget可让您在水平（Row）和垂直（Column）方向上创建灵活的布局。其设计是基于web开发中的Flexbox布局模型。  
* Stack： 取代线性布局 (译者语：和Android中的LinearLayout相似)，Stack允许子 widget 堆叠， 你可以使用 Positioned 来定位他们相对于Stack的上下左右四条边的位置。Stacks是基于Web开发中的绝度定位（absolute positioning )布局模型设计的。  
* Container： Container 可让您创建矩形视觉元素。container 可以装饰为一个BoxDecoration, 如 background、一个边框、或者一个阴影。 Container 也可以具有边距（margins）、填充(padding)和应用于其大小的约束(constraints)。另外， Container可以使用矩阵在三维空间中对其进行变换  

#### MaterialApp

为了继承主题数据，widget需要位于MaterialApp内才能正常显示， 因此我们使用MaterialApp来运行该应用。

在MyAppBar中创建一个Container，高度为56像素（像素单位独立于设备，为逻辑像素），其左侧和右侧均有8像素的填充。在容器内部， MyAppBar使用Row 布局来排列其子项。 中间的title widget被标记为Expanded, ，这意味着它会填充尚未被其他子项占用的的剩余可用空间。Expanded可以拥有多个children， 然后使用flex参数来确定他们占用剩余空间的比例。

MyScaffold 通过一个Column widget，在垂直方向排列其子项。在Column的顶部，放置了一个MyAppBar实例，将一个Text widget作为其标题传递给应用程序栏。将widget作为参数传递给其他widget是一种强大的技术，可以让您创建各种复杂的widget。最后，MyScaffold使用了一个Expanded来填充剩余的空间，正中间包含一条message。

##### 使用Materia组件  
Flutter提供了许多widgets，可帮助您构建遵循Material Design的应用程序。Material应用程序以MaterialApp widget开始， 该widget在应用程序的根部创建了一些有用的widget，其中包括一个Navigator， 它管理由字符串标识的Widget栈（即页面路由栈）。Navigator可以让您的应用程序在页面之间的平滑的过渡。 是否使用MaterialApp完全是可选的，但是使用它是一个很好的做法。

