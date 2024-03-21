This code is for a scheduling method based on place-timed Petri nets and an A* search algorithm. The design of the heuristic function in Petri-net-based A* search significantly impacts the efficiency and result quality of scheduling robotic cellular manufacturing (RCM) systems. Previous work in such designs lacks consideration for some key features such as token remaining time, alternative routes, weighted arcs, multiple resource copies, and batch-processing ability. This paper proposes a novel admissible heuristic function tailored to address these challenges. It is designed from the perspective of maximal time usage of each part token. In addition, it is admissible, which guarantees that its obtained schedules are optimal. Most importantly, it is highly informative, enabling efficient scheduling of generalized PNs of RCM systems.

The project is developed using Visual Studio 2022 with C# on the Windows platform.

https://github.com/PNOptimizer/NewHDesign/assets/125330242/0caf9a65-1bb3-4157-9a82-98866fafc9b1


用途与运行环境：
本程序平台采用C#实现我们所提出的基于Petri网的类A*搜索算法，详细算法描述请参见我们的英文专著及相应论文。

Bo Huang, MengChu Zhou. Supervisory Control and Scheduling of Resource Allocation Systems. Hoboken, NJ, USA: John Wiley & Sons (IEEE-Wiley), July 2020.
Bo Huang, MengChu Zhou, XiaoYu Sean Lu, and Abdullah Abusorrah. Scheduling of Resource Allocation Systems with Timed Petri Nets: A Survey. ACM Computing Surveys, Feb. 2023, 55(11): 1-27. 


本平台基于Visual Studio 2008开发，安装VS2008后直接双击后缀名为.sln或.csproj文件即可打开运行。如果采用的不同版本的VS则可能无法直接打开，此时需要新建空白C# Console工程，将Main.cs, AStar.cs和Heap.cs三个文件，以及bin文件夹和帮助文档拷贝至新建工程的所在目录，然后在工程中Project->add existing item将三个cs文件加入即可。（将老的程序备份，并创建新的程序也是此流程）

运行：打开main.cs，点击Debug->Start Debugging(F5)

平台组成：
Main.cs: 主程序，输入一些用户参数。
AStar.cs: 搜索程序，定义了两个类AStarNode和AStar。
Heap.cs: 堆栈操作函数，用于处理OPEN, CLOSED之类的堆栈操作，通常不用改动，直接调用即可。
Bin/Debug文件夹：存放输入和输出文件。输入文件，对于一个Petri网，需要给出两个输入文件，其中xxx_matrix.txt放置Petri网的关联矩阵的转置矩阵（即行为变迁，列为托肯），xxx_init.txt放置起始标识，库所操作时间信息，和目的标识。输出文件为0result.txt。

版本更新说明：
https://static.app.yinxiang.com/embedded-web/profile/#/join?guid=0f885707-2f1a-4ea6-9fab-f2479b6dd6b5&sharedNotebookGuid=&channel=copylink&shardId=s34&ownerId=25641086

For any inquiries or issues, please reach out to us at huangbo@njust.edu.cn.

March 21, 2024.
