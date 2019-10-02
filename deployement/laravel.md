### Laravel project deployement

The key folder in laravel project is the `/public` folder, there many methode to expose this folder
the best one (for me oc) is copy all ur laravel project to the `public_html` in ur server and put it in folder there
to keep things clear , lets say ur project now is in `public_html/project`
now u need to expose ur laravel publid folder , so u should move it's content from `public_html/project/public` to 
`public_html` , then go to `index.php` file and change this two line to adjust ne directories 

`require __DIR__.'/../vendor/autoload.php';` to `require __DIR__.'/../project/vendor/autoload.php';`
`$app = require_once __DIR__.'/../bootstrap/app.php';` to `$app = require_once __DIR__.'/../project/bootstrap/app.php';`

enjoy :) 