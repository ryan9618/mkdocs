# Dash   
### tags:
      - py
      - dash


```

import dash
from dash import html
import feffery_antd_components as fac
from dash.dependencies import Input, Output

# 实例化Dash应用对象
app = dash.Dash(__name__)

# 添加初始化页面内容
app.layout = html.Div(
    [
        fac.AntdTitle('你好！Dash!',level=3),
        fac.AntdText('Dash版本%s' % dash.__version__),
        fac.AntdDivider(),
        fac.AntdText('fac版本%s' % fac.__version__)

    ]
)


if __name__ == '__main__':
    app.run(debug=False)






'''

https://fac.feffery.tech/
环境搭建
在基于dash和fac进行应用开发之前，我们需要先搭建好所需的环境，推荐使用conda作为环境管理工具，这里以Python 3.7版本为例，在终端执行下列命令进行相关环境的创建及激活：
注：由于国内pypi相关镜像的更新延迟，通过其进行相关库的安装，版本可能滞后于原始pypi中的最新版本
默认方式
国内使用镜像
conda create -n dash-devs python=3.7 -c https://mirrors.aliyun.com/anaconda/pkgs/main/ -y
conda activate dash-devs
完成环境的创建及激活后，我们在对应环境中直接通过pip进行相关基础依赖库的安装即可：
默认方式
国内使用镜像
pip install dash feffery-antd-components -U -i https://pypi.tuna.tsinghua.edu.cn/simple

conda create -n pytest-devs python=3.8 -c https://mirrors.aliyun.com/anaconda/pkgs/main/ -y
conda create -n pymain-dev python=3.8 -c https://mirrors.aliyun.com/anaconda/pkgs/main/ -y


conda env list

'''
conda create -n pytest-dev python=3.9 -c https://mirrors.aliyun.com/anaconda/pkgs/main/ -y


conda create -n dash-devs python=3.8 -c https://mirrors.aliyun.com/anaconda/pkgs/main/ -y



```
```



```
