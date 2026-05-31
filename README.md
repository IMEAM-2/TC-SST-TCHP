# Tropical Cyclone OISST SST Cooling Statistics

This repository provides a compact dataset of tropical cyclone track points and nearby sea surface temperature statistics based on best-track data and NOAA OISST daily SST.

For each 65 kt+ tropical cyclone record, the dataset includes storm location, intensity, translation speed, motion direction, center ocean/land flag, and R100/R200 OISST-based SST statistics. The SST metrics include the mean SST before the record time, the minimum SST after the record time, and an approximate cooling value.

This dataset is intended for tropical cyclone case review, visualization, and exploratory climate statistics. It is not an official operational product.

In addition to the compact OISST-based tables, this repository also includes selected SST and OHC/TCHP figures for historical tropical cyclone cases. These figures are intended for case review and visual reference, and they do not necessarily cover all storms in the tabular dataset.

The figure sources include Mercator Ocean products, SODA ocean reanalysis, REMSS SST/ocean products, and related datasets. Since these products differ in spatial resolution, temporal coverage, and data assimilation methods, the figures should mainly be used for qualitative comparison and case-based illustration rather than as a uniform quantitative dataset.

Data sources

The tropical cyclone track records used in this dataset are merged from several best-track-like sources. The current merging priority is:

ChestnutMeow / MIWU self-evaluated bdeck
https://github.com/ChestnutMeow111/ChestnutMeow_bdeck
XRQA self-evaluated bdeck
https://github.com/CyanideCN/xrqa_bdeck_data/
USA best-track-like files, including NHC / CPHC / JTWC-style records where available.

IBTrACS v04r01 is used only for storm name matching and metadata assistance, not as the primary track source.

The sea surface temperature statistics are calculated from NOAA OISST daily 0.25° SST data. For each selected tropical cyclone record, R100/R200 circular-mean SST metrics are calculated around the best-track center.

Because part of the track data comes from self-evaluated bdeck datasets, users should check the `source` field and apply their own filtering criteria when using the data for formal analysis.

本仓库整理了一份基于 best-track 路径资料与 NOAA OISST 日海温资料的热带气旋海温统计派生表。

数据针对 65 kt 及以上热带气旋报点，统计了中心位置、强度、移速、移动方向、中心是否位于海上，以及中心附近 R100/R200 范围内的 OISST 海温指标。主要指标包括报点前期平均海温、报点后期最低海温，以及由此估算的近似冷却量。

该数据主要用于气象爱好者进行个例检视、简单统计和可视化探索，不是官方业务产品，也不代表瞬时眼墙下方真实海温。

此外，仓库中还保存了部分历史热带气旋个例的 SST、OHC/TCHP 图像，用于辅助展示强台风经过前后的海洋热力环境。这些图像并不一定覆盖全部系统，主要作为个例检视和可视化参考。

相关图像的数据来源包括 Mercator Ocean、SODA 海洋再分析资料、REMSS 海温/海洋产品等。不同资料的时空分辨率、同化方法和时间覆盖并不完全一致，因此图像结果更适合作为定性对比和个例辅助，而不建议直接与 OISST 简表指标混合作为同一套定量统计。

数据来源

本数据集使用多套 best-track-like 热带气旋路径资料合并而成。目前路径资料的合并优先级为：

ChestnutMeow / MIWU 自评 bdeck
https://github.com/ChestnutMeow111/ChestnutMeow_bdeck
XRQA 自评 bdeck
https://github.com/CyanideCN/xrqa_bdeck_data/
USA 系 best-track-like 文件，包括可用的 NHC / CPHC / JTWC 风格路径资料。

IBTrACS v04r01 主要用于热带气旋名称匹配和元数据辅助，不作为主要路径来源。

由于部分路径资料来自自评 bdeck 数据集，使用者在进行正式统计或研究时，建议结合 `source` 字段自行筛选和核查。

海温统计基于 NOAA OISST daily 0.25° SST 资料计算。对每个筛选出的热带气旋报点，以 best-track 中心为圆心，计算 R100/R200 范围内的圆形平均海温及相关冷却指标。

