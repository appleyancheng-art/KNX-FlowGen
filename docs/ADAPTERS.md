# 网关适配补充

完整手册包含 2.0 工作流与宜巢适配。本页补充后续新增的迈联规则。软件版本继续保持 2.0。

## 迈联智家 / Morelinks

设备规划、批量规划、现场记录与 ETS6 XML 导入数据可进入适配中心。选择设备，核对统一名称、设备类型、功能编号和 DPT，再确认导出。

同一设备使用相同基础名称，后面附“类型编号 功能编号”。普通灯 `主卧射灯 1 0` 为读/反馈，`主卧射灯 1 1` 为写/控制。后缀属于名称，不重新分配实际组地址。

输出遵循提供样例的九列 CSV、GBK 编码与 CRLF 换行。名称含 GBK 无法表示的字符时会阻止导出。已录入 31 类、157 个编号条目；其中 26 个参数条目与1个歧义条目不生成虚构地址。双色温类型9的六种功能可由样例核对，其他类型仍需项目与主机验证。

## 宜巢 / YCZNWL KNX Gateway

按已提供模板生成六类 KNX 设备 JSON，保留组地址。房间 ID 需要填写目标网关已有值；复核实例名称和设备参数。网关内部 scene_uuid 无法从 KNX 场景地址生成，不会自动编造。

## 验证范围

软件自动检查与浏览器导出验证不等于全部网关硬件验收。导入前先备份目标配置，并用少量代表设备确认控制、反馈和参数。没有匹配的功能会要求补充或明确跳过，不补造地址。

## English supplement

Morelinks uses a common device base name followed by type and function numbers. Type 1 suffix `1 0` is read/feedback and `1 1` is write/control. Numeric KNX addresses are preserved. The exporter follows the supplied nine-column GBK CSV format. Unresolved parameter entries are excluded from address export. YCZNWL requires room IDs from the target gateway; internal scene UUIDs are not invented. Validate a small representative import on actual hardware before wider use.
