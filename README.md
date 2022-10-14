# 供应链项目管理（微观）
1. 项目目标
    1. NPI系统搭建（system engineering)
        1. 子项目接口
        2. Flow (Provide, transfer), Stable(Maintain)
        3. Flow Disruption Risk(Estimation, Safety inventory, Plan B)

    2. 建模优化(object function aimed at most)
        1. 降低cost
        2. 降低lead time
        3. 降低quene
        4. 提升accuracy
        5. 提升stability

    3. 稳定性 Resilience (constraints aimed at least)
        1. 吸收波动（Buffer）
        2. Risk indetificaton & metigation (Plan B)
        3. 针对未来变化的可扩展性、前瞻性adaptation

2. 基础数据
    0. Resource: Supplier, Capacity, Layout, Relationship with client and supplier
    1. Time：Master Planning, Supplier Lead Time, Quene/Delivery Time(Capacity+Layout)
    2. Cost：Purchase Cost, Holding Cost, Transport Cost
    3. Quantity：BOM
    4. Flow-related: Capacity(Production, Batch-Size, Transpotation), Buffer
    5. Stability: Fluctuation+Accuracy, Variation+Statistical caliber, Risk Level Estimation+Consequence(Delay,Shortage,Quality),
    Extra Resource+Plan B

3. 项目实施
    1. 项目优先级判断(byself/out-resourcing )
    2. 全局资源分配(1.effect+difficulty 2.Critical Path)
    3. 建模
    4. 数据埋点与收集处理

4. 过程控制与反馈
    1. 监测指标
        1. Inventory
        1. Cost
        3. Milestone
        3. Delivery Time
        4. Accuracy
        5. Stability
    2. 资源利用与回收
        1. Cash flow: Payment terms
        2. Time: EDI,Difference Delay
        3. Room and Capacity: Share Logistic
        4. Variation: Complementary Fluctuation
    3. Extra Resource Request
        1. Presentation + Negotiation
    4. 项目修正与中止


# 全局map
https://whimsical.com/VuycUqwRmkk7thnkaKce48



# 全局关键 Macro Supply vs Macro Demand
0. Macro Demand with service level
    1. Quantity
    2. Lead-time/Waiting time (push/pull)
    3. Error Pecentage
    4. Customer tolerance (a kind of resource to be utilized) (marginal revenue)

0. Macro Supply with inventory and risk
    1. Inventory
    2. Resource/Capacity (including resource belong to others)

1. Demand Uncertainty/Supply Fluctuation deduced by Data & Distribution
    1. Forecasting & Risk Metigation
    2. Expected Result (Stocastic Optimization)
    3. Tradeoff (Marginal Revenue/Sensitivity)




# 子工程
* Push/Pull System（Push/Pull boundary)
    1. Principle:
        * Maximize external variaty with minimize internal variety
        * Keep in-process inventory as "Raw as Possible"
    2. Benefit:
        * Efficient mass customization(Postponement)
        * Pooling of product - Aggregating demand
        * Recent demand is more accuracy

* Segmentation - Inventory/Transportation/Forecasting
    |Physical|Customer|Supplier|Functional/Innovative|Revenue|
    |    :----:|    :----:|    :----:|:----:|:----:|
    |Size|Seasonality|Reliability|Y/N|Cost/Profit|
    1. Principle: Power Law
    2. Application:
        * Supply Chain Resource Allocation among differenct product category (functional vs innovative)
        * Distribution Integration (customer)
        * Sharing Logistic (customer)
        * ABC Method (Revenue)
        * Pooling of product(Customer)

* Aggregating
    1. Time
    2. Location
    3. SKU
    4. Benefit:
        1. Increase accuracy of forecasting
        2. Reduce safety stock

* Data & Distribution 
    1. Data:
        * Demand (normal distribution)
        * Leadtime/Transit time (log-normal)
        * Queueing (poisson distribution)


* Correlation analysis(regression)
    1. find the factor affecting the depant variable

    