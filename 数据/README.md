# 数据集说明

> 由 HIP HUB（编舞师名录）维护，随站点数据同步更新。
> 最后同步：2026-11-16

## 文件

| 文件 | 一行是什么 | 关键字段 |
|---|---|---|
| `teachers.csv` | 一位编舞师 | `teacher_id` `name` `type` `status` |
| `trips.csv` | 一场行程 / 特邀课 | `trip_id` `teacher_id` `date_start` `city` `studio_id` `kind` |
| `regular_classes.csv` | 一条每周固定课 | `regular_id` `weekday` `studio_id` `start_time` `month` |
| `studios.csv` | 一家舞室 / 品牌 | `studio_id` `name` `city` `brand_id` `kind` |
| `cities.csv` | 一座城市 | `city` |

## 口径

- `kind` 只有两个值：`workshop`（特邀课，被店请去上）和 `regular`（常规课）
- 细分（内训 / 夜训 / 艺考 / 拍摄）写在 `note` 的方括号前缀里
- 课程类型定义见 `文章/course-types.md`
- 城市写法已规范化，原始写法保留在 `city_raw`
- `month` 表示这条常规课只在某月有效；空 = 不展示

## 隐私

**已剔除所有联系方式类字段**（微信、电话、报价、详细地址）。
本数据集只包含可公开的事实：谁、在哪天、在哪座城市、哪家舞室、上什么课。

## 引用

```
来源：HIP HUB · 编舞师名录 · ` + SITE + `
```
