This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
# 拉面餐厅网页设计模块总结

该网页包含五个主要模块，每个模块具有不同的布局和交互效果。以下是各个模块的设计概要：

## 1. 开头动画模块
- **动画效果**:
    - 一个约1秒的动画，展示两只手把拉面展开，随后把面放到桌子上，定格并变为背景图片。
    - 动画结束后，中间显示餐厅的牌子和简短介绍文字，介绍餐厅的背景：餐厅起源于中国西北，已在蒙特利尔运营8年。

## 2. 历史介绍模块
- **布局**:
    - 左侧为图片，右侧为文字，展示餐厅的历史。
- **效果**:
    - 随着用户向下滚动，图片和文字逐步出现，可能配合渐变或飞入动画。

## 3. 菜单 Gallery 模块
- **布局**:
    - 横向排列的菜单图片画廊，自动每2秒切换一张图片。
- **效果**:
    - 每张图片的中间浮现一个按钮，鼠标悬停时图片渐暗，按钮显现。
    - 点击按钮进入菜单分页，查看具体菜品详情。

## 4. 评论展示模块
- **布局**:
    - 两行滚动的评论。
- **效果**:
    - 第一行评论从左向右滚动，第二行评论从右向左滚动，增加动态感和趣味性。

## 5. 地图模块
- **功能**:
    - 集成 Google Maps，展示餐厅各个分店的位置及其坐标。
- **效果**:
    - 地图中显示分店标记，用户可以点击查看分店详情（如地址和联系方式）。

## 6. 多语言支持模块
- **语言**:
    - 网页支持中英法三国语言，默认语言为英语。
    - 右上角有一个地球小图标，用户可以点击图标切换语言，切换后页面内容会更新为相应语言。

---

## 开发技术建议
- **前端框架**: React.js + Next.js，适合动态交互和页面的响应式设计。
- **动画与交互**: 使用 Framer Motion 或 GSAP 实现复杂的动画效果，如页面滚动、按钮显示、评论滚动等。
- **样式框架**: Tailwind CSS 或 SCSS，便于快速实现响应式布局和自定义样式。
- **地图功能**: 使用 Google Maps API 显示分店位置，结合 React Google Maps 提供地图组件。
- **数据管理**: 如果涉及到动态数据，可以使用 Redux 或 React Context 来进行状态管理。
- **多语言支持**: 使用 i18n 或 React-Intl 实现多语言切换功能，支持中英法三种语言，右上角地球小图标可切换语言。
