Google Cloud의 virtual computer를 이용한 개발용 개인 서버
========================================================

아이패드, 노트북, 데스크탑에서 같은 개발환경에서 개발하기 위해서 Google Cloud에서 무료로 VM 인스턴스를 할당 받았다. 

튜토리얼은 다음 영상을 참고했다.

튜토리얼: https://www.youtube.com/watch?v=u7LvG-deMOE&t=41s

해당 인스턴스 설정에 내 컴퓨터, 아이패드, 노트북에서 접속하기 위해서 해당 컴퓨터에 rsa 공개키를 만들고 인스턴스 설정에 추가해줘야한다.

rsa 공개키 설정 방법및 인스턴스 접속 방법은 다음 튜토리얼을 참고했다.

튜토리얼: https://jybaek.tistory.com/611

공개키를 생성하고 인스턴스에 등록까지 마쳤다면 이제 서버에 접속할 수 있다.

다음 명령어로 접속하자.

```
$ ssh -i [키 경로] [사용자이름]@[외부 아이피주소]
```

Vimrc를 이용한 Vim 플러그인 설치
========================================================
Vim이라는 에디터는 개발자들이 사용하는 에디터 중 가장 오래된 것 중 하나이다.

그런 만큼 단순하고 개발자들이 필요로하는 기능에 대한 플러그인들이 잔뜩있다.   
(누가 말하기를 현재 나온 에디터들이 지원하는 모든 기능은 vim 플러그인으로 이미 존재한다고...)

그렇기에 Vim에 플러그인 설치하는 방법과 미리 세팅해 둔 Vimrc 파일로 쉽게 플러그인을 설치할 방법을 정리 해둔다.

먼저 플러그인 관리용 플러그인 'Vundle' (bundle+vim인듯) 설치해야한다. 
```
$ git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```
튜토리얼은 다음을 참고했다.

튜토리얼: https://nolboo.kim/blog/2016/09/20/vim-plugin-manager-vundle/

Vundle을 git에서 클론 했다면 vimrc 파일을 root폴더로 옮긴 후 vim으로 열어 다음 명령어를 실행시키자  

```
:PluginInstall
```

vimrc에 적혀있는 플러그인들이 자동으로 설치되는 모습을 볼 수 있을 것이다.  
내가 현재 사용하고 있는 플러그인들은 다음과 같다. 링크를 타고 들어가면 각 플러그인들의 설명이 있다.  
+tagbar같은 경우 사용하는 언어의 태그가 설치되어있어야한다. 나 같은 경우 C++로 요즘 알고리즘을 풀기 때문에 Ctags를 설치해야 했다. 
```
$ sudo apt install ctags
```
Ctags 튜토리얼: https://danguria.tistory.com/207  

부록(https://github.com/klange/nyancat)  

* 플러그인 링크  
'nanotech/jellybeans.vim' - https://github.com/nanotech/jellybeans.vim  
'majutsushi/tagbar' - https://github.com/majutsushi/tagbar  
'scrooloose/nerdtree' - https://github.com/scrooloose/nerdtree-git-plugin  
'nathanaelkane/vim-indent-guides' - https://github.com/nathanaelkane/vim-indent-guides  
'airblade/vim-gitgutter' - https://github.com/airblade/vim-gitgutter  
'tpope/vim-fugitive' - https://github.com/tpope/vim-fugitive  
'vim-airline/vim-airline' - https://github.com/vim-airline/vim-airline  
'vim-airline/vim-airline-themes' - https://github.com/vim-airline/vim-airline-themes  
'blueyed/vim-diminactive' - https://github.com/blueyed/vim-diminactive  
