![QuickLook icon](https://cloud.githubusercontent.com/assets/1687847/26008086/060d9cca-374c-11e7-9345-7f0f0f91a421.png)

[![Build status](https://ci.appveyor.com/api/projects/status/w5lx1mlq8b0mb8fo?svg=true)](https://ci.appveyor.com/project/xupefei/quicklook)

*This project is currently under heavy development. Come back often to see what's new.*

<img src="http://pooi.moe/QuickLook/sample.gif?2" width="400">

## Background
[Quick Look](https://en.wikipedia.org/wiki/Quick_Look) is among the few features I missed from Mac OS X. It enables *very* quick preview of file by pressing <kbd>Space</kbd> key while highlighting it, without opening its associated application. Then I decide to add this feature to Windows by myself, which results this “QuickLook” project.

You may ask, why you write this when there several alternatives available on the Internet (e.g. [WinQuickLook](https://github.com/shibayan/WinQuickLook) and [Seer](https://github.com/ccseer/Seer))? The answer is that, they are all among those which no longer actively developed, lack of support of file types and plugins, or asking user for amounts of $$$.

## Features
Till now, QuickLook supports the preview of 

 - Images: e.g. `.png`, `.jpg`, `.bmp`, `.gif`, `.psd` and Camera RAW formats
 - Compressed archives: `.zip`, `.rar`, `.tar.gz`, `.7z` etc.
 - Pdf file
 - All kinds of text files (determined by file content)
 - Microsoft Word (`.doc`, `.docx`), Excel (`.xls`, `.xlsx`) and PowerPoint (`.ppt`, `.pptx`) files (requires MS Office installation)
 - OpenDocument (`odt`, `.ods` and `.odp`) files (requires MS Office installation)
 - Video files (`.mp4`, `.mkv`, `.m2ts` etc.)
 - HTML files (`.htm`, `.html`)
 - Markdown file (`.md`)
 - Other files and folders will be shown in a information box

## Usages
In-place preview / Integrate with 3rd-party file manager
 - You may set up a custom hot key that fires event `QuickLook.exe C:\path\to\your\file.txt`. Press your hotkey for the 2nd time will close the existing preview window.
 
Hotkeys in preview window:

 - <kbd>Space</kbd> Show/Hide the preview window
 - <kbd>Esc</kbd> Hide the preview window
 - <kbd>Enter</kbd> Open/Execute current file
 - <kbd>Mouse️</kbd> <kbd>↑</kbd> <kbd>↓</kbd> <kbd>←</kbd> <kbd>→</kbd> Preview another file
 - <kbd>Ctrl-Wheel</kbd> Zoom in/out

## Development

The previewing ability can be extended by new plugins. Read the [plugin interface](https://github.com/xupefei/QuickLook/blob/master/QuickLook/Plugin/IViewer.cs), [context object](https://github.com/xupefei/QuickLook/blob/master/QuickLook/Plugin/ContextObject.cs) for more information. [Out-of-box plugins](https://github.com/xupefei/QuickLook/tree/master/QuickLook.Plugin) contain more detailed implementation.
Note that any plugin must be under the `QuickLook.Plugin` namespace, has the filename similar to `QuickLook.Plugin.YourPlugin.dll` and placed under `<Application>\Plugins\QuickLook.Plugin.YourPlugin\` subfolder.

## Related projects

QuickLook is standing on shoulders of several open-source libraries, named

 - [Font-Awesome-WPF](https://github.com/charri/Font-Awesome-WPF): WPF & UWP controls for the iconic font and CSS toolkit Font Awesome
 - [SharpCompress](https://github.com/adamhathcock/sharpcompress): a fully managed C# library to deal with many compression types and formats
 - [WpfWebBrowserWrapper](https://www.codeproject.com/Articles/555302/A-better-WPF-Browser-Control-IE-Wrapper): a better WPF-Browser-Control (IE-Wrapper)
 - [PreviewHandlerHost](http://www.brad-smith.info/blog/archives/79): IPreviewHandler Revisited
 - [ExifLib](https://www.codeproject.com/Articles/36342/ExifLib-A-Fast-Exif-Data-Extractor-for-NET): a fast Exif data extractor for .NET 2.0+
 - [dcraw](http://www.cybercom.net/~dcoffin/dcraw/): decoding raw digital photos in Linux
 - [ImageMagick](http://www.imagemagick.org): convert, edit, or compose bitmap images
 - [Magick.NET](https://github.com/dlemstra/Magick.NET): The .NET wrapper for the ImageMagick library
 - [XamlAnimatedGif](https://github.com/XamlAnimatedGif/XamlAnimatedGif): a simple library to display animated GIF images in XAML apps
 - [markdown-it](https://github.com/markdown-it/markdown-it): markdown parser, done right. 100% CommonMark support, extensions, syntax plugins & high speed
 - [github-markdown-css](https://github.com/sindresorhus/github-markdown-css): The minimal amount of CSS to replicate the GitHub Markdown style
 - [MuPdf](https://mupdf.com/): lightweight PDF, XPS, and E-book viewer
 -  [Sumatra PDF](https://www.sumatrapdfreader.org): a PDF, ePub, MOBI, CHM, XPS, DjVu, CBZ, CBR reader for Windows
 - [FFmpegMediaElement](https://github.com/unosquare/ffmediaelement/tree/master/Unosquare.FFmpegMediaElement): WPF MediaElement replacement based on FFmpeg
 - [FFmpeg](https://ffmpeg.org/): a complete, cross-platform solution to record, convert and stream audio and video
 - [AvalonEdit](https://github.com/icsharpcode/AvalonEdit): the WPF-based text editor component used in SharpDevelop

## Licenses

![LGPL-v3](http://www.gnu.org/graphics/lgplv3-147x51.png)

Application icons made by Freepik from www.flaticon.com. Used under the [Flaticon Basic License](http://file000.flaticon.com/downloads/license/license.pdf).

All source codes, except which are from other projects mentioned in “Related projects” section, are licensed under [LGPL-3.0](https://opensource.org/licenses/LGPL-3.0).

If you want make any modification on these source codes while keeping new codes not protected by LGPL-3.0, please contact me for a sublicense instead.
