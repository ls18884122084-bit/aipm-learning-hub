# AI PM 学习平台 - 内容管理系统

## 📁 目录结构

```
ai-pm-learning-hub/
├── index.html              # 主页面（学习平台）
├── content/                # 内容目录（每周更新）
│   ├── week-2026-03-16.json   # 本周内容
│   ├── week-2026-03-23.json   # 下周内容（待生成）
│   └── ...
├── archives/               # 历史内容存档
└── README.md               # 本文件
```

## 📰 内容来源

### 国内平台
| 平台 | 地址 | 内容类型 |
|------|------|----------|
| 人人都是产品经理 | woshipm.com | 深度文章、行业分析 |
| 知乎 | zhihu.com | 专栏、问答 |
| 即刻 | okjike.com | 短内容、动态 |
| 36氪 | 36kr.com | 行业新闻 |
| 虎嗅 | huxiu.com | 商业分析 |

### 国外平台
| 平台 | 地址 | 内容类型 |
|------|------|----------|
| Medium | medium.com | 深度文章 |
| LinkedIn | linkedin.com | 行业洞察 |
| Product School | productschool.com | 课程、指南 |
| Lenny's Newsletter | lennysnewsletter.com | PM专栏 |
| Boston Institute | bostoninstituteofanalytics.org | AI趋势 |

## 📝 内容JSON格式

每周内容文件 `week-YYYY-MM-DD.json` 格式：

```json
{
  "weekId": "2026-03-16",
  "weekLabel": "3月第3周",
  "generatedAt": "ISO时间戳",
  "theme": "本周主题",
  "articles": [
    {
      "id": "唯一ID",
      "title": "文章标题",
      "source": "来源平台",
      "sourceUrl": "原文链接",
      "author": "作者",
      "date": "发布日期",
      "difficulty": 1-3,  // 1简单 2中等 3困难
      "tags": ["标签数组"],
      "summary": "一句话摘要",
      "keyPoints": ["核心要点数组"],
      "quiz": [
        {
          "question": "题目",
          "options": ["选项A", "选项B", "选项C", "选项D"],
          "answer": 0-3,  // 正确答案索引
          "explanation": "解析"
        }
      ]
    }
  ],
  "totalQuestions": 15,
  "passScore": 80,
  "nextUpdateDate": "下次更新日期"
}
```

## 🔄 每周更新流程

### 自动更新（已配置Automation）
- **频率**：每周日 9:00
- **内容**：自动搜索各平台最新 AI PM 文章
- **输出**：生成新的 `week-YYYY-MM-DD.json`

### 手动更新步骤
1. 搜索本周热门 AI PM 文章（国内外各2-3篇）
2. 按难度分级：入门(1) → 中等(2) → 进阶(3)
3. 每篇文章提取 3-4 道测试题
4. 总题数控制在 12-15 题
5. 保存为 `content/week-YYYY-MM-DD.json`

## 📊 难度分级标准

| 难度 | 适合人群 | 内容特点 | 题目类型 |
|------|----------|----------|----------|
| ⭐ 简单 | 零基础入门 | 基础概念、术语解释 | 定义、概念辨析 |
| ⭐⭐ 中等 | 有一定基础 | 方法论、实战技巧 | 场景应用、方法选择 |
| ⭐⭐⭐ 进阶 | 进阶提升 | 深度分析、前沿趋势 | 综合分析、策略判断 |

## 🎯 测试题设计原则

1. **来源真实**：每道题必须基于当周推文内容
2. **难度渐进**：简单题在前，困难题在后
3. **解析清晰**：每题都有详细解释，帮助理解
4. **实用导向**：题目考查实战能力，非纯记忆

## 📈 用户学习数据

平台会自动记录：
- 学习天数 & 连续打卡
- 测试分数 & 通过率
- 文章阅读量
- 能力成长曲线
- 学习心得

## 🚀 后续迭代计划

- [ ] 接入 RSS 自动抓取文章
- [ ] AI 自动生成测试题
- [ ] 支持用户自定义订阅源
- [ ] 错题本 & 针对性复习
- [ ] 社区排行榜
- [ ] 移动端 PWA 支持

---

*最后更新：2026-03-16*
