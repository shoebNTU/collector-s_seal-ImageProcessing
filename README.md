# collector-s_seal-ImageProcessing
This is a simple demo for processing stamp images.
(2020.1.20:*Update to SealsCharacters_Segmentation_1.02.py)



In classical materials, seals are often covered by handwritten words.

![](image/1CAC342D-ECE6-457C-AF2A-5D20C6D33EEA.png)

To split the seal areas from background ,we can project RGB three channels information of image into three-dimensional space

automatically extracts areas with more red components by using k-means clustering
![](image/binarization.png)

-------

The default value of K is 3.
Adjusting the results of seal‘s area extraction by adjusting the value of K
run:
```python
python3 Binarization.py --ImageSelecter=imageDir(default='test.jpg') --clusters=K
Ex.python Binarization.py --ImageSelecter=test.jpg  --clusters=3

```
to get results of Binarization.The generated file will be named Binarization(0-n).jpg
Select the file you want to segment to single character.

run:
```python
python3 SealsCharacters_Segmentation.py --ImageSelecter=imageDir(default='Binarization2.jpg') 
Ex.python3 SealsCharacters_Segmentation.py --ImageSelecter=Binarization2.jpg
```
Then you can see the Characters Segmentation result in the result folder.

![](image/2.gif)

Authors
-------

- @Kangying Li 


License
-------
