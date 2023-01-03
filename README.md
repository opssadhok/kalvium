# kalvium
Build a image exif cleanup app: the user can upload an image from camera (which typically has a lot of EXIF meta data attached). The backend removes all of this information, and returns the image back without any exif metadata.

// code 

from PIL import Image
from PIL.ExifTags import TAGS

import matplotlib.pyplot as plt
import numpy as np
import cv2

from google.colab import files
from io import BytesIO
from PIL import Image

uploaded = files.upload()
im = Image.open(BytesIO(uploaded['raju.jpg']))

plt.imshow(im)

from PIL import Image
from PIL.ExifTags import TAGS

print(im.geexif_table={}
for k, v in im.getexif().items():
    tag=TAGS.get(k)
    exif_table[tag]=v
print(exif_table)

texif())

exif_table={}
for k, v in im.getexif().items():
    tag=TAGS.get(k)
    exif_table[tag]=v
print(exif_table)

from PIL import Image

image = Image.open('raju.jpg')

# next 3 lines strip exif
data = list(image.getdata())
image_without_exif = Image.new(image.mode, image.size)
image_without_exif.putdata(data)

image_without_exif.save('raju.jpg')

