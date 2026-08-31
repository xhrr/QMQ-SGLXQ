# 老马Web — 内容更新说明

本静态站点支持通过 GitHub Issues 自动更新内容。<br>
涉及到图片的有能力可以自己放图床之后放外链，也可以给我网盘的链接（用网盘得手动更新，比较慢，优先外链）<br>
图片推荐压缩成webp再上传到图床，保证访问速度的情况下，画质损失最小

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
