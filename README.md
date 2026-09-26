# 内容更新说明

这个站的内容不需要登服务器改：新建 Issue，按下面的模板填写，管理员审核通过后系统会自动更新内容并重新部署，全程几分钟。

日常的照片图集也可以直接在网站上的投稿页提交（支持多图、自动压缩、选封面），审核通过同样自动上线；Issue 通道更适合作品、荣誉、行程这类结构化内容。

## 提交前请留意

- 图片请用能长期访问的直链，尽量一次给全
- 他拍的照片请提前征得原作者同意再投，谢谢


## 新增代表作品

sourceUrl 是打开这部短剧的视频地址、豆瓣或者 TMDB 地址；poster 是海报，images 是剧集图。

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

## 新增写真集

自己拍的照片、公开的照片都行；如果是他拍的照片，请提前询问原作者，谢谢。cover 是封面，images 是所有会展示的照片。

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

## 新增荣誉

指获了什么奖项。

```text
type: awards
year: 2025
name: 奖项名称
org: 颁奖方
work: 关联作品
```

## 新增动态

比如新作品上映、社媒发的新动态。

```text
type: news
date: 2026.03
title: 动态标题
summary: 动态摘要
sourceUrl: https://example.com/original
```

## 新增行程

日常行程有 BOT 自动更新，临时新增的可手动填这里。

```text
type: schedule
date: 2026.03.12
city: 城市
event: 活动事项
sourceUrl: https://example.com/original
```

## 站点更新日志

### 建站与自动化（v0.1–v0.3）

- 初版上线：首页、代表作品、写真集、动态、荣誉、行程、关于，七大板块一次到位；写真集瀑布流加全屏灯箱，作品支持分类筛选与搜索；全站移动端自适应，可视化后台同步上线
- 内容自动更新流水线：图集、作品、动态、荣誉、行程全部支持「提交 → 审核 → 自动上线」，更新网站不用碰代码
- 全站 SEO：每个页面独立标题与描述，社交分享卡片（OG 标签）、sitemap 与 robots 配置齐全

### 分享与稳定链接（v0.4–v0.5）

- 分享功能：作品、写真集详情页一键复制链接；页脚分享海报有横竖两版高清图，保存即分享
- 稳定 ID 体系：全部内容有唯一标识，删除或重新排序后历史链接永不变动，老格式的分享链接一直可达

### 留言板与图集时间轴（v0.6–v0.7）

- 留言板上线：作品、写真集、动态详情页都可以留言；杂志风排版，支持楼中楼回复，未署名默认叫「马铃薯」；提交后经整理展示
- 图集时间轴：每个图集有了「发帖日期」；图集页支持按年份、月份两层筛选，最新内容优先；历史图集的日期已经全部补齐

### 投稿与移动端（v0.8–v0.10）

- 投稿开放：全新投稿页，支持图集、作品两种类型；多图上传自动压缩成 webp，支持拖拽文件或整个文件夹、点击图片更换封面；投稿进入待审队列，审核通过自动上线
- 补充图片：投稿新增「补充」类型，粘贴已有图集或作品的详情页链接（或者 `a-xxxx`、`w-xxxx`），就能为它追加照片——图片排在原有图片末尾，不替换、不打乱顺序，重复图片自动跳过
- 移动端体验：触屏按压反馈与可点提示动效，卡片一眼可知「能点」；留言与表单布局优化；所有提交动作加了弹窗式的结果反馈
