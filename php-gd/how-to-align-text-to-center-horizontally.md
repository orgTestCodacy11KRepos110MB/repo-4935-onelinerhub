# How to align text to center horizontally

```php
<?php

$im = imagecreatetruecolor(400, 300);

$c_black = imageColorAllocate($im, 0,0,0);
$c_green = imageColorAllocate($im, 46,204,64);
$text = 'Hi';

$font = '/usr/share/fonts/truetype/dejavu/DejaVuSans.ttf';
$p = imagettfbbox(40, 0, $font, $text);

imagettftext($im, 40, 0, (400 - $p[2])/2, 100, $c_green, $font, $text);
imagePng($im, '/tmp/image.png');
```

- `imagecreatetruecolor` - creates true color [lib:GD](https://onelinerhub.com/php-gd/how-to-install-gd-for-php-on-ubuntu-ubuntuversion) image object with specified width & height
- `imageColorAllocate` - creates color object to later use in image
- `$font` - path to `ttf` font to use
- `imagettfbbox` - return size of box that given text fits into
- `imagettftext` - draw text with given `ttf` font
- `(400 - $p[2])/2` - calculate `x` coordinate so our text is centered horizontally
- `imagePng` - saves image in PNG format to the given path

group: text

## Example: 
```php
<?php

$im = imagecreatetruecolor(400, 300);

$c_black = imageColorAllocate($im, 0,0,0);
$c_green = imageColorAllocate($im, 46,204,64);
$text = 'Hi';

$font = '/usr/share/fonts/truetype/dejavu/DejaVuSans.ttf';
$p = imagettfbbox(40, 0, $font, $text);

imagettftext($im, 40, 0, (400 - $p[2])/2, 100, $c_green, $font, $text);
imagePng($im, '/tmp/image.png');
```

