# 生态

## LIB | 标准库
包含了以下支持版本

语言 | OneDice 版本 | 主要作者 | 项目地址
:-: | :-: | :-: | :--
Python | V1 | [lunzhiPenxil](https://github.com/lunzhiPenxil) | [OlivOS-Team/lib-onedice/python](https://github.com/OlivOS-Team/lib-onedice/tree/main/python)
Kotlin | V1 | [zhaodice](https://github.com/zhaodice) | [OlivOS-Team/lib-onedice/kotlin](https://github.com/OlivOS-Team/lib-onedice/tree/main/kotlin)
Rust | V1 | [abrahum](https://github.com/abrahum) | [abrahum/diro](https://github.com/abrahum/diro)
Node.js | V1 | [Nanahira](https://twitter.com/Nana_Yumesaki) | [onedice.js](https://github.com/koishijs/onedice.js)

### Python 版本
![Pypi](https://img.shields.io/pypi/v/onedice.svg)

#### 安装

##### 从 PyPI 安装（推荐）

- 使用 pip

```
pip install onedice
```

#### 使用
##### 参考代码
```python
import onedice

dice = onedice.RD("(1d8+2d100)*1d10")
dice.roll()
print(dice.resInt)
print(dice.resError)
```

##### 输出结果
```
1296
None
```

### Node.js 版本

#### 安装

```
npm install onedice
```

#### 使用

##### 参考代码
```ts
import { OneDice } from 'onedice'

const onedice = new OneDice()
console.log(dice.calculate('(1d8+2d100)*1d10'))
```
