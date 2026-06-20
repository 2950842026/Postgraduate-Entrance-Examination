# 专业复试线小文件

网页会在选择具体专业后按需请求 `scores/{专业代码}.json`，例如 `scores/085404.json`。

每个文件只放一个专业的近三年复试线，避免把所有成绩直接打包进页面。字段示例：

```json
{
  "majorCode": "085404",
  "majorName": "计算机技术",
  "updatedAt": "2026-06-19",
  "lineType": "复试线（初试门槛）",
  "lines": [
    {
      "year": 2026,
      "schoolCode": "10005",
      "schoolName": "北京工业大学",
      "collegeName": "计算机学院",
      "majorCode": "085404",
      "majorName": "计算机技术",
      "studyMode": "",
      "totalScore": 365,
      "politics": 40,
      "foreignLanguage": 40,
      "business1": 70,
      "business2": 70,
      "sourceUrl": "https://..."
    }
  ]
}
```

如果只有通用单科线，也可以使用 `singleSubject100` 和 `singleSubjectGt100`，页面会自动映射到政治/外语和两门业务课。
