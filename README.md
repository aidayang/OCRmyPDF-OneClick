<!-- SPDX-FileCopyrightText: 2014 Julien Pfefferkorn -->
<!-- SPDX-FileCopyrightText: 2015 James R. Barlow -->
<!-- SPDX-License-Identifier: CC-BY-SA-4.0 -->

<img src="docs/images/logo.svg" width="240" alt="OCRmyPDF">

# OCRmyPDF-OneClick
OCRmyPDF windows版免安装部署一键启动整合包

OCRmyPDF可以将PDF内不可搜索的图片和文字识别转换为可复制可搜索的文本，并对PDF文件进行优化。

![](https://raw.githubusercontent.com/aidayang/OCRmyPDF-OneClick/refs/heads/main/ocrmypdf2.webp)


## OCRmyPDF介绍

主要特点

从常规 PDF生成可搜索的PDF/A文件

将 OCR 文本准确放置在图像下方，以方便复制/粘贴

保持原始嵌入图像的精确分辨率

如果可能，以“无损”操作插入 OCR 信息，而不会破坏任何其他内容

优化 PDF 图像，通常生成比输入文件更小的文件

如果需要，在执行 OCR 之前校正和/或清理图像

验证输入和输出文件

将工作分配到所有可用的 CPU 核心

使用Tesseract OCR引擎识别100多种语言

保护您的私人数据不受侵犯。

适当扩展以处理数千页的文件。

经过数百万份 PDF 的实战测试。

## OCRmyPDF整合包使用说明

OCRmyPDF依赖其它外部程序Ghostscript和Tesseract，网盘内有安装程序，全程保持默认安装即可

安装Tesseract最后一步会自动下载英文的语言包文件，如果无法自动下载的话，可以直接cancel取消跳过，到我网盘里下载需要的语言包放到Tesseract安装目录内的tessdata文件夹内

然后将软件压缩包OCRmyPDF.7z下载到本地电脑上并解压，然后双击【启动软件.exe】打开软件

首先选择待处理文件，可以是PDF也可以是图片，也可以输入文件夹路径批量处理文件夹内所有文件。

批处理功能做的比较简单，所有文件是同时处理的，所以建议待处理的文件夹内不要有太多文件，否则可能会比较卡。而且待处理文件夹内不要有PDF和图片以外的文件。如果待处理的文件夹内有图片，批量处理还要设置【图片DPI】值

【OCR语言】默认只支持英文，识别其它语言的话需要下载支持文件.traineddata，常见语言网盘里有，把.traineddata格式文件下载到tesseract安装目录tessdata文件夹内，语言代码如下：

简体中文：chi_sim

繁体中文：chi_tra

德语：deu

法语：fra

日语：jpn

韩语：kor

俄语：rus

泰语：tha

缅甸语：vie

识别英语可以不用填写，识别其它语言的话需要在输入框中输入语言代码。如果是多种语言的话可以混合输入，识别中英文的话可以输入：eng+chi_sim

其它国家语言代码对照表：https://nuowa.net/1796

其它语言包文件下载链接：https://github.com/tesseract-ocr/tessdata

【重新OCR】强制对每页重新渲染并 OCR

【跳过文本】跳过已有文本的页面（仅处理纯图片页）

【重新OCR】和【跳过文本】不可同时选中

【校正倾斜】自动校正页面倾斜（提升 OCR 准确率），比如扫描出的PDF文档内容是倾斜的，可以开启此项功能

【清理伪影】清理扫描伪影（如黑边、噪点）并将处理后的图像嵌入最终 PDF

如果需要使用【清理伪影】功能，则电脑上需要安装unpaper，unpaper安装步骤如下：

首先安装Chocolatey，然后安装unpaper
choco install unpaper
【图片DPI】处理图片文件的话要指定该值

【输出格式】默认输出 pdfa 存档，pdf格式修改最小，还有pdfa-1,pdfa-2,pdfa-3等

【标题】自定义 PDF 元数据标题

【指定页面】只处理指定的PDF页面，填数字如1,2,5-8，逗号和连字符都要用英文符号

【线程数】设置并行线程数（默认使用所有 CPU 核心）

【输出txt】生成独立的txt格式的OCR 文本文件（用于校对或文本分析）

【图像压缩级别】0无压缩，3最高压缩（最大节省空间）

使用【图像压缩级别】功能的话，电脑上需要安装pngquant， PowerShell运行下面命令安装

choco install pngquant

视频教程及效果演示：https://www.youtube.com/watch?v=7-GbGwcyGUU

## 注意事项
整合包只支持windows10或11

软件运行路径中不要有非英文字符和空格，待处理文件同样要注意

## PDF OCR识别转文本软件OCRmyPDF下载链接
https://pan.quark.cn/s/c5adb7ecd22b

https://pan.baidu.com/s/1CK49OoGZVeAY67ywkBWUWg?pwd=dw5i

## 项目链接
https://github.com/ocrmypdf/OCRmyPDF
