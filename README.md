# 阅读好项目源代码查阅资料记录

### 获取手机系统可用空间大小
```objc
NSDictionary *attrs = [[NSFileManager defaultManager] attributesOfFileSystemForPath:NSHomeDirectory() error:&error];
int64_t space =  [[attrs objectForKey:NSFileSystemFreeSize] longLongValue];
```
### 该主题会一直持续更新，记录自己漫漫学习路~！


