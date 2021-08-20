# go-mosaic

[<img src="https://img.shields.io/github/license/esrrhs/go-mosaic">](https://github.com/esrrhs/go-mosaic)
[<img src="https://img.shields.io/github/languages/top/esrrhs/go-mosaic">](https://github.com/esrrhs/go-mosaic)
[![Go Report Card](https://goreportcard.com/badge/github.com/esrrhs/go-mosaic)](https://goreportcard.com/report/github.com/esrrhs/go-mosaic)
[<img src="https://img.shields.io/github/v/release/esrrhs/go-mosaic">](https://github.com/esrrhs/go-mosaic/releases)
[<img src="https://img.shields.io/github/downloads/esrrhs/go-mosaic/total">](https://github.com/esrrhs/go-mosaic/releases)
[<img src="https://img.shields.io/docker/pulls/esrrhs/go-mosaic">](https://hub.docker.com/repository/docker/esrrhs/go-mosaic)
[<img src="https://img.shields.io/github/workflow/status/esrrhs/go-mosaic/Go">](https://github.com/esrrhs/go-mosaic/actions)

go-mosaic是一个制作相片马赛克的工具。相片馬賽克，或稱蒙太奇照片、蒙太奇拼貼，是一種影像處理的藝術技巧，利用這個方式做出來的圖片，近看時是由許多張小照片合在一起的，但遠看時，每張照片透過光影和色彩的微調，組成了一張大圖的基本像素，就叫做相片馬賽克技巧

[README_EN](./README_EN.md)

# 特性
* 专为海量图片设计，可支持数百万张图片
* 内建缓存数据库，图片删除、更改自动从缓存剔除
* 多核构建，加载、计算、替换均为并发

# 使用
* 克隆项目，编译，或者下载[release](https://github.com/esrrhs/go-mosaic/releases)
* 执行命令，等待完成
```
./go-mosaic -src input.png -target output.jpg -lib ./test
```
* 其中./test为图片文件夹，用来组成最终图片的元素。input.png为目标图片，用来生成最终的大图output.jpg。素材图片越多，生成越精确
* 更多参数，参考help
```
Usage of D:\project\go-mosaic\test.exe:
  -checkhash
    	check database pic hash (default true)
  -database string
    	cache datbase (default "./database.bin")
  -lib string
    	image lib path
  -libname string
    	image lib name in database (default "default")
  -maxsize int
    	pic max size in GB (default 4)
  -pixelsize int
    	pic scale size per one pixel (default 64)
  -scalealg string
    	pic scale function NearestNeighbor/ApproxBiLinear/BiLinear/CatmullRom (default "CatmullRom")
  -src string
    	src image path
  -srcsize int
    	src image auto scale pixel size (default 128)
  -target string
    	target image path
  -worker int
    	worker thread num (default 12)
```

# 示例
![image](./images/input.png)
![image](./images/smalloutput.png)


