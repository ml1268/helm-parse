### design
1. 抽离helm的parse chart文件部分，使其成为一个独立的package，可以将helm支持的chart格式定义的各种模板文件，无差别的嵌入到各个开源组件中
    现阶段的目的是，不使用helm的tiller等其他功能，只抽离helm的render chart目录下模板的功能，满足在dashboard中，可以使用helm定义的模板及参数
    读取helm chart风格的模板，渲染生成对应yaml
