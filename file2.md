# 账号与主机关联

* 测试是否关联过 ssh -T git@github.com
* 修改本地配置文件，在配置文件中添加两项
 * 查看配置项 git config --list
 * 添加配置项 git config --global user.name "用户名"
 * 添加配置项 git config --global user.email "邮箱"
* 修改本机密钥RSA ssh-keygen -t rsa -C "邮箱"
* 找到密钥位置，复制密文，粘贴到网站账户中的对应位置，就完成认证

# 生成仓库地址，将内容上传到指定仓库

* 添加仓库   	    git remote add origin "SSH仓库地址"
* 删除仓库   	    git remote remove origin
* 添加缓冲区 	    git add 文件名
* 提交文件   	    git commit -m "备注"
* 上传云端   	    git push origin master
* 查看本地仓库状态 git status

# 删除文件
* 删缓冲区  rm 文件名
* 删仓库    git rm 文件名
* 提交
* 上传云端

# 推拉操作（云端版本与仓库版本不一致，导致推失败）
* 推操作 git push origin master 
* 拉操作 git pull --rebase origin master


# 下载开源项目资源
* git clone HTTP地址

# 云端仓库与本地不一致，导致无法正常值 （先拉再推）
* git pull --rebase origin master
* git status 查看冲突及解决方法
* git rebase --skip 跳过冲突，放弃本地内容
* git rebase --continue 版本合并

