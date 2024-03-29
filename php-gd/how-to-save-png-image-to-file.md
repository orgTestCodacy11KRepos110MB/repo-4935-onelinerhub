# How to save PNG image to file

```php
$im = imagecreatetruecolor(400, 300);

# ...

imagepng($im, '/tmp/image.png');
```

- `imagepng` - saves given image resource in `PNG` format
- `imagecreatetruecolor` - creates true color [lib:GD](https://onelinerhub.com/php-gd/how-to-install-gd-for-php-on-ubuntu-ubuntuversion) image object with specified width & height
- `/tmp/image.png` - path to file save image to

group: save_formats

## Example: 
```php
<?php

$im = imagecreatetruecolor(400, 300);

$c_black = imageColorAllocate($im, 0,0,0);
$c_green = imageColorAllocate($im, 46,204,64);

imageellipse($im, 200, 150, 100, 100, $c_green);

imagepng($im, '/tmp/image.png');
```

