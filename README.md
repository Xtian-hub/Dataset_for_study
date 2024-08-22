# 研究可能会用到的数据集
用于收集研究中可能会用到的数据集或数据集链接

## 用于加速开发和基准测试太阳预测方法的综合数据集
## A comprehensive dataset for the accelerated development and benchmarking of solar forecasting methods
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
