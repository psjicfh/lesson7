#lesson7笔记
##安装vim插件
	在网站http://www.vim.org/scripts/script.php?script_id=2540下载插件
	akaedu@akaedu-desktop:~$ unzip snipMate.zip -d ~/.vim
	"-d" 把解压的文件转移到"~/.vim" 目录下
	即：把插件snipMate.zip 解压到主用户目录下的“.vim” 文件夹
	使用方法:vim xxx.c
	按 main则：
	int main(int argc, const char *argv[])
	{
		
		return 0;
	}
	接着按fun则
	int main(int argc, const char *argv[]) 
	{ 
		void function_name()
		{
			/* code */
		}
		return 0;
	}
###插件小解
	akaedu@akaedu-desktop:~$ cd .vim
	akaedu@akaedu-desktop:~/.vim$ ls
	after  autoload  doc  ftplugin  plugin  snippets  syntax
	akaedu@akaedu-desktop:~/.vim$ cd snippets/
	akaedu@akaedu-desktop:~/.vim/snippets$ la
	autoit.snippets      java.snippets  python.snippets   tcl.snippets
	cpp.snippets         mako.snippets  ruby.snippets     tex.snippets
	c.snippets           objc.snippets  sh.snippets       vim.snippets
	html.snippets        perl.snippets  _.snippets        zsh.snippets
	javascript.snippets  php.snippets   snippet.snippets
	akaedu@akaedu-desktop:~/.vim/snippets$ vim c.snippets 
	akaedu@akaedu-desktop:~/.vim/snippets$ 
	自己加
	snippet dog
        	I love dogs  （注意格式）
  	其余的自己自学喽！

###刚进去一个文件在普通模式下按d+G即可删除当前光标到最后一行，看peter的公式
	yy -- to copy current line
	dd -- to cut the current line
	p  -- to paste
	#include <stdio.h>
	int main(int argc, const char *argv[])
	{
		printf("hello world!\n");

		printf("hello world!\n");
		printf("hello world!\n");
		printf("hello world!\n");
		printf("hello world!\n");
		printf("hello world!\n");
		printf("hello world!\n");
		printf("hello world!\n");
		printf("hello world!\n");
	}
 
###snipMate插件
	akaedu@akaedu-desktop:~$ unzip snipMate.zip -d ~/.vim
				 //"-d"的作用是压缩包解压到~/.vim目录下
	ctrl+n :补齐

###配置bash
	akaedu@akaedu-desktop:~$ vim .bashrc
	#alias for apt-get
	alias psjicfh='sudo apt-get install' #新加	

### akaedu@akaedu-desktop:~$ source .bashrc //相当于重启bash
### akaedu@akaedu-desktop:~$ psjicfh fortune
### akaedu@akaedu-desktop:~$ psjicfh cowsay // 安装两个软件
### akaedu@akaedu-desktop:~$ psjicfh fortune | cowsay
	 ___________________________________
	/ Don't look back, the lemmings are \
	\ gaining on you.                   /
	 -----------------------------------
		\   ^__^
		 \  (oo)\_______
		    (__)\       )\/\
			||----w |
			||     ||

###光标跳到行尾 end 跳到行首 home
###删除一个 Repository
    Dashboard -> 要删除的Repository -> 右上角 Admin -> 
    右下角Delete this repository
###删除仓库中的一个文件
    kaedu@akaedu-desktop:~/work/lesson7/lesson7_project$ vim lesson7_1.c
    akaedu@akaedu-desktop:~/work/lesson7/lesson7_project$ git add lesson7_1.c
    akaedu@akaedu-desktop:~/work/lesson7/lesson7_project$ git commit -a -m "less    on7_1.c"
    akaedu@akaedu-desktop:~/work/lesson7/lesson7_project$ git push
	//此时仓库lesson7_project中就有了两个文件 lesson7.c lesson7_1.c

    删除步骤：
    akaedu@akaedu-desktop:~/work/lesson7/lesson7_project$ git rm lesson7_1.c
    akaedu@akaedu-desktop:~/work/lesson7/lesson7_project$ git commit -a
    akaedu@akaedu-desktop:~/work/lesson7/lesson7_project$ git push
    删除仓库中的 lesson7_1.c 成功
