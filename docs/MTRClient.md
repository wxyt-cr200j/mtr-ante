# MTR 客户端数据

MTR将数据存储在[ClientData.java](https://github.com/aphrodite281/Minecraft-Transit-Railway/blob/master/common/src/main/java/mtr/client/ClientData.java)中，因此您可以通过以下方法来访问列车，时刻表，车站，线路等数据。


## MTRClientData
`MTRClientData.DATA_CACHE:ClientCache`
-MTR客户端数据缓存，类型是`ClientCache`
`MTRClientData.SCHEDULES_FOR_PLATFORM:Map<Long, Set<ScheduleEntry>> `
-MTR的列车时刻表
`MTRClientData.RAILS:Map<BlockPos, Map<BlockPos, Rail>>`
-MTR的轨道数据

## ClientCache

提供了一些能用于获取单个数据以及对数据操作的方法，更高阶的，详见[ClientCache.java](https://github.com/aphrodite281/Minecraft-Transit-Railway/blob/master/common/src/main/java/mtr/client/ClientCache.java)。

| 方法                                         | 说明                                                         |
| -------------------------------------------- | ------------------------------------------------------------ |
| `ClientCache.stationIdMap:Map<Long, Station> ` |通过车站id获取MTR的车站数据的Java Map |
| `ClientCache.routeIdMap:Map<Long, Route> ` |通过线路id获取MTR的线路数据的Java Map |
| `ClientCache.platformIdMap:Map<Long, Platform> ` |通过站台id获取MTR的站台数据的Java Map |
| `ClientCache.sidingIdMap:Map<Long, Siding> ` |通过侧线id获取MTR的侧线数据的Java Map |
| `ClientCache.depotIdMap:Map<Long, Depot> ` |通过车厂id获取MTR的车厂数据的Java Map |


