# stardust
星座検出プログラム  

|input|output|
|---|---|
|<img src="./example_input.JPG" width=400px>|<img src="./example_output.JPG" width=400px>|
 

## requirements
```
opencv-python==3.4.0
numpy==1.14.0
```  

## Usage
```
$ git clone https://github.com/takasa5/stardust
$ cd stardust
```
```python
from stardust import Stardust
import Constellation

# 入力画像のパスで初期化
sd = Stardust("./input.jpg")
# 検出したい星座を指定
cs = Constellation.Sagittarius() # いて座
# 星座線を引く(あれば)
sd.draw_line(cs.get())
# 画像を返す
ret = sd.get_image()
# cv2.imshow()なり cv2.imwrite()なりする
```

## TODO
- 精度向上
- 星座データを追加する
    - 現状はいて座(Sagittarius)とペルセウス座(Perseus)のみ
    - データを紹介してくれる方、撮影した写真を提供してくれる方を募集しています
