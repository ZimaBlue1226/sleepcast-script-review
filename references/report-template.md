# Report construction

Fill the following template in Chinese. Retain its four main sections. Repeat finding entries under the appropriate type, ordered by severity within each type. Omit template instructions from the delivered report.

Identify the input by its actual filename and a supplied version or observed file modification date; do not invent a version. State English-only review, applicable standards and whether the input is a complete script or excerpt. Chinese passages are reviewer aids translated from the English quoted here.

For zero findings, use zero totals and “在本次审查范围内未发现有充分依据的问题。” in the detail section. For a pending creative choice, retain the replacement field as “待确认：…” and explain the unresolved decision in the suggestion; do not fabricate replacement English or Chinese. If a finding spans several locations, pair each exact excerpt with its own translation and repair or clearly identify the shared consolidated repair.

```markdown
# 《{{脚本标题}}》英文脚本审核报告

- **审核日期：** {{YYYY-MM-DD}}
- **英文脚本：** {{实际输入文件名}}
- **审核版本：** {{提供的版本或核对到的文件修改日期}}

## 一、审核范围

{{本次实际读取范围、适用标准与必要限制。}}

### 审核重点

{{本次适用的英文表达、成人助眠、逻辑、题材和节奏检查。}}

## 二、问题统计

### 2.1 按优先级统计

| 优先级 | 问题数量 |
|---|---:|
| P0 | {{数量}} |
| P1 | {{数量}} |
| P2 | {{数量}} |
| **合计** | **{{总数}}** |

### 2.2 按问题类型聚类

| 问题类型 | 合计 | P0 | P1 | P2 | 问题 ID |
|---|---:|---:|---:|---:|---|
| {{类型}} | {{总数}} | {{数量}} | {{数量}} | {{数量}} | {{ID列表}} |
| **合计** | **{{总数}}** | **{{数量}}** | **{{数量}}** | **{{数量}}** | — |

## 三、详细问题

### 3.1 {{一级类型}}

#### {{ID}}：{{问题标题}}

- **优先级：** {{P0/P1/P2}}
- **问题类型：** {{一级类型 / 二级类型}}
- **所处位置：** {{原MD文件行号；存在PART时同时注明}}
- **问题说明：** {{具体缺陷、对应标准、上下文及实际影响，说明定级依据}}
- **修改建议：** {{修复方式；必要时列明待确认的创作选择}}

**对应原文：**

    EN:
    {{准确引用英文}}

    ZH:
    {{上述英文的中文翻译}}

**修改后文本：**

    EN:
    {{可直接替换的完整英文}}

    ZH:
    {{修改后英文的中文翻译}}

## 四、审核结论

{{一至三段概括英文内容的可用性、主要问题与影响；不重复全部条目，不将严重程度当作修改排期，不声称TTS或工程验收通过。}}
```

Use fenced `text` blocks instead of indentation for the original/replacement passages in the final report. Only their quoted English is source text; the report's Chinese is a translation aid.
