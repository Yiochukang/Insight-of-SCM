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
1. Demand
    1. Hardline: Quantity/Quality Control
    2. Service Level: Waiting time/Wastage/Fulfillment Percentage(marginal revenue vs marginal cost)
    

2. Supply 
    1. Priority/Resource Allocation(Capacity, Cash, Storage, Leadtime)
    2. Safety Stock/Additional Resource(Bottleneck)/Plan B: Risk and fulctuation
    3. Heijunka & TAKT: Buffer/Multi-Sourcing


3. Process Control(Plus vs Pruning)
    1. Priority Review
    2. Tradeoff: Increase resource or sacrifice service level(Marginal and Redline)





# Method
* Push-Pull Boundary（Delay Differentiation/Mass Customerization/Scale Effect)
    1. Principle:
        * Maximize external variaty with minimize internal variety
        * Keep in-process inventory as "Raw as Possible"
    2. Application:
        * Decrease complexity → Aggregating demand → Increase prediction accuracy：Efficient mass customization
        * Reduce lead-time (WIP), then decrease intentory furthermore


* Segmentation(Priority/Power law)
    |Physical|Customer|Supplier|Functional/Innovative|Revenue|
    |    :----:|    :----:|    :----:|:----:|:----:|
    |Size|Seasonality|Reliability|Y/N|Cost/Profit|
    1. Principle: Power Law
    2. Application:
        * Supply Chain Resource Allocation among differenct product category (functional vs innovative)
        * ABC Method (Revenue/Cost)


* Aggregating(Scale effect/Pooling of product)
    1. Criteria:SKU/Location/Function/Issue/Process/Manufacuture process/Labour required
    3. Application
        1. Increase prediction accuracy: Distribution Integration
        2. Decrease cost: Sharing Logistic (Pooling of product)
        3. Decrease safety stock (by decreasing std)
        4. Decrease warm-up time: Batch size/Minimun Order size


* Additional Resource/Plan B
    1. Principle: Tradeoff cost and risk
    2. Application
        1. Eliminate current bottleneck/increase revenue/decrease quene and leadtime
        2. Risk mediation
        3. Decrease leadtime (on shore supplier), furthermore decrease safety stock


* Pruning and stop-loss
    1. Principle: bottom line/Capacity/priority list/Milestone
    2. Application:
        1. TAKT: Batch size/decrease service level to free up resource for higher priority task
        2. Marginal profit derived from margin increase in service leverl


* Reserved Resource for future development
    1. System Sensitivity/Robustness/Resilient/Adaptability


* Optimization
    1. Local optimization
    2. Expected value and stocastic optimization    
    2. Operation management
        1. Pre-requsite
        2. Bottleneck and Critical Chain
        3. Take advantage of lead-time
    3. Scale of economy
   

* Data & Distribution 
    1. Distribution:
        * Demand (normal distribution)
        * Leadtime/Transit time (log-normal)
        * Queueing (poisson distribution)
    2. Operation Cost
        1. Raw material/Logistic/Warehousing/Labour/Machine
        2. Policy and International Tax    
    3.  Correlation analysis(regression)
        * find the factor affecting the depant variable   


# 供应链模式要匹配产品战略，确定各项指标
指标：
1. 供给顺畅、特定技术与质量（integrated supplier)
2. 成本、时效（leadtime、覆盖率)、定制多样化（SKU）、地缘优势（需求供给地理距离，地缘优惠政策）

产品目标/定位（迎合群体）：
1. 时代特征（经济泡沫/石油危机/政治经济）：UNIQLO/Toyota/Tesla
2. 科技技术：Apple，AMSL，Pfizer
3. 快速反应：ZARA、Dell、HP
4. 多样化：GM，Nike，GAP
5. 服务：Costco（售后），3PL/京东（及时率），美团/walmart（覆盖率）


# 信息中台监测，及时调整（ABS）
1. 库存管理
    1. 通用件 + push/pull point
    2. 预测端：aggregation，降低std
    3. 供给端：distribution integration + risk pooling + sharing logistic + 路径优化
    4. segmantation: critical component vs screw

2. 风险管理
    1. holding cost vs disruption
    2. obermeyer case：准确度高的优先

3. 供应商管理
    1. 是否符合产品定位，有助于revenue增值（子功能与系统总功能 方向一致）
    2. Selection criteria（同鲫比较/局部最优）
        1. 时间
        2. 成本
        3. 系统性风险（uncertainty)
            1. sole supplier（material,capacity,quality)
            2. 核心技术
    3. single soucing(规模效应，供应商关系与协调研发 vs 系统性风险) vs multi-sourcing（成本、管理难度）

4. 系统稳定性，生产平整化
5. 预留长期接口 optimization vs adaptability














