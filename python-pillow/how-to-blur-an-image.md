# How to blur an image

```python
from PIL import Image, ImageFilter

im = Image.open('/var/www/examples/heroine.png')
im = im.filter(ImageFilter.BoxBlur(10))

im.show()
```

- `PIL` - import [lib:Pillow](https://onelinerhub.com/python-pillow/how-to-install-python-pillow-module) package modules
- `Image.open` - open given image with Pillow
- `/var/www/examples/heroine.png` - path to sample image to open
- `.filter(` - add specified filter to an image
- `ImageFilter.BoxBlur` - blur type we use
- `10` - blur radius (strength of blur, the larger the more blurry image we get)
- `.show()` - displays resulting image

group: blur

## Example: 
```python
from PIL import Image, ImageFilter

im = Image.open('/var/www/examples/heroine.png')
im = im.filter(ImageFilter.BoxBlur(10))

im.show()
```

