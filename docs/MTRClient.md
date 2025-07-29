# MTR 客户端数据

MTR将数据存储在[ClientData.java](https://github.com/aphrodite281/Minecraft-Transit-Railway/blob/master/common/src/main/java/mtr/client/ClientData.java)中，因此您可以通过以下方法来访问列车，时刻表，车站，线路等数据。


## MTRClientData
`MTRClientData.DATA_CACHE:ClientCache`
-MTR客户端数据缓存，类型是`ClientCache`
`MTRClientData.SCHEDULES_FOR_PLATFORM:Map<Long, Set<ScheduleEntry>> `
-MTR的列车时刻表，可通过站台的id获取这个站台的所有时刻表
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
| `ClientCache.platformIdToStation:Map<Long, Station>`|通过站台id获取站台所在车站的Java Map|
| `ClientCache.sidingIdToDepot:Map<Long, Depot>`|通过侧线id获取侧线所在车厂的Java Map|
| `ClientCache.routeIdToOneDepot:Map<Long, Station>`|通过线路id获取线路的车厂的Java Map|
|`ClientCache.stationIdToConnectingStation:Map<Station, Set<Station>>`|通过车站获取它的所有连接车站的Java Map|
`requestStationIdToPlatforms(long stationId)：Map<Long, Platform>`
-通过车站的id请求车站所有的站台，返回一个Java Map。
`requestDepotIdToSidings(long depotId)：Map<Long, Siding>`
-通过车站的id请求车厂所有的侧线，返回一个Java Map。
`requestPlatformIdToRoutes(long platformId) :List<PlatformRouteDetails>`
-通过站台id获取站台的所有线路，注意返回的是List<PlatformRouteDetails>而不是List<Route>。
