CFD Model HydroFlow Supplemental Tools
===  
本项目为计算流体力学程序HydroFlow-IBM辅助工具开发，主要应用于网格文件生成，计算文件预处理、数据分析、计算结果可视化等工作。     
## mesh
网格生成程序MixGrid数据文件编写及简易可视化。
- **BdCreate**  
> 分段边界信息生成，可生成任意划分直线边界与弧边界并相应组合，更多功能开发中......

- **MeshFile**  
> MixGrid网格文件生成，可生成笛卡尔结构化网格、非结构网格、柱面网格、网格局部加密等。
  
- **IbFile**  
> 浸没边界法虚拟边界文件生成，二维边界通过曲线方程离散，三维边界通过ICEM建模导出。 

- **MeshCustom**  
> 自定义网格文件生成，用于对具体算例所需要的网格文件自由修改。  

## ocerm
计算文件预处理，包括头文件信息修改、网格文件修改、边界条件设置等部分。
- **IncludeCreate**  
> 初始边界条件迭代文件生成。  
> 1. create_qbc：入口流量边界条件迭代文件生成。
> 2. create_gauge：水位与流速监测点设置。
> 3. set_kb：非均匀垂向网格剖分坐标计算。

- **IncludeModify**
> 网格文件与计算头文件修改。  
> 1. modify_grd，modify_cuv：网格垂向分层与边界位置修正。
> 2. modify_inf：计算头文件网格信息修正。
> 3. modify_qbc，modify_ebc：入口与出口边界条件设置。

## paperfig
数据结果分析与可视化，应用于论文插图绘制。
- **VisIBM**  
> 浸没边界法虚拟边界识别相关可视化。
> 1. ibm_gc_2D，ibm_gc_3D：二维与三维边界识别可视化。
> 2. ibm_image_2D，ibm_wm_2D：边界镜像点与插值单元识别可视化。
> 3. ibm_vec：边界单元切向与法向速度场结果分析。
> 4. ibm_df_2D：Delta函数影响域可视化。
> 5. ibm_mesh：网格单元识别可视化。
> 6. ibm_ani_2D：运动边界动画化结果绘制。

- **VisResult**  
> 算例计算结果分析与可视化。
> 1. u_boundary：底部边界层速度剖面分布可视化。
> 2. u_Cp，u_CDCL：压力系数，阻力系数，升力系数数值模拟结果分析。
> 3. u_mid：半水深处圆柱绕流沿直径径向速度分布与监测点速度随时间变化数值模拟结果分析。
> 4. u_result：具体算例数值模拟结果与实验数据对比分析。
> 5. u_fft：基于快速傅里叶变换的流场数值模拟频谱分析。
> 6. wave_fig：数值水波初始波形可视化。

## get_data  
简易的数据提取工具，用于获取文献实验结果图中原始数据，使用OpenCV开发，更多功能待实现中...  
