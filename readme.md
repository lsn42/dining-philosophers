# 哲学家进餐
## 一、课程设计目的
掌握基本的同步与互斥算法，掌握进程并发执行的原理，及其所引起的同步、互斥问题的方法。
## 二、课程设计内容
自己编写信号量和 wait、signal 操作的模拟程序，然后用它们解决不死锁的哲学家问题或者读者-写者问题。
## 三、要求及提示
本题目必须单人完成。
### 解决不死锁的哲学家问题，要求把哲学家们的活动过程用文字或图形可视化形式表示出来。 
提示：首先设置一个“PCB”数组或队列，其中一个字段表示“阻塞原因兼阻塞标志”，本实验中，该数组有 5 个元素表示 5 个哲学家即可。它们随机提出申请以及进行“思考”和“吃”的行为。再设一个“筷子”数组。还需要设置哪些数据结构以及需要哪些字段自己考虑。

### 可能用到的 API 函数：
|函数名|用途|
|:----|:----|
|CreateThread()|在调用进程的地址空间上创建一个线程|
|ExitThread()|用于结束当前线程|
|Sleep()|可在指定的时间内挂起当前线程|
|CreateMutex()|创建一个互斥对象，返回对象句柄|
|OpenMutex()|打开并返回一个已存在的互斥对象句柄，用于后续访问|
|ReleaseMutex()|释放对互斥对象的占用，使之成为可用|
|WaitForSingleObject()|可在指定的时间内等待指定对象为可用状态|
|InitializeCriticalSection()|初始化临界区对象|
|EnterCriticalSection()|等待指定临界区对象的所有权|
|LeaveCriticalSection()|释放指定临界区对象的所有权|
|CreateSemaphore()|创建一个信号量对象|
|ReleaseSemaphore()|将所指信号量加上指定大小的一个量|