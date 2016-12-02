
##初进公式的流程（process）
>1 下载项目，一般公司会有自己的github或者svn 
 
### git的配置ssh和用户名以及邮箱
 这些配置是为了以后领导看你的代码或者qa测试给你提bug的时候用
 ```
    $ git config --global user.name "xxxx"
    $ git config --global user.email "xxxxx"
```
###生成密钥
  ```  
  $ ssh-keygen -t rsa -C "xxxx"
  ```
>连续3个回车。如果不需要密码的话。
最后得到了两个文件：id_rsa和id_rsa.pub。
文件地址 ：C:\Users\Administrator\.ssh
或者使用命令行 $ cat ~/ssh/id_rsa.pub

当然，你也可以直接使用nodepad++等编辑器打开这个文件，复制出来。 
将获得的public key添加在github账户上：


![Alt text](./1480389806709.png)


###ssh key添加到github上
右上角点击头像-> 点击settings-> 点击SSH KEYS-> 点击ADD SSH KEYS-> 将获取的public key粘贴于此
![Alt text](./1480389395046.png)
![Alt text](./1480389444923.png)
![Alt text](./1480389544517.png)
5、测试：
    $ ssh -T git@github.com
你将会看到：

    The authenticity of host 'github.com (207.97.227.239)' can't be established.
    RSA key fingerprint is 16:27:ac:a5:76:28:2d:36:63:1b:56:4d:eb:df:a6:48.
    Are you sure you want to continue connecting (yes/no)?
选择 yes

xxx! You've successfully authenticated, but GitHub does not provide shell access.
如果看到Hi后面是你的用户名，就说明成功了。

##你已经有权限下载了
git clone 地址 

