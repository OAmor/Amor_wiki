** GIT FTP **

Git ftp is a greate tool that lets you track ur server without need to a third part, just using ur git cli and knowledges 

### Instalation 
clone and cd to the dir 
`git clone https://github.com/git-ftp/git-ftp.git`
`cd git-ftp`

choose the newest release
`tag="$(git tag | grep '^[0-9]*\.[0-9]*\.[0-9]*$' | tail -1)"`

checkout the latest tag
`git checkout "$tag"`
`sudo make install`

### Usage
first u need to set ur env param ,go to ur project and 

set the url and server credentials 
`git config git-ftp.url ftp.example.net` u may need use an ftps
`git config git-ftp.user ftp-user`
`git config git-ftp.password gtp-secret`

u can see ans update these credentials in `.git/config` for ur project

i there is a security problem with ur server u can set the insecure var by 
`git config git-ftp.insecure true`

after that we have to options 
 - Ur server is empty and this is ur first upload so simply `git ftp init`
 - Ur server is not empty so we need to catchup by `git ftp catchup`

### Work and deploy
make any change in ur code like 
`echo "new content" >> index.txt`
add & commit new changes 
`git commit index.txt -m "Add new content"`
and simply use the magic word 
`git ftp push`
it will push just ur new changes 

enjou :)  
