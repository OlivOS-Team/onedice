# 生态

## LIB | 标准库
包含了以下支持版本

语言 | OneDice 版本 | 主要作者 | 项目地址
:-: | :-: | :-: | :--
Python | V1 | [lunzhiPenxil](https://github.com/lunzhiPenxil) | [OlivOS-Team/lib-onedice/python](https://github.com/OlivOS-Team/lib-onedice/tree/main/python)
Kotlin | V1 | [zhaodice](https://github.com/zhaodice) | [OlivOS-Team/lib-onedice/kotlin](https://github.com/OlivOS-Team/lib-onedice/tree/main/kotlin)
Rust | V1 | [abrahum](https://github.com/abrahum) | [abrahum/diro](https://github.com/abrahum/diro)
TypeScript | V1 | [Anillc](https://github.com/Anillc) | [Anillc/onedice](https://github.com/Anillc/onedice)
Node.js | V1 | [Nanahira](https://twitter.com/Nana_Yumesaki) | [onedice.js](https://github.com/koishijs/onedice.js)（非Koishi官方）

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
```bash
yarn add @onedice/core     # npm install @onedice/core
```

#### 示例
```typescript
import { dice } from '@onedice/core'

const [value, root] = dice('(7a3)d(5d(2^2)k3+5f+{qwq})+d', {
  env: {
    qwq: 'd'
  }
})
const details = root.toString()
// value: 133
// details: `{
//   A: ({
//     A: 7, B: 3, C: 8, E: 10
//     rounds: {
//       {<[9]>, <6>, <3>, 1, <[9]>, <3>, <[10]>}
//       {<6>, <6>, <[8]>, 1, <5>, <[10]>}
//       {<[10]>, <4>, <4>, <3>, <[8]>}
//       {<5>, <[9]>, <7>, <[8]>, 1}
//       {<5>, <[9]>, <[8]>, <7>}
//       {<5>, <[10]>, <3>, <[9]>}
//       {<7>, <[8]>, <[8]>, <3>}
//       {<6>, <3>, 1, <6>}
//       {1, <7>, 1}
//       {2}
//     }
//   }(3 + 2 + 2 + 2 + 2 + 2 + 2 + 0 + 0 + 0)(15)), B: ({1, 2, [3], [3], [4]}(10) + {1, -1, 1, 0, 0}(1) + ((2))), C: 15, D: 0
//   roll: [10, 11, 11, 12, 2, 2, 2, 2, 3, 4, 5, 5, 7, 7, 8]
// }(91) + (42)`
