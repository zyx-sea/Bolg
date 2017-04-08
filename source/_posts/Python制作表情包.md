---
title: Python自动生成表情包
---

## Python自动生成表情包


>在微信公众号（清华大数据）看到的，Python利用PIL生成表情包感觉很有趣。

## 材料准备

![表情包背景](https://raw.githubusercontent.com/zyx-sea/zyx-sea.github.io/master/images/di.jpg)

![表情包表情](https://raw.githubusercontent.com/zyx-sea/zyx-sea.github.io/master/images/shang.jpg)



## 代码实现

```
from PIL import Image,ImageDraw,ImageFont
img=Image.open("F:\Python练习\表情包制作\di.jpg")
jgz=Image.open("F:\Python练习\表情包制作\shang.jpg")
img.paste(jgz,(73,42))
##img.show()

draw=ImageDraw.Draw(img)
ttfront=ImageFont.truetype('simhei.ttf',24)
draw.text((32,190)," 内心毫无波澜\n  甚至还想笑",fill=(0,0,0),font=ttfront)
img.show()
img.save("F:\Python练习\表情包制作\生成的表情包.jpg")
```
## 成果

![生成的表情包](https://raw.githubusercontent.com/zyx-sea/zyx-sea.github.io/master/images/生成的表情包.jpg)