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

程序说明：
API_KEYS: 这是你的四个API Key的列表。
input_folder: 设置你要压缩的图片所在文件夹路径。
output_folder: 压缩后的图片将保存到此文件夹下，如果文件夹不存在，程序会自动创建。
compress_image: 这个函数用于压缩单张图片并保存结果。
main: 主函数负责遍历文件夹中的所有图片，调用API进行压缩，并在处理450张图片后切换API Key。
使用方法：
替换脚本中的YOUR_API_KEY_X为你实际的API Key。
设置input_folder为你图片所在的目录路径。
运行脚本，压缩后的图片将会保存在compress文件夹下。
这个脚本会根据图片数量自动切换API Key，当所有API Key都用完时，程序会停止执行。如果图片数量超过了所有API Key的总限额，部分图片可能无法被压缩。
