# How to set line thickness

### While you can't directly set line thickness with `gd`, you can emulate thick lines by drawing multiple thin lines:

```php
<?php

$im = imagecreatetruecolor(400, 300);

$c_black = imageColorAllocate($im, 0,0,0);
$c_green = imageColorAllocate($im, 46,204,64);

for ( $thick = 5; $thick > 0; $thick-- ) {
  imageline($im, 50, 50 + $thick, 350, 250 + $thick, $c_green);
}


imagePng($im, '/tmp/image.png');
```

- `imagecreatetruecolor` - creates true color [lib:GD](https://onelinerhub.com/php-gd/how-to-install-gd-for-php-on-ubuntu-ubuntuversion) image object with specified width & height
- `imageColorAllocate` - creates color object to later use in image
- `imageline` - draws line using given coordinates and color
- `$thick = 5` - resulting line thickness (`5` in our case)
- `imagePng` - saves image in PNG format to the given path

group: line

## Example: 
```php
<?php

$im = imagecreatetruecolor(400, 300);

$c_black = imageColorAllocate($im, 0,0,0);
$c_green = imageColorAllocate($im, 46,204,64);

for ( $thick = 5; $thick > 0; $thick-- ) {
  imageline($im, 50, 50 + $thick, 350, 250 + $thick, $c_green);
}


imagePng($im, '/tmp/image.png');
```

