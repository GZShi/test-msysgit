msysgit note
================

### 生成SSH
``` bash
$ cd ~/.ssh  
$ ssh-keygen -t rsa -C "email@host.com"  
```  
在输入文件名的时候直接`Enter`   
接下来是输入密码和确认密码  

### 提交SSH
* 打开Github
* 打开“Account Settings”
* 点击左侧边栏的“SSH Key”
* 点击“Add SSH Key”
* 然后把本地`~/.ssh/id_rsa.pub`中的内容复制进去
* 点击“Add key”完成

### 第一次与github连接
``` bash
$ ssh -T git@github.com  
```  
会提示输入用户名和密码  

[github help](https://help.github.com/articles/generating-ssh-keys);  

### 克隆repo
``` bash
$ git clone git https://github.com/[username]/[reponame].git  
```

### 添加文件
``` bash
$ git add .			# 所有文件  
$ git add *.txt  	# 指定后缀  
```  

### 提交修改
``` bash  
git commit -m "commit log" -a   # 提交所有修改  
git commit -m "add a file" readme.md	# 提交一个文件修改  
```  

### 本地远程同步  
``` bash  
$ git remote add origin https://github.com/[username]/[reponame].git  
$ git push -u origin master  
```  