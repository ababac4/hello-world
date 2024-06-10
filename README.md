markdown测试文本

# github入门：

## 关键字查询
**xx(python) awesome**:查该标签下的xx
(Python)项目

**xx(python) tutorial**:查询xx(python)资料、书
籍、文档

**xx(socket)**
sample:查询对应技术(socket)的
代码样本

## github三要素
### Repository 仓库
仓库是github项目管理存储基本单位
一个仓库中存储一个项目，一个用户可以拥有多个仓
库，一般仓库分为public，private
<br>
### Commit 提交:
程序员在整个开发周期，有大量的对代码资源的选代

和修改，都可以通过commit的方式进行记录,便于程

序员回溯代码, 即使这些代码被删除

提交便于使用者观察整个工程的开发流程以及设计流
程
<br>
### Branch 分支:
在仓库中可以包含多个分支，分支才是代码文件的第
一存储单位，默认的仓库主分支为master/main
\*不仅可以管理代码存储，便于多人协作开发
合作图
![https://picture.gptkong.com/20240610/1555388086acf44e46b35e6c2766a6e6e1.png](https://picture.gptkong.com/20240610/1555388086acf44e46b35e6c2766a6e6e1.png])

## 仓库内容
1. Code，资源存储，代码资源，
二进制，项目管理脚本，许可证等等

2. issues，使用时遇到的bug 或 进行提交，等待反馈
README，使用markdown语言编写，工程自述文
件，开发进度，，版本更新，使用介绍等等

3. LICENSE 许可证:GPL2.0,3.0.Apahce 2.0，Mit，这
些许可证，给使用者最大使用权限以及最少的限制


## Git软件，分布式版本控制系统
仓库管理软件，使用git管理私人代码或企业代码



## 设备认证

1. 让网站的账户与设备绑定，后续完成代
码的管理，上传下载
  * **初始化仓库**

  ```bash
   git init //// 创建本地仓库
*后续对仓库的操作，都要在仓库位置(master)
   ```
   <br>
  ```bash
  git config --list //查看git环境变量
  ``` 
  <br>
  * **修改或添加config配置项**
  ```bash
  git config --global user.name//用户名
  git config --global user.email//注册邮箱
  ```
  * **生成本机设备密文**
  ```bash
  ssh-keygen -t rsa -c“注册邮箱"   # 创建本地密文 *去对应的目录下查找密文文件
  ```
  <br>
  点击new sshkey将复制的密文复制进去即可
  ![如下](https://picture.gptkong.com/20240610/1608d5cc79dfd44872a42ab80cfae42342.png)

   * **测试关联是否完成**
   ```bash
   ssh -T git@github.com//ssh远程登录
   ```
   <br>
   如果报端口错误

   去路径C:\Program Files\Git\etc\ssh\ssh_config
   添加config文件
   <br>
   输入以下内容
   ```bash
   Host github.com
   User //自己邮箱
   Hostname ssh.github.com
   PreferredAuthentications publickey
   IdentityFile ~/.ssh/id_rsa
   Port 443
   ```
2. **为目标仓库起别名，定位目标仓库，后
续上传**
   * 定位仓库
   ```bash
git remote add test(别名)SSH地址 (云端仓库
地址)
git remote remove test
#删除地址别名
   ```

## 本地设备与云端仓库的交互逻辑



\<br\>换行符号
\# 数目为标题大小
<br>

# 一级标题
## 二级标题
### 三级标题

两个段空格也能分开

*测试文本1*
<br>
**测试文本2**
<br>
***测试文本3***
<br>
~~测试文本4~~

测试文本5 强调`关键字`
## 分割符  \-\-\- 或者\*\*\*
---


## 引用 \> 数目有关
> 一级引用
>> 二级引用
>>> 三级引用

## 无序列表 \*
* 一级列表
 * 二级列表

## 有序列表 1.
1. 一级列表
  2. 二级列表
  3. 二级2列表

## 混合列表
1. 一级列表
  * 无序一级
  2. 二级列表


## 表格
人|身高|体重
-|:--:|-:
你好|124|45
不好|51|51

## 代码片段

```c
#include<stdio.h>
int main()
{
return 0;
}
```

```cpp
#include<iostream>
using namespace std;
```
##超链接: \[\]\(\)  图片为\!\[\]\(\)

[github](https://github.com/)
