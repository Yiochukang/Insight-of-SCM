# 供应链项目管理（微观）
1. 项目目标
    1. NPI系统搭建（system engineering)
        1. 子项目接口
        2. Flow (Provide, transfer), Stable(Maintain)
        3. Flow Disruption Risk(Estimation, Safety inventory, Plan B)

    2. 建模优化(object function aimed at most)
        ~~1. 降低cost~~
        ~~2. 降低lead time~~
        3. 降低quene
        ~~4. 提升accuracy~~
        5. 提升stability

    3. 稳定性 Resilience (constraints aimed at least)
        1. 吸收波动（Buffer）
        ~~2. Risk indetificaton & metigation (Plan B)~~
        ~~3. 针对未来变化的可扩展性、前瞻性adaptation~~

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
    ~~3. 建模~~
    ~~4. 数据埋点与收集处理~~

4. 过程控制与反馈
    1. 监测指标
        ~~1. Inventory~~
        ~~1. Cost~~
        ~~3. Milestone~~
        ~~3. Delivery Time~~
        ~~4. Accuracy~~
        ~~5. Stability~~
    2. 资源利用与回收
        1. Cash flow: Payment terms
        ~~2. Time: EDI,Difference Delay~~
        ~~3. Room and Capacity: Share Logistic~~
        ~~4. Variation: Complementary Fluctuation~~
    ~~3. Extra Resource Request~~
        ~~1. Presentation + Negotiation~~
    ~~4. 项目修正与中止~~


# 全局map
https://whimsical.com/VuycUqwRmkk7thnkaKce48



# Core Topic and Measurement
1. Generalized Demand
    1. Quantity
    2. Waiting time (push/pull,delay differciation)
    3. Error Pecentage/Service level/Customer tolerance (a kind of resource to be utilized) (marginal revenue vs marginal cost)
    
2. Generalized Supply 
    1. Safety Inventory/Buffer
    2. Max Capacity/Limitation/Lead time/Bottleneck
    2. Plan B/Multi-Sourcing/Extra Resource(Resource belong to others)

3. Operation Cost
    1. Raw material/Logistic/Warehousing/Labour/Machine
    2. Policy and International Tax

4. Risk/Additional resource/Stop-loss
    2. Expected Result (Stocastic Optimization)
    3. System Sensitivity/Robustness/Resilient/Adaptability
    4. Bottleneck/Process control/Adjustment/Optimization




# Method
* Push-Pull Boundary（Delay Differentiation/Mass Customerization/Scale Effect)
    1. Principle:
        * Maximize external variaty with minimize internal variety
        * Keep in-process inventory as "Raw as Possible"
    2. Application:
        * Decrease complexity → Aggregating demand → Increase prediction accuracy：Efficient mass customization
        * Reduce lead-time (WIP)


* Segmentation(Priority/Power law)
    |Physical|Customer|Supplier|Functional/Innovative|Revenue|
    |    :----:|    :----:|    :----:|:----:|:----:|
    |Size|Seasonality|Reliability|Y/N|Cost/Profit|
    1. Principle: Power Law
    2. Application:
        * Supply Chain Resource Allocation among differenct product category (functional vs innovative)
        * ABC Method (Revenue/Cost)



* Aggregating(Scale effect/Pooling of product)
    1. Criteria:SKU/Location/Function/Issue/Process
    3. Application
        1. Increase prediction accuracy: Distribution Integration
        2. Decrease cost: Sharing Logistic (Pooling of product)
        3. Decrease safety stock
        4. Decrease warm-up time


* Additional Resource/Plan B
    1. Principle: Tradeoff cost and risk
    2. Application
        1. Eliminate current bottleneck/increase revenue/decrease quene and leadtime
        2. Risk mediation


* Pruning and stop-loss
    1. Principle: bottom line/Capacity/priority list/Milestone
    2. Application:
        1. TAKT: decrease service level, free up resource for higher priority task



* Data & Distribution 
    1. Data:
        * Demand (normal distribution)
        * Leadtime/Transit time (log-normal)
        * Queueing (poisson distribution)
    2.  Correlation analysis(regression)
        * find the factor affecting the depant variable

    