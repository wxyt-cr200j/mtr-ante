# MTR 客户端数据

MTR将数据存储在[ClientData.java](https://github.com/aphrodite281/Minecraft-Transit-Railway/blob/master/common/src/main/java/mtr/client/ClientData.java)中，因此您可以通过以下方法来访问列车，时刻表，车站，线路等数据。


## MTRClientData
`MTRClientData.DATA_CACHE:ClientCache`-MTR客户端数据缓存，类型是ClientCache


## 版本

提供了一些能用来获得版本号的函数，以便让作者能兼容不同版本的不同（如果有）。

| 函数                                         | 说明                                                         |
| -------------------------------------------- | ------------------------------------------------------------ |
| `static Resources.getMTRVersion(): String`   | MTR 的版本字符串，形如 `1.19.2-3.1.0-hotfix-1`               |
| `static Resources.getNTEVersion(): String`   | NTE 的版本字符串，形如 `0.4.0+1.19.2`                        |
| `static Resources.getNTEVersionInt(): int`   | NTE 的版本的数字形式，以便比较；例如 0.4.0 的是 4000，1.9.1 的会是 19100 |
| `static Resources.getNTEProtoVersion(): int` | NTE 的存档格式版本数字。                                     |


