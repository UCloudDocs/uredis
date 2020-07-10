## 数据分片管理

分布式Redis（高性能版）实例可以通过控制台详情-分片管理来管理集群的各个分片，可以查看集群实例的各个分片使用情况并进行单个分片管理监控，分片管理入口：
![image](/images/udredis202006001.png)

#### 分片升降级

分布式Redis（高性能版）实例支持对单个分片进行配置升降级设置；如需对某一个分片进行升降级容量，可以选定该分片的操作项进行单个分片升降级：
![image](/images/udredis202006002.png)

注：在实际生产环境中，由于单个分片一旦内存使用量已满将会导致部分数据无法写入，因此，即使整个集群内存容量足够，但如果出现某个分片负载较高或内存使用率较高时，需要对该分片进行扩容操作。另外，建议用户使用中尽量使各个分片负载比较均衡，避免出现某个分片非常空闲造成资源浪费、而另外某个分片则负载严重。

#### 分片监控管理
通过单个分片各自监控信息，可以掌握各个分片的负载情况，并根据需要有针对性对具体分片进行升级扩容等管理：
![image](/images/udredis202006003.png)
另外，单个分片默认接入“默认云内存存储告警模板”，当内存使用率达到告警模板中设置的阈值时，触发告警机制。