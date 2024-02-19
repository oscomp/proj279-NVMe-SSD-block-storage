# proj279-NVMe-SSD-block-storage
## 标题

基于NVMe SSD的块存储实时性设计与实现

## 项目描述

《中国制造2025》指出今年来我国载人航天、大型飞机、北斗卫星导航等重大技术装备取得突破，这些设备都大量用到了实时系统和技术。近年来发展迅速的无人驾驶汽车、无人机、实时数据库等对块存储的实时性有了较高要求。同时，近年来新型存储硬件，如NVMe SSD快速发展，它们具有非易失性、抗冲击、低功耗和快速访问时间等特性，非常适合应用在实时块存储中。

由于无人驾驶算法、实时数据库等大都运行在linux操作系统上，所以本项目是在linux平台上增强以NVMe SSD为存储介质的块存储实时性。为此，需要设计相应的机制来提高linux块存储的实时性，比如根据进程的优先级将块存储IO进行分类的IO调度器，优先处理高优先级任务的IO请求，充分利用NVMe SSD的特性等。

由于无人驾驶算法、实时数据库等的块存储IO特点为：实时性要求较高的少量小文件读，同时可能存在实时性要求低的大量读写。为此，需要在保证实时性IO请求的前提下，尽量减少对块存储IO吞吐量的影响。

本项目的目的是鼓励对操作系统感兴趣的师生增强对linux内核的分析和改造能力，并将内核分析改造的方法和心得共享给大家。 这个项目的特点是：分析linux块存储IO栈，设计相应机制以提高liunx块存储的实时性，使得学生可以更好地理解和掌握linux的块存储子系统。

## 预期目标

- 分析linux块存储IO栈，找出影响块存储实时性的主要几个因素，并进行修改优化；
- 设计实现可以根据进程优先级分类的IO调度器，在提高linux块存储IO实时性的前提下不过大影响块存储IO吞吐量；

## 特征

- 扩展linux IO调度器，使linux块存储系统可根据进程优先级进行IO调度；
- 文档、代码、问题、答疑交互过程都开放和开源的；
- 个人PC、服务器等都可作为实验平台；
- 使用性能较高的NVMe SSD作为存储介质。

## 已有参考资料

- [Linux](https://www.kernel.org/)
- [Linux block documents](https://elixir.bootlin.com/linux/v5.19.17/source/Documentation/block)
- [Linux block analysis](https://blog.csdn.net/hu1610552336/article/details/111464548)
- [Linux Block IO: Introducing Multi-queue SSD Access onMulti-core Systems](https://kernel.dk/systor13-final18.pdf)

## 赛题分类

2.3 操作系统内核大类-->2.3.6 内核完善

## 参赛要求

- 以小组为单位参赛，最多三人一个小组，且小组成员是来自同一所高校的本科生或研究生
- 允许学生参加大赛的多个不同题目，最终自己选择一个题目参与评奖
- 请遵循“2024全国大学生操作系统比赛”的章程和技术方案要求

## 难度

中等。

## License

GPL-3.0 License

## 所属赛道

2024全国大学生操作系统比赛的“OS功能挑战”赛道

## 项目导师

- 姓名：董攀
- 单位：国防科技大学
- email：[pandong@nudt.edu.cn](mailto:pandong@nudt.edu.cn)
