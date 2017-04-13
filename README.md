# 阅读好项目源代码查阅资料记录

### 获取手机系统可用空间大小
```objc
NSDictionary *attrs = [[NSFileManager defaultManager] attributesOfFileSystemForPath:NSHomeDirectory() error:&error];
int64_t space =  [[attrs objectForKey:NSFileSystemFreeSize] longLongValue];
```
### OC重载函数(方法名一样，参数不一样时候可用重载函数达到目的)
```objc
static inline __attribute__((overloadable)) int  Foo(int a , int b) {
    return a + b;
}
static inline __attribute__((overloadable)) int  Foo(int b){
    return Foo(0,b);
}

@interface ViewController ()  
  
@end  
  
NSString * __attribute__((overloadable)) sark(NSString *x) {return @"nsstring";}  
NSString * __attribute__((overloadable)) sark(NSNumber *x) {return @"nsnumber";}  
NSString * __attribute__((overloadable)) sark(NSDictionary *x) {return @"nsdictionary";}  
NSString * __attribute__((overloadable)) sark(int x) { return @"int"; }  
NSString * __attribute__((overloadable)) sark(double x) { return @"double"; }  
NSString * __attribute__((overloadable)) sark(long x) { return @"long"; }  
  
@implementation ViewController  
  
- (void)viewDidLoad {  
    [super viewDidLoad];  
    NSLog(@"%@", sark(133333333));   
}  
@end  
```
### 该主题会一直持续更新，记录自己漫漫学习路~！


