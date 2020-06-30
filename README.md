Django知识点集锦
---
* 系列简介  
    大家好, 在本系列视频中, 我将以短视频的方式逐个讲解Django知识点, 讲解过程中通常会辅以示例代码或截图. 
    
    相比之阅读帮助文档, 也许有些朋友更喜欢视频教程, 这就是本系列视频的目的: 做一个视频版的帮助文档.
    
    我无法保证会一直更新下去. 但我会尽力去做. 
    
    知识点目录参考了官方文档 [**Using Django**](https://docs.djangoproject.com/en/3.0/topics/), 不完全一致.
    
    点击以下的每个章节链接都会跳转到对应的**Branch**, 也可以在Github Branch中搜索你想看的章节
    
    欢迎在 [**Issues**](https://github.com/208352363/Using_Django/issues) 面板中提出你的问题，建议和观点.
* 操作指南 
```shell script
# 克隆仓库到本地
git clone https://github.com/208352363/Using_Django.git
# 查看所有分支(章节), 建议在Git Bash窗口中运行以避免乱码
git branch
# 切换分支(章节) `git checkout 分支名称` 例如:
git checkout Model和数据库-Model-Model简介
```
* 准备工作
    * [安装Python](https://github.com/208352363/Using_Django/tree/%E5%87%86%E5%A4%87%E5%B7%A5%E4%BD%9C-%E5%AE%89%E8%A3%85Python)
    * [安装Git](https://github.com/208352363/Using_Django/tree/%E5%87%86%E5%A4%87%E5%B7%A5%E4%BD%9C-%E5%AE%89%E8%A3%85Git)
    * [安装Pycharm](https://github.com/208352363/Using_Django/tree/%E5%87%86%E5%A4%87%E5%B7%A5%E4%BD%9C-%E5%AE%89%E8%A3%85Pycharm)
    * [(可选)安装MySQL](https://github.com/208352363/Using_Django/tree/%E5%87%86%E5%A4%87%E5%B7%A5%E4%BD%9C-(%E5%8F%AF%E9%80%89)%E5%AE%89%E8%A3%85MySQL)
    * [(可选)安装Postman](https://github.com/208352363/Using_Django/tree/%E5%87%86%E5%A4%87%E5%B7%A5%E4%BD%9C-(%E5%8F%AF%E9%80%89)%E5%AE%89%E8%A3%85Postman)
    * [(可选)安装FireFox Developer Edition](https://github.com/208352363/Using_Django/tree/%E5%87%86%E5%A4%87%E5%B7%A5%E4%BD%9C-(%E5%8F%AF%E9%80%89)%E5%AE%89%E8%A3%85FireFox-Developer-Edition)
    * [创建项目(使用Pycharm或命令行)](https://github.com/208352363/Using_Django/tree/%E5%87%86%E5%A4%87%E5%B7%A5%E4%BD%9C-%E5%88%9B%E5%BB%BA%E9%A1%B9%E7%9B%AE(%E4%BD%BF%E7%94%A8Pycharm%E6%88%96%E5%91%BD%E4%BB%A4%E8%A1%8C))
    * [项目的Git和Github配置](https://github.com/208352363/Using_Django/tree/%E5%87%86%E5%A4%87%E5%B7%A5%E4%BD%9C-%E5%88%9B%E5%BB%BA%E9%A1%B9%E7%9B%AE(%E4%BD%BF%E7%94%A8Pycharm%E6%88%96%E5%91%BD%E4%BB%A4%E8%A1%8C)#-3)
    * [常用配置(settings.py)](https://github.com/208352363/Using_Django/tree/%E5%87%86%E5%A4%87%E5%B7%A5%E4%BD%9C-%E5%B8%B8%E7%94%A8%E9%85%8D%E7%BD%AE(settings.py))
    * [懒人运行manage.py的方法](https://github.com/208352363/Using_Django/tree/%E5%87%86%E5%A4%87%E5%B7%A5%E4%BD%9C-%E6%87%92%E4%BA%BA%E8%BF%90%E8%A1%8Cmanage.py%E7%9A%84%E6%96%B9%E6%B3%95)
* Model和数据库
    * Model
        * [Model简介](https://github.com/208352363/Using_Django/tree/Model%E5%92%8C%E6%95%B0%E6%8D%AE%E5%BA%93-Model-Model%E7%AE%80%E4%BB%8B)
        * [Field简介](https://github.com/208352363/Using_Django/tree/Model%E5%92%8C%E6%95%B0%E6%8D%AE%E5%BA%93-Model-Field%E7%AE%80%E4%BB%8B)
        * Field一对一,多对一,多对多
        * Model之Meta,属性,方法
        * Model继承
            * 抽象父类
            * 多表继承
            * 代理Model
* 处理Http请求
    * 处理URL
        * [Django如何处理请求](https://github.com/208352363/Using_Django/tree/%E5%A4%84%E7%90%86Http%E8%AF%B7%E6%B1%82-%E5%A4%84%E7%90%86URL-Django%E5%A6%82%E4%BD%95%E5%A4%84%E7%90%86%E8%AF%B7%E6%B1%82)
* 使用表单
    * [Django表单简介](https://github.com/208352363/Using_Django/tree/%E4%BD%BF%E7%94%A8%E8%A1%A8%E5%8D%95-Django%E8%A1%A8%E5%8D%95%E7%AE%80%E4%BB%8B)
* 处理文件
    * [在Model中使用文件](https://github.com/208352363/Using_Django/tree/%E5%A4%84%E7%90%86%E6%96%87%E4%BB%B6-%E5%9C%A8Model%E4%B8%AD%E4%BD%BF%E7%94%A8%E6%96%87%E4%BB%B6)
    * File对象
    * [文件存储(方式)](https://github.com/208352363/Using_Django/tree/%E5%A4%84%E7%90%86%E6%96%87%E4%BB%B6-%E6%96%87%E4%BB%B6%E5%AD%98%E5%82%A8(%E6%96%B9%E5%BC%8F))