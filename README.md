# 食刻菜单 ✨

> 把你的馋意变成一份专属菜单

食刻菜单是一款 AI 驱动的周末菜单规划应用。记录你本周的饮食灵感，AI 主厨帮你整合成一份完整的宴客菜单——包含菜品图片、备菜清单和分级食谱。

---

## 功能亮点

- **馋意收藏** — 支持文字描述、链接（小红书/下厨房）、图片三种方式记录想吃的菜，并按"想吃 / 很想吃 / 馋疯了"三档优先级标记
- **AI 菜名识别** — 自动从输入内容中提取菜名，图片可直接识别菜品
- **氛围菜单生成** — 5 种用餐氛围（丰盛中式晚宴 / 快手午餐 / 精致西式 / 慵懒早午餐 / 深夜食堂），一键生成完整菜单
- **个性化定制** — 支持设置用餐人数、特殊忌口、是否减肥
- **备菜清单** — 自动生成按菜品分类的食材清单，确保备料不遗漏
- **分级食谱** — 厨房小白 / 普通厨艺 / 大厨三档，随时切换
- **营养分析** — 每道菜热量估算，以及蛋白质/碳水/糖分比例

---

## 技术栈

| 层级 | 技术 |
|------|------|
| 前端框架 | React 19 + TypeScript |
| 构建工具 | Vite 6 |
| 样式 | Tailwind CSS v4 |
| 动画 | Motion (Framer Motion) |
| AI 模型 | Google Gemini (`gemini-2.0-flash`) |
| AI SDK | `@google/genai` |

---

## 快速开始

### 1. 克隆仓库

```bash
git clone https://github.com/your-username/craving-menu.git
cd craving-menu
```

### 2. 安装依赖

```bash
npm install
```

### 3. 配置环境变量

复制 `.env.example` 并填入你的 Gemini API Key：

```bash
cp .env.example .env
```

```env
GEMINI_API_KEY=your_gemini_api_key_here
```

> 在 [Google AI Studio](https://aistudio.google.com/apikey) 免费获取 API Key。

### 4. 启动开发服务器

```bash
npm run dev
```

打开 [http://localhost:3000](http://localhost:3000) 即可使用。

---

## 部署到 Vercel（推荐）

部署后可生成公开链接，微信直接打开。

1. 将代码推送到 GitHub
2. 在 [vercel.com](https://vercel.com) 导入该仓库
3. 在 **Environment Variables** 中添加 `GEMINI_API_KEY`
4. 点击 Deploy，约 1 分钟完成

---

## 项目结构

```
src/
├── App.tsx              # 主应用，包含所有页面视图
├── main.tsx             # 入口文件
├── index.css            # 全局样式
├── types.ts             # TypeScript 类型定义
└── services/
    └── gemini.ts        # Gemini AI 调用（菜名识别、菜单生成、图片搜索）
```

---

## 使用流程

```
记录馋意 → 设置氛围 → 生成菜单 → 查看备菜清单 / 食谱
```

1. 在首页输入想吃的菜（文字/链接/图片），选择优先级后点击「收藏」
2. 点击「整合周末菜单」，选择氛围、人数、忌口等偏好
3. 点击「生成氛围感菜单」，等待 AI 主厨规划
4. 查看生成的菜单，进入「备菜清单」或「做法参考」

---

## License

Apache-2.0
