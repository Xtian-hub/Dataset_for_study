# 研究可能会用到的数据集
用于收集研究中可能会用到的数据集或数据集链接

## 1 用于加速开发和基准测试太阳预测方法的综合数据集
## 1 A comprehensive dataset for the accelerated development and benchmarking of solar forecasting methods
### 直达链接
https://zenodo.org/records/2826939
### 描述
此存储库包含全面的太阳辐照度、成像和预报数据集。 
此版本的目标是为研究界提供标准化的太阳和气象数据集，以加速预测方法的开发和基准测试。 
数据包括三年（2014-2016 年）质量控制的 1 分钟分辨率全球水平辐照度和加利福尼亚州直接法向辐照度地面测量数据。 
此外，我们还提供常用外生变量的重叠数据，包括天空图像、卫星图像、数值天气预报和天气数据。 
我们还包括基线模型的示例代码，用于对更复杂的模型进行基准测试。
### 文件 
  · Folsom_irradiance.csv                           主要的一分钟 GHI、DNI 和 DHI 数据。  
  · Folsom_weather.csv                              主要一分钟天气数据。  
  · Folsom_sky_images_{YEAR}.tar.bz2    主 Tar 档案，包含 2014、2015 和 2016 年每隔 1 分钟捕获的白天天空图像，使用 bz2 压缩。  
  · Folsom_NAM_lat{LAT}_lon{LON}.csv   对距离目标位置最近的四个节点的主要 NAM 预测。{LAT} 和 {LON} 被本文表 I 中列出的节点坐标替换。   
  · Folsom_sky_image_features.csv          从天空图像中得出的次要特征。  
  · Folsom_satellite.csv                              以目标位置为中心的辅助 10 像素 x 10 像素 GOES-15 图像。   
  · Irradiance_features_{horizo​​n}.csv          不同预测范围的二次辐照度特征（{horizo​​n} 1⁄4 {小时内，白天，日前}）。   
  · Sky_image_features_intra-hour.csv       用于小时内预报发布时间的次要天空图像特征。   
  · Sat_image_features_intra-day.csv         用于日内预报发布时间的二次卫星图像特征。   
  · NAM_nearest_node_day-ahead.csv     为距离目标位置最近的节点准备的用于日内预报的二次 NAM 预报（GHI、用 DISC 算法计算的 DNI 和总云量）。  
  · Target_{horizo​​n}.csv                              不同预测范围的次要目标数据。  
  · F orecast_{horizo​​n}.py                           代码 Python 脚本用于创建不同范围的预测。   
  · Postprocess.py                                      代码 Python 脚本用于计算所有预测的误差度量。  
### Additional details
#### Related works
Is compiled by 10.1063/1.5094494  (DOI)
#### References
Pedro, H.T.C., Larson, D.P., Coimbra, C.F.M., 2019. A comprehensive dataset for the accelerated development and benchmarking of solar forecasting methods. Journal of Renewable and Sustainable Energy 11, 036102. https://doi.org/10.1063/1.5094494

## 2 通过卫星图像检测可用于安装光伏板的屋顶面积
## 2 Detecting available rooftop area from satellite images to install photovoltaic panels
### 直达链接
https://github.com/riccardocadei/photovoltaic-detection?tab=readme-ov-file#methods
### 主题：检测可用于光伏安装的屋顶面积  
该项目的目标是在瑞士（日内瓦）的航拍图像中分割出可用于安装屋顶光伏 (PV) 板的区域，即在排除烟囱、窗户、现有 PV 装置和其他所谓的“上层建筑”后屋顶上的区域。该任务是一个逐像素的二元语义分割问题。我们感兴趣的是像素可以被归类为 PV 装置的“合适区域”的类别。
![image](https://github.com/user-attachments/assets/345915d3-e853-44f1-92b8-73eac0413781)
### 数据
· 输入的航空图像是 PNG 格式的 RGB 航空图像，每张图像尺寸为 250×250×3，像素大小为 0.25×0.25 m^2。  
· 数据集中的所有图像都是使用中的有用函数手动标记的labelling_tool。  
· 标记的图像是一个二进制掩码，其中 PV 区域中的像素为 1，否则为 0。  
· 训练之前，对原始输入图像进行饱和度和经典归一化变换。  
· 实时数据论证仅应用于训练集，通过随机水平或垂直翻转图像或旋转九十度。  
· 我们的模型的输出再次是二值图像，其中，如果像素位于 PV 区域的概率大于固定阈值，则该像素为一。  
· 训练/验证/测试比例：80/10/10％  
### 方法
我们使用基于 U-net 的卷积神经网络 (CNN) 模型和自适应学习算法对其进行训练，计算 Iou 和 Acurrancy 来评估性能。  
我们首先在整个数据集上训练模型，然后只关注特定类别的图像，即住宅区  
### 结果
我们能够在像素级自动检测测试图像中的可用屋顶面积，性能可与最先进的技术相媲美。特别是，仅关注住宅区图像，我们在测试集上获得的准确率约为 0.97，交并比指数为 0.77，仅使用 244 张图像进行训练。下面是测试集上的预测示例。  
![image](https://github.com/user-attachments/assets/3013bf41-f811-4ce1-a8f3-cb8c30300009)  

## 3 NSRDB: National Solar Radiation Database
## 3 国家太阳辐射数据库
### 直达链接
### 描述
该数据集中有时间动态变化的太阳辐射值，精度可达到每半小时变化。  
![image](https://github.com/user-attachments/assets/c091b628-361b-4f74-938d-71b84ab33dfc)  
![image](https://github.com/user-attachments/assets/052f3cf1-b063-46ae-ada1-bea97ae93ce2)  


