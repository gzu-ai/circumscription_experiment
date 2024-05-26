# 限定理论模型的两种计算方法 实验结果

## 电路诊断实验
对应 `circuit_diagnosis`目录

我们选用ISCAS85标准电路测试集，并将其转化为CNF文件作为诊断的SD部分；OBS使用程序随机生成；将电路元件作为 COMP 部分。SD和OBS作为限制理论的子句集，COMP 作为极小化部分，电路其他部分作为可变部分。每个电路实例我们都随机生成了20个公式作为诊断的观察部分，每个观察与SD、COMP 部分组合成为一个实验样本。每个实验样本重复进行5次实验。


结果目录说明

- circ_lfc_solver_lstm_result 为 circ_lfc 结果数据
- circ_reduct_solver_lstm_result 为 circ_reduct_solver 结果数据
- circ_solver_lstm_result 为 circ_solver 结果数据
- circ2dlp_result 为circ2dlp 结果数据

- `cnf`  为原始子句集公式文件
- `dlp` 为 与 `cnf` 一一对应的逻辑程序公式

## 随机数据实验
对应 `random`目录

随机数据实验使用Giovanni等人提供的生成工具，生成了原子数量从50到1000 步长为50、子句/原子从3.0到4.5步长为0.5共800组实验数据，其中每组数据生成10个数据样本。
在可变原子、极小化原子上选取上 二者均在样本原子数量的 10%、30% 和50% 上随机选取，共产生9组实验参数。
我们使用 circ_solover 、 circ_reduct_solver 、 circ_lfc_solver 和 circ2dlp 等四个求解器进行实验，每组数据取可满足样本取其均值。

数据目录说明

- `circ_lfc_solver_lstm为` circ_lfc 算法脚本数据
- `circ_reduct_solver_lstm为` circ_reduct_solver 算法脚本数据
- `circ_solver_lstm` 为 circ_solver 算法脚本数据
- `circ2dlp` 为circ2dlp 脚本数据
- `cnf`  为原始子句集公式文件
- `dlp` 为 与 `cnf` 一一对应的逻辑程序公式

结果目录/压缩包说明

- circ_lfc_solver_lstm_result 为 circ_lfc 结果数据
- circ_reduct_solver_lstm_result 为 circ_reduct_solver 结果数据
- circ_solver_lstm_result 为 circ_solver 结果数据
- circ2dlp_result 为circ2dlp 结果数据

内部包含详细实验结果于统计数据
## SAT 竞赛实验
 对应 `sat_comp`

 其中 params 文件 保存 对应实例的 固定原子集(以 `.f`结尾)、 可变化原子集(以 `.v`结尾) 、 极小化原子集(以 `.p` 结尾)


## 随机3CNF模型枚举实验
对应 `random_enumeration`


