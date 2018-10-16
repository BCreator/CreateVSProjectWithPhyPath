# ConvertVSProjectWithPhyPath

- 无论多么喜欢GNU那套东西，但不得不说VS是最好用的IDE，对GNU体系支持也越来越好，哪怕当成一个工程代码阅读器也很有用。特别是每个代码文件都能生成轮廓，还有其内建及各种Extensions提供了有不少便于代码阅读以及了解代码调用关系的功能。但一些功能不是简单的打开一个代码物理目录就能激活，还是需是sln模式。而此工具可以帮到这一点。
- 这是个把VS Community 2017自带的“New->Project From Existing Code...”（以下简称PFC)弄出  来的工程，增加与物理目录结构相同的Filter体系的工具。原始代码来源于文章，感谢原作者：
  https://blog.csdn.net/u012852324/article/details/49686401
- 本工具的意义只是为了使用VS来阅读代码，使用VS的一些在Folder和CMake等模式下无效的功能，并不是用来Build。
- 运行后，会提示输入功能filter路径（*..vcxproj.filters）。2017以外的filters格式也许一样，都能支持，我没花时间测试。
- 改进让所有类型的文件都能被路径化，去掉了次数限制，支持了无Filter子的情况（None类型），请见下面houstond注释。但不知道还有其他问题。
- PFC本来就把文件目录的大小写转乱了，所以此工具对大小写也是乱的，在非Windows的VS可能就会有问题，我没花时间测试。
- PFC对一些不支持的文件是不加入生成的，这可能取决于，执行转化的时候，自己对扩展名列表的选择，我没花时间测试。

graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;


dasdgd


gantt
        dateFormat  YYYY-MM-DD
        title Adding GANTT diagram functionality to mermaid
        section A section
        Completed task            :done,    des1, 2014-01-06,2014-01-08
        Active task               :active,  des2, 2014-01-09, 3d
        Future task               :         des3, after des2, 5d
        Future task2               :         des4, after des3, 5d
        section Critical tasks
        Completed task in the critical line :crit, done, 2014-01-06,24h
        Implement parser and jison          :crit, done, after des1, 2d
        Create tests for parser             :crit, active, 3d
        Future task in critical line        :crit, 5d
        Create tests for renderer           :2d
        Add to mermaid                      :1d
        
        
gdgdgd

sequenceDiagram
    participant Alice
    participant Bob
    Alice->John: Hello John, how are you?
    loop Healthcheck
        John->John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br/>prevail...
    John-->Alice: Great!
    John->Bob: How about you?
    Bob-->John: Jolly good!
    

