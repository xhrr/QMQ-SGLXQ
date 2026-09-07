# QMQWeb — 内容更新说明

本静态站点支持通过 GitHub Issues 自动更新内容。<br>


# 站点更新日志

> 马倩倩应援站 · 从上线至今的全部更新

---

## v0.1 · 站点初版上线

- 首页 / 代表作品 / 写真集 / 动态 / 荣誉 / 行程 / 关于，七大板块一次到位
- 写真集瀑布流浏览 + 全屏灯箱，作品多分类筛选与搜索
- 全站移动端自适应，后台可视化管理系统同步上线

## v0.2 · 内容自动更新流水线

- 图集 / 作品 / 动态 / 荣誉 / 行程全部支持「提交 → 审核 → 自动上线」
- 审核通过后自动构建发布，无需手动更新网站

## v0.3 · 全站 SEO 优化

- 每个页面独立标题与描述，搜索引擎收录更友好
- 社交平台分享卡片（OG 标签）、sitemap 与 robots 配置齐全

## v0.4 · 分享功能

- 作品 / 写真集详情页一键复制链接
- 页脚分享海报：横竖两版高清图，保存即分享

## v0.5 · 稳定 ID 体系

- 全内容唯一标识：删除或重新排序内容，历史链接永不变动
- 老格式的分享链接持续可达

## v0.6 · 留言板上线

- 作品 / 写真集 / 动态详情页均可留言
- 杂志风排版、支持楼中楼回复，未署名默认「马铃薯」
- 留言审核制：提交后经整理展示，友善发言

## v0.7 · 图集时间轴

- 每个图集新增「发帖日期」
- 图集页支持按 **年份 / 月份** 两层筛选，最新内容优先展示
- 历史图集日期已全部补齐

## v0.8 · 投稿开放 

- 全新投稿页：**图集 / 作品** 双类型表单
- 多图上传自动压缩为 webp，支持 **拖拽文件或整个文件夹**、点击图片更换封面
- 投稿进入待审队列，审核通过自动上线

## v0.9 · 移动端体验升级

- 触屏按压反馈 + 可点提示动效，卡片一眼可知「能点」
- 留言与表单移动端布局优化
- 所有提交动作增加弹窗式结果反馈



## 提交流程

1. 新建 Issue
2. 按下面的模板填写内容
3. 等待管理员审核
4. 审核通过后系统会自动更新并部署

---

## 新增代表作品
#### sourceUrl是打开这个短剧的视频地址、豆瓣或者TMDB地址，poster是海报，images是剧集图

```text
type: works
category: 电视剧
title: 作品标题
role: 饰演角色
year:  2025-03-01
director: 导演
sourceUrl: https://example.com/original
poster: https://example.com/poster.jpg
synopsis: 一句话简介
images:
  - https://example.com/still1.jpg
  - https://example.com/still2.jpg
```

## 新增写真集---自己拍的照片，公开的照片都行，如果是他拍的照片，请提前询问原作者，谢谢
#### cover是封面，images是所有会展示的照片
```text
type: album
title: 写真集标题
author: 摄影师 / 来源作者（必填）
sourceUrl: https://example.com/original
date: 2025-03-01
cover: https://example.com/cover.jpg
images:
  - https://example.com/photo1.jpg
  - https://example.com/photo2.jpg
  - https://example.com/photo3.jpg
```

## 新增荣誉---指获了什么奖项

```text
type: awards
year: 2025
name: 奖项名称
org: 颁奖方
work: 关联作品
```

## 新增动态---比如新作品上映，社媒发的新动态

```text
type: news
date: 2026.03
title: 动态标题
summary: 动态摘要
sourceUrl: https://example.com/original
```

## 新增行程---啊吧啊吧，有倩一波日常的BOT自动更新，临时新增可填

```text
type: schedule
date: 2026.03.12
city: 城市
event: 活动事项
sourceUrl: https://example.com/original
```



