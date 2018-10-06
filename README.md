# CVSProjectWithPhyPath

- 这是个把把VS Community 2017自带的“New->Project From Existing Code...”（以下简称
  PFC)弄出  来的工程，增加与物理目录结构相同的Filter体系的工具。原始代码来源于文章，
  感谢原作者：
  https://blog.csdn.net/u012852324/article/details/49686401
- 本工具的意义只是为了使用VS来阅读代码，使用VS的一些在Folder和CMake等模式下无效的功
  能，并不是用来Build。
- 运行后，会提示输入功能filter路径（*..vcxproj.filters）。2017以外的filters格式也许
  一样，都能支持，我没花时间测试。
- 改进让所有类型的文件都能被路径化，去掉了次数限
  制，支持了无Filter子的情况（None类型），请见下面houstond注释。但不知道还有其他问题。
- PFC本来就把文件目录的大小写转乱了，所以此工具对大小写也是乱的，在非Windows的VS可能
  就会有问题，我没花时间测试。
- PFC对一些不支持的文件是不加入生成的，这可能取决于，执行转化的时候，自己对扩展名列表
  的选择，我没花时间测试。
