# Hermes Agent Loop 调用链分析

## 1. 用户输入从哪里进入



## 2. System Prompt 在哪里构建

待分析。

## 3. Provider 在哪里选择

待分析。

## 4. Tool Schema 从哪里产生

待分析。

## 5. 模型返回的 Tool Call 如何解析

待分析。

## 6. Tool 如何执行

待分析。

## 7. Tool Result 如何回填上下文

待分析。

## 8. Agent 为什么继续循环或结束

待分析。

## 9. Session 在什么时候保存

待分析。

## 10. 异常、超时和最大轮次如何处理

待分析。

## 初步调用链

```text
用户输入
  ↓
CLI / Gateway
  ↓
AIAgent
  ↓
Prompt Builder
  ↓
LLM Provider
  ↓
Tool Call 判断
  ├─ 无 Tool Call → 最终响应
  └─ 有 Tool Call
       ↓
     Tool Registry
       ↓
     Tool Execution
       ↓
     Tool Result 回填
       ↓
     再次调用 LLM