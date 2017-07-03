# virtualenv - virtualenvwrapper

## 创建**env_test**的虚拟环境

* virtualenv env_test
    
    默认情况下，虚拟环境会依赖系统环境中的site packages，就是说系统中已经安装好的第三方package也会安装在虚拟环境中，如果不想依赖这些package，那么可以加上参数 **--no-site-packages** 建立虚拟环境

* virtualenv --no-site-packages env_test

* 可以使用-p PYTHON_EXE选项在创建虚拟环境的时候指定python版本
    
    virtualenv -p /usr/bin/python2.7 env_test

    virtualenv -p /usr/local/bin/python3.4 env_test
    
* 启动虚拟环境
  
    cd env_test
    
    source ./bin/activate
    
    注意此时命令行会多一个(env_test)，env_test为虚拟环境名称，接下来所有模块都只会安装到该目录中去。

* 退出虚拟环境
    
    deactivate

