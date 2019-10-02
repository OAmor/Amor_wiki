### Imagick installation 
ImageMagick is a php module whiche help to make full modification to your images (resizing,cropping ..) 
First we need to install ImageMagick module using brew `brew install ImageMagick` for mac or `apt-get` for linux
we can test it using `convert --list ` to check if it's properly installed

after that we need to generate the `.so` extension file to add it in `php.ini` for that we use `pecl` but 
before we need to confirm that we use `pecl` of `php 5.6` 'or whatever the php version used to run the project' to generate the compatible extension
file we can find it in `/usr/local/php5/bin/pecl install imagick` and now we need just to add `extension = imagick.so
` in `php.ini` file 