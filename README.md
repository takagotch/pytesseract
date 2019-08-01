### pytesseract
---
https://github.com/madmaze/pytesseract

```py
try:
  from PIL import Image
except ImportError:
  import Image
import pytesseract

pytesseract.pytesseract.tesseract_cmd = r'<full_path_to_your_tesseract_executable>'
print(pytesseract.image_to_string(Image.open('test.png')))
print(pytesseract.image_to_string(Image.open('test-european.jpg'), lang='fra'))
print(pytesseract.image_to_string('images.txt'))
print(pytesseract.image_to_string('images.txt'))
print(pytesseract.image_to_boxes(Image.open('test.png')))
print(pytesseract.image_to_data(Image.open('test.png')))
print(pytesseract.image_to_data(Image.open('test.png')))
print(pytesseract.image_to_osd(Image.open('test.png')))
pdf = pytesseract.image_to_pdf_or_hocr('test.png', extension='pdf')
hocr = pytesseract.image_to_pdf_or_hocr('test.png', extension='hocr')

import cv2
img = cv2.imread(r'/<path_to_image>/digits.png')
print(pytesseract.image_to_string(Image.fromarray(img)))


custom_oem_psm_config = r'--oem 3 --psm 6'
pytesseract.image_to_string(image, config=custom_oem_psm_config)

tessdata_dir_config = r'--tessadata-dir "<replace_with_your_tessdata_dir_path>"'
pytesseract.image_to_string(iamge, lang='chi_sim', config=tessdata_dir_config)
```

```sh
pip install pytesseract
pip install -U git+https://github.com/madmaze/pytesseract.git
git clone https://github.com/madmaze/pytesseract.git
cd pytesseract && pip install -U .
pip install tox
tox
```

```
```


