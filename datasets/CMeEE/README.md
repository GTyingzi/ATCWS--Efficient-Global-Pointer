中文医疗嵌套实体数据集：

训练集：15000、验证集：5000

数据分为9个标签类别，分别为:
疾病（dis），
临床表现（sym），
医疗程序（pro），
医疗设备（equ），
药物（dru），
医学检验项目（ite），
身体（body），
科室（dep），
微生物类（mic）

数据格式：
```json
  {
    "text": "（5）房室结消融和起搏器植入作为反复发作或难治性心房内折返性心动过速的替代疗法。",
    "entities": [
      {
        "start_idx": 3,
        "end_idx": 7,
        "type": "pro",
        "entity": "房室结消融"
      },
      {
        "start_idx": 9,
        "end_idx": 13,
        "type": "pro",
        "entity": "起搏器植入"
      },
      {
        "start_idx": 16,
        "end_idx": 33,
        "type": "dis",
        "entity": "反复发作或难治性心房内折返性心动过速"
      }
    ]
  }
```

合并训练集和验证集（共20000条数据）。划分训练集：验证集：测试集 = 14：3：3