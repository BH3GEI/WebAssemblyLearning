属于是补档，一个月前就开始了，但大跃进式地学习，学完就忘
特此整理一下

## 不臭不长的介绍

取代js密集计算而不是取代js，编译一次就可以到处运行，新的二进制格式的开放标准

![image](https://github.com/BH3GEI/WebAssemblyLearning/assets/58540850/c70b0e61-97d1-4a16-94ba-f28c7a088d0a)

前端、游戏、动画、区块链、容器、虚拟机

- **Rust**
  - 工具链完备，但debug工具还有待完善
  - 不用担心内存问题
  - 导出包自带ts声明

- **C/C++**
  - 主要应用于老项目的遗留
  - 各种编译 各种烦
  - 需要注意内存问题 各种糟心 人活不了几年 就别Cpp

- 其他的都有运行时 性能有问题

还是rust吧

微软的Blazor，C#，visual studio 很丝滑，但emmm

- **缺点**
  - 文件太大
  - 依赖容量太大
  - 有运行时

- **优点**
  - 开发简单
  - 调试傻瓜

对Rust支持最好的IDE是微软家的Vscode，Rust对WebAssembly调试问题有望解决

- Rust能用来做什么 或是为什么要选择Rust
  - WebAssembly Rust支持的最好
  - WebAssembly是Rust全村的希望
- WebAssembly始于Rust，是Rust的主场
- Rust 近期比较多的应用场景
  - web开发 微服务
  - 区块链
  - WebAssembly

基本都和WebAssembly有关系

- **WebAssembly技术受众**

- 前端
- 后端 微服务
- 云服务、容器化、运维
- 游戏开发
- 音视频开发
- 区块链从业者
- 
## 开始code
### wat2wasm网站
.WASM是binary
.WAT是text

- wasm有一种基于文本助记的表示形式WAT如下
  ```wat
  (module
    (func (export "addTwo") (param i32 i32) (result i32)
      local.get 0
      local.get 1
      i32.add))
  ```
- wat通过wabt工具编译成二进制文件wasm

chrome会简单地将wasm二进制表示编译为wat，可以像调试js一样进行打断点等
但是这些只是一些代码段，并不是完整的.wat


- [https://webassembly.github.io/wabt/demo/wat2wasm/](https://webassembly.github.io/wabt/demo/wat2wasm/)
  跟他妈汇编一样
- 在左侧的文本区域中输入 WebAssembly 文本。右侧要么显示错误，要么显示带有生成二进制文件描述的日志。
- 还可以下载生成的wasm二进制文件
