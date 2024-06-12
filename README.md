# GitHub
## 关键字查询：
	awesome：查该标签下的项目

	tutorial：查询资料、书籍、文档 

	sample：查询对应技术的代码样本
## GitHub三要素：
### Repository 仓库：
	仓库是github项目管理存储基本单位 

	一个仓库中存储一个项目，一个用户可以拥有多个仓库，一般仓库分为public， private
### Commit 提交：
	程序员在整个开发周期， 有大量的对代码资源的选代和修改， 都可以通过commit的方式进行记录, 便于程序员回溯代码, 即使这些代码被删除 

	提交便于使用者观察整个工程的开发流程以及设计流程
### Branch 分支：
	在仓库中可以包含多个分支，分支才是代码文件的第一存储单位，默认的仓库主分支为master/main 

	不仅可以管理代码存储， 便于多人协作开发

	

## 仓库内容
* Code，资源存储，代码资源，二进制，项目管理脚本，许可证等等
* issues，使用时遇到的bug 或 进行提交，等待反馈
* README，使用markdown语言编写，工程自述文件，开发进度，，版本更新， 使用介绍等等
* LICENSE 许可证：
	
	GPL2.0,3.0.Apahce 2.0，Mit，这些许可证，给使用者最大使用权限以及最少的限制
##Git软件，分布式版本控制系统
	仓库管理软件，使用git管理私人代码或企业代码


## 设备认证 
1. 让网站的账户与设备绑定，后续完成代码的管理，上传下载
	1. git init   // 创建本地仓库 
	2. git config -list   //查看git的配置文件修改或添加config配置项
	3. 修改或添加config配置项

	   	git config --global user.name  "用户名" 
	  
	   	git config --global user.email "邮箱" 
	4. 创建本地秘文

	   	ssh-keygen -t rsa -C “注册邮箱”

	   	rsa.pub复制密文，粘贴到settings->SSH key and GPG -> new ssh key ->粘贴    
	5. 测试关联是否完成
	   	ssh -T git@github.com    # ssh远程登录
2. 为目标仓库起别名，定位目标仓库，后续上传
	1. git remote add orgin(别名) SSH地址(云端仓库地址)
	2. git remote remove origin    #删除地址别名本地设备与云端仓库的交互逻辑
	3. git add code.c   #添加内容#将缓冲区数据提交到本地仓库
	4. git commit    #提交到本地仓库
	 
	   git commit -m "备注信息"    #生成提交记录
	5. git push origin(云端仓库地址) master    #将本地仓库内容推到云端仓库
	6. git status       #查看状态
	7. git rm code.c     #删除本地文件以及仓库中文件
	8. git restore code.c   #复位误删除文件（仓库存在）
## 代码更新的依赖关系被破坏
	本地内容要比云端新, 完成更新替换， 但是如果直接修改云端内容, 导致, 本地内容无法再次提交
	
	先拉取 git pull 云端内容 与本地内容合井或操作， 而后再次推即可
	
	git pull --rebase origin master
	1. git rebase --abort    #忽略新版，此时还不能上传
	2. git rebase --skip     #需略旧版，更新本地后可以上传
	3. git rebase --continue #版本合并，解决冲突后可以直接上下载开源代码
## 下载开源代码	
	git clone "https仓库地址”   #下载开源项目code资源分支Branch
## 分支Branch
	关于分支的相关命令， 创建分支、选择分支、合并分支等等
# Markdown语言
Markdown , 文本修饰语言 ， 用特殊符号修饰正文效果<br>

## 标题修饰符\#

# 标题修饰符（一级标题）
## （二级标题）
### （三级标题）
#### （四级标题）
##### （五极标题）


## 正文内容
   输入正文内容 ， 但是如果需要换行， 用\<br\>标签

## 修饰正文
   *一段测试文本*

   **一段测试文本**
   
   ***一段测试文本***
   
   ~~一段测试文本~~

   这是一段测试文本 ， 将`关键字`凸显

## 分割线
   
   用\-\-\- 表示分割线

---

## 引用效用\>表示
> 你自己就是一座金山 ，关键在于如何挖掘和利用自己 
>> 苏格拉底
>>> 三级引用
>>>> 四级引用

## 列表修饰符
### 无序列表 \*
* 二次元
  * 元神
    * 神力凌华
* 大逃杀类
  * PUBG
  * APEX

### 有序列表 1.
1. 物理学
   1. 粒子物理
   2. 原子核物理
   3. 凝聚态物理
2. 计算机科学
   1. 分布式架构
   2. 云计算

### 混合列表
1. 测试一级
   * 测试二级
   2. 测试三级

### 表格
名称|技能|排行
--|:--:|--:
蝙蝠侠|有钱|32
海王|游泳|16
闪电侠|跑|18

### 代码片段

```c
	#include<stdio.h>
	int main(void)
	{
		printf("test code\n");
		return 0;
	}
```

```cpp
	#include <iostream>
```

```python
	import <os>
```

```bash
	echo "测试"
	pwd
	ps aux
	ls -l
```

### 超链接技术

[Gitnub](https://www.github.com"点击访问")

### 插入图片
![]()
