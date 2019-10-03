### Create a linux command ( alias )

creating terminal commands will help us to win a lot of time , to define it in linux (also in osx) 
we need to go to `~/.profile` if it doesn't exist just create one and add a line like this for ur new command 
`alias <command name>="<command line to execute"` so let's take an exemple for the famous laravel running server command

`alias pas="php artisan serve"` and then we need to refresh our profile to take new lines by executing `. ~/profile`

now we can go to our laravel project and run it directly by using `pas` instead of `php artisan serve` cool isn't it ?

enjoy :) 
