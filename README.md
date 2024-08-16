# TinyCompress
Tiny、图片压缩

通过chatgpt提示词生成的压缩代码，准备好tiny的key,由于单个key每月限制500张，程序支持了多个key

提示词：
、、、
tinypng 是一个非常好的图片网站，它提供一个api可以压缩图片，具体如下
curl https://api.tinify.com/shrink \
     --user api:YOUR_API_KEY \
     --data-binary @unoptimized.jpg \
     --dump-header /dev/stdout

我有1600张图片，网站限制一个key只能压缩450张，我现在有4个key，请帮忙编写python程序，循环遍历文件夹下的图片，调用它的api进行压缩，压缩后的文件放在 compress文件夹下。
、、、
