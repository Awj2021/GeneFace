# Modification
记录在运行过程中的一些bugs, 以及相应的解决方案；
## Environment Setting.
- 3090:
如果有3090的显卡，为了方便，直接通过.yaml文件进行安装(此处直接忽略install_guide.md) 
环境安装完成之后，为了验证环境的有效性，参考install_guide.md, 对环境进行验证(**Verification of the Installation**)  

在使用**geneface_rtx3090.yaml**进行安装的时候，需要手动先删除其中的一些不存在的安装包
```
# .yaml文件中删除的package. 主要是0.0.0.
= 0.0.0
```

```
conda env create -f geneface_rtx3090.yaml
# 如果创建env的过程遇到一些错误
conda activate geneface
conda env update --file geneface_rtx3090.yaml --prune   
pip install dominate
```

