# 高性能并行编程与优化 - 字幕

这里托管本课程录屏的字幕，感谢 @inkydragon 的支持，他给出的工作流如下：

## 分工
（等有人来了再细分吧

p01 = 80min = 5min * 16
- [x] 00-05
- [x] 05-10
- [ ] 10-15

p02 = 135min = 5min * 27
p03 = 110min = 5min * 22
p04 = 112min  = 5min * 22

目前我估测 5min 视频大约对应 30~40 句话，我自己因为很熟练大概需要半小时能校对完。时间仅供参考。

## SubtitleEdit 使用简介

### 需要的依赖
+ course repo
+ B站对应课程的视频。建议转为 mp4 
    「阿里云盘：archibate-parallel-101」https://www.aliyundrive.com/s/zoUuVu8kNxw
    云盘没有，可以使用油猴脚本下载：[the1812/Bilibili-Evolved: 强大的哔哩哔哩增强脚本](https://github.com/the1812/Bilibili-Evolved)
    
+ [SubtitleEdit/subtitleedit](https://github.com/SubtitleEdit/subtitleedit)

视频命名为和 `*.ass` 字幕文件一样，也放在同一个文件夹内。
然后用 SubtitleEdit 打开字幕文件。
SubtitleEdit  可能会然你下载 mpv 作为播放器，然他自动下载就好。

成功打开字幕文件后长这样：
![image](https://user-images.githubusercontent.com/5158738/147956725-f09ecf01-6e1b-49dd-a5a5-9d8cbe290ac6.png)


### 选择字幕行
双击一行字幕会转跳到对应的时刻。

### 播放暂停视频
按空格/手动按播放键，可以播放视频。
等播放到你觉得该停顿的地方就再次按空格键/暂停按钮停下来。

这里以第77行为例。我们播放完 “然后我们这里因为要编译 C++” 这一句就暂停。
> 然后我们这里因为要编译 C++ ，所以就不是用的GCC，而是 g++ 了

### 字幕切分
一般来说你都需要把一行长的字幕切分为更短的句子。
这里我们选择在 `C++` 后切分。

在字幕编辑窗口 `C++` 一词后右键选择 “在光标/视频处分割行”。
这个差不多是最常用的操作，可以去设置里给他添加一个快捷键。
SE 会自动在对应的时间点和光标指定的位置，将当前行切分为两条新字幕。

切分时：
![image](https://user-images.githubusercontent.com/5158738/147957076-c0808cc4-0b1b-4b6c-acd3-b68b26d89169.png)

切分完成后：
![image](https://user-images.githubusercontent.com/5158738/147957567-9064a92b-4d30-4eae-a2c6-6b0eaf88a03b.png)

可以看见新增了第78条字幕，下面的音频显示也变成了两部分。

### 校对字幕
切分完成后，我们继续校对第77行。

首先，删除连词“然后”；

接着调整第77行的开始时间：直接拖动波形图部分，对应字幕行右侧的绿线。
你可以先听一遍，就知道应该拖动到哪里了。
听多了有经验了，只听一边就能完成切分+调整开头结尾的起止时间。
（神仙打轴甚至可以做到不听音频，直接看波形切分；我还听过只看频谱图然后录入日文字幕的传说

调整前：
![image](https://user-images.githubusercontent.com/5158738/147958023-53d457c2-9551-4a8e-b072-06efe060991b.png)
调整后：
![image](https://user-images.githubusercontent.com/5158738/147958063-e1f8bba9-c4a3-4565-91b8-8b491d662aed.png)

最后我们检查一下有没有专有名词的问题，并重新播放这一句，看看观感。
至此一行字幕就校对完毕了。

等完成 5min 的校对（这里就演示校对了几行）就可以提交 commit，然后准备打开 pr 了。
具体的 fork/commit/pr 看视频：[【GitHub】五分钟教你开 Pull Request_bilibili](https://www.bilibili.com/video/BV13i4y197k9?p=1)

![image](https://user-images.githubusercontent.com/5158738/147959347-74eec72d-3984-4d86-8a31-d8b9b0c927b4.png)


