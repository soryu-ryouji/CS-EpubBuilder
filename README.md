![logo](./Docs/Images/logo.png)

# Epub Builder Library

**Example**

```c#
var epubMetadata = new EpubMetadata
{
    Title = "太原之恋",
    Language = "zh",
    Author = "刘慈欣",
};

var mdPath = @"D:\Books\Novel\太原之恋\太原之恋.md";
var coverPath = @"D:\Books\Novel\太原之恋\cover.jpg";
var buildMetadata = new BuildMetadata(mdPath, coverPath, pageSplitLevel:1);
var epub = new Epub(epubMetadata, buildMetadata);

var zip = epub.Generate();
zip.Save(@"D:\太原之恋.epub");
```

## Docs

[Epub 电子书格式介绍](./Docs/Epub电子书格式.md)

[EpubBuilder 执行流程](./Docs/程序执行流程.md)

[如何将 EpubBuilder 打包为应用程序](./Docs/如何构建EpubBuilderCLI.md)

## Todo List

- [x] 多级目录的实现
- [x] 添加子标签目录跳转支持
- [x] markdown文本渲染
- [x] markdown图像文件插入


## LICENSE

![MIT](./Docs/Images/MIT.png)

Epub is released under the MIT