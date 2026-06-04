# Tropical Cyclone SST Statistics

This repository provides compact datasets of tropical cyclone track points and nearby sea surface temperature statistics based on merged best-track-like tropical cyclone records and daily SST products.

The main SST statistics are based on NOAA OISST daily 0.25° SST. For each 65 kt+ tropical cyclone record, the dataset includes storm location, intensity, translation speed, motion direction, center ocean/land flag, and R100/R200 OISST-based SST statistics. The SST metrics include the mean SST before the record time, the minimum SST after the record time, and an approximate cooling value.

This dataset is intended for tropical cyclone case review, visualization, and exploratory climate statistics. It is not an official operational product.

In addition to the compact OISST-based tables, this repository also includes a COBE-SST3-based comparison table for 65 kt+ tropical cyclone records from 1978 to 2024. The COBE-SST3 table uses the same basic method as the OISST table: for each selected best-track record, circular-mean SST is calculated within R100 and R200 around the storm center.

The compact SST metrics include:

* `sst_r100_pre3_mean` / `sst_r200_pre3_mean`: mean SST from 3 days before to 1 day before the record time
* `sst_r100_min_0p7` / `sst_r200_min_0p7`: minimum SST from the record day to 7 days after
* `Cooling_R100` / `Cooling_R200`: `min_0p7 - pre3_mean`, where negative values indicate cooling

The COBE-SST3 comparison is mainly intended for background SST sensitivity testing. Preliminary checks suggest that COBE-SST3 is relatively smooth for storm-scale cold-wake signals, so COBE-based cooling metrics should be interpreted with caution and are not used as the primary estimate of tropical-cyclone-induced SST cooling.

In addition to the tabular datasets, this repository also includes selected SST and OHC/TCHP figures for historical tropical cyclone cases. These figures are intended for case review and visual reference, and they do not necessarily cover all storms in the tabular dataset.

The figure sources include Mercator Ocean products, SODA ocean reanalysis, REMSS SST/ocean products, NOAA OISST, and related datasets. Since these products differ in spatial resolution, temporal coverage, and data assimilation methods, the figures should mainly be used for qualitative comparison and case-based illustration rather than as a uniform quantitative dataset.

## Data sources

The tropical cyclone track records used in this dataset are merged from several best-track-like sources. The current merging priority is:

1. ChestnutMeow / MIWU self-evaluated bdeck
   https://github.com/ChestnutMeow111/ChestnutMeow_bdeck

2. XRQA self-evaluated bdeck
   https://github.com/CyanideCN/xrqa_bdeck_data/

3. USA best-track-like files, including NHC / CPHC / JTWC-style records where available.

IBTrACS v04r01 is used only for storm name matching and metadata assistance, not as the primary track source.

The main SST statistics are calculated from NOAA OISST daily 0.25° SST data. The COBE-SST3 table is provided as an additional background SST comparison dataset. For each selected tropical cyclone record, R100/R200 circular-mean SST metrics are calculated around the best-track center.

Because part of the track data comes from self-evaluated bdeck datasets, users should check the `source` field and apply their own filtering criteria when using the data for formal analysis.

---

26.6.4
## REMSS MW OI comparison

A REMSS Microwave OI SST table is also provided for 65 kt+ tropical cyclone records from 1998 onward. REMSS MW OI is a microwave-only daily SST product with 0.25° resolution, which is more suitable than infrared-dominated products for observing SST under cloudy tropical cyclone conditions.

The REMSS MW OI table uses the same compact metrics as the OISST table:

- `sst_r100_pre3_mean` / `sst_r200_pre3_mean`
- `sst_r100_min_0p7` / `sst_r200_min_0p7`
- `Cooling_R100` / `Cooling_R200`


# 热带气旋 SST 与 TCHP 统计数据

本仓库整理了一份基于多源 best-track-like 路径资料与日海温资料的热带气旋海温统计派生表。

主海温统计基于 NOAA OISST daily 0.25° SST 资料。数据针对 65 kt 及以上热带气旋报点，统计了中心位置、强度、移速、移动方向、中心是否位于海上，以及中心附近 R100/R200 范围内的 OISST 海温指标。主要指标包括报点前期平均海温、报点后期最低海温，以及由此估算的近似冷却量。

该数据主要用于气象爱好者进行个例检视、简单统计和可视化探索，不是官方业务产品，也不代表瞬时眼墙下方真实海温。

除 OISST 主表外，本仓库还提供了一份基于 COBE-SST3 的 65 kt 及以上热带气旋报点对照表，时间范围为 1978–2024 年。COBE-SST3 表采用与 OISST 表基本一致的方法：对每个筛选出的 best-track 报点，以风暴中心为圆心，计算 R100 和 R200 范围内的圆形平均 SST。

精简海温指标包括：

* `sst_r100_pre3_mean` / `sst_r200_pre3_mean`：报点前 3 天至前 1 天平均 SST
* `sst_r100_min_0p7` / `sst_r200_min_0p7`：报点当天至后 7 天最低 SST
* `Cooling_R100` / `Cooling_R200`：`min_0p7 - pre3_mean`，负值表示冷却

COBE-SST3 对照表主要用于检验背景海温的敏感性。初步检查发现，COBE-SST3 对风暴尺度冷尾流信号较为平滑，因此 COBE 计算得到的冷却量仅供参考，不作为本项目中热带气旋过境降温的主要估计。

此外，仓库中还保存了部分历史热带气旋个例的 SST、OHC/TCHP 图像，用于辅助展示强台风经过前后的海洋热力环境。这些图像并不一定覆盖全部系统，主要作为个例检视和可视化参考。

相关图像的数据来源包括 Mercator Ocean、SODA 海洋再分析资料、REMSS 海温/海洋产品、NOAA OISST 等。不同资料的时空分辨率、同化方法和时间覆盖并不完全一致，因此图像结果更适合作为定性对比和个例辅助，而不建议直接与简表指标混合作为同一套定量统计。

## 数据来源

本数据集使用多套 best-track-like 热带气旋路径资料合并而成。目前路径资料的合并优先级为：

1. ChestnutMeow / MIWU 自评 bdeck
   https://github.com/ChestnutMeow111/ChestnutMeow_bdeck

2. XRQA 自评 bdeck
   https://github.com/CyanideCN/xrqa_bdeck_data/

3. USA 系 best-track-like 文件，包括可用的 NHC / CPHC / JTWC 风格路径资料。

IBTrACS v04r01 主要用于热带气旋名称匹配和元数据辅助，不作为主要路径来源。


26.6.4
## REMSS MW OI 对照数据

本仓库还提供了一份基于 REMSS Microwave OI SST 的 65 kt+ 热带气旋报点对照表，时间范围从 1998 年以后开始。REMSS MW OI 是仅基于微波资料的 0.25° 日海温产品，相比主要依赖红外资料的高分辨率产品，更适合在热带气旋云区条件下观测海温变化。

REMSS MW OI 表使用与 OISST 表相同的精简指标：

- `sst_r100_pre3_mean` / `sst_r200_pre3_mean`
- `sst_r100_min_0p7` / `sst_r200_min_0p7`
- `Cooling_R100` / `Cooling_R200`

相较于 OISST 和 COBE-SST3，REMSS MW OI 表主要作为偏向冷尾流观测的对照数据。但由于该资料在近岸、陆地附近、海冰区或质量控制区域可能存在缺测，`center_has_sst` 仅表示风暴中心最近的 REMSS SST 格点在报点当天是否有有效 SST，不应被严格解释为海陆判定。




