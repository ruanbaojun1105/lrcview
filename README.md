此项目拷贝于https://github.com/wangchenyan/lrcview

# lrcview
[ ![Download](https://api.bintray.com/packages/ruanbaojun1105/maven/lrcview/images/download.svg) ](
https://bintray.com/ruanbaojun1105/maven/lrcview/_latestVersion)

## 使用
**Gradle**
implementation 'com.rbj:lrcview:1.0.5'



# 1.0.0：添加歌词控件的单击事件
# 1.0.5：修改中轴线的单击事件


## 系列文章
- [Android开源在线音乐播放器——波尼音乐](https://juejin.im/post/5c373a32e51d4551cc6df6db)
- [Android开源音乐播放器之播放器基本功能](https://juejin.im/post/5c373a32e51d45521315fc50)
- [Android开源音乐播放器之高仿云音乐黑胶唱片](https://juejin.im/post/5c373a336fb9a04a016488e8)
- [Android开源音乐播放器之自动滚动歌词](https://juejin.im/post/5c373a336fb9a049f43b85de)
- [Android开源音乐播放器之在线音乐列表自动加载更多](https://juejin.im/post/5c373a336fb9a049b82aaaaf)

- 如果喜欢，欢迎Star！

## 简介
Android歌词控件，支持上下拖动歌词，歌词自动换行，自定义属性，支持双语歌词。

![](https://raw.githubusercontent.com/wangchenyan/lrcview/master/art/screenshot.gif)


## 属性
| 属性 | 描述 |
| ---- | ---- |
| lrcTextSize | 当前歌词文本字体大小 |
| lrcNormalTextSize | 普通歌词文本字体大小 |
| lrcNormalTextColor | 非当前行歌词字体颜色 |
| lrcCurrentTextColor | 当前行歌词字体颜色 |
| lrcTimelineTextColor | 拖动歌词时选中歌词的字体颜色 |
| lrcTextGravity | 歌词对齐方向，center：居中对齐，left：靠左对齐，right：靠右对齐，默认为 center |
| lrcDividerHeight | 歌词间距 |
| lrcAnimationDuration | 歌词滚动动画时长 |
| lrcLabel | 没有歌词时屏幕中央显示的文字，如“暂无歌词” |
| lrcPadding | 歌词文字的左右边距 |
| lrcTimelineColor | 拖动歌词时时间线的颜色 |
| lrcTimelineHeight | 拖动歌词时时间线的高度 |
| lrcPlayDrawable | 拖动歌词时左侧播放按钮图片 |
| lrcTimeTextColor | 拖动歌词时右侧时间字体颜色 |
| lrcTimeTextSize | 拖动歌词时右侧时间字体大小 |

## 方法
| 方法 | 描述 |
| ---- | ---- |
| loadLrc(File lrcFile) | 加载歌词文件 |
| loadLrc(File mainLrcFile, File secondLrcFile) | 加载双语歌词文件，两种语言的歌词时间戳需要一致 |
| loadLrc(String lrcText) | 加载歌词文本 |
| loadLrc(String mainLrcText, String secondLrcText) | 加载双语歌词文本，两种语言的歌词时间戳需要一致 |
| loadLrcByUrl(String lrcUrl) | 加载在线歌词文本，默认使用 utf-8 编码 |
| loadLrcByUrl(String lrcUrl, String charset) | 加载在线歌词文本 |
| hasLrc() | 歌词是否有效 |
| setLabel(String label) | 设置歌词为空时视图中央显示的文字，如“暂无歌词” |
| updateTime(long time) | 刷新歌词 |
| ~~onDrag(long time)~~ | ~~将歌词滚动到指定时间。已弃用，请使用 updateTime(long) 代替~~ |
| ~~setOnPlayClickListener(OnPlayClickListener onPlayClickListener)~~ | ~~设置拖动歌词时，播放按钮点击监听器。如果为非 null ，则激活歌词拖动功能，否则将将禁用歌词拖动功能。已弃用，请使用 setDraggable 代替~~ |
| setDraggable(Boolean draggable, OnPlayClickListener onPlayClickListener) | 设置歌词是否允许拖动。如果允许拖动，则 OnPlayClickListener 不能为 null |
| setNormalColor | 设置非当前行歌词字体颜色 |
| setCurrentColor | 设置当前行歌词字体颜色 |
| setTimelineTextColor | 设置拖动歌词时选中歌词的字体颜色 |
| setTimelineColor | 设置拖动歌词时时间线的颜色 |
| setTimeTextColor | 设置拖动歌词时右侧时间字体颜色 |
| setCurrentTextSize | 当前歌词文本字体大小 |
| setNormalTextSize | 普通歌词文本字体大小 |


## License

    Copyright 2020 RuanJeam

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
