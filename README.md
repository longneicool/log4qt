#### 使用方法
1. 在.pro文件中加入log4qt文件
```
include(../log4qt/src/log4qt/log4qt.pri)
```

2. 在main函数中添加
```
#include "log4qt/logmanager.h"
#include "log4qt/logger.h"
#include "log4qt/propertyconfigurator.h"
Log4Qt::PropertyConfigurator::configure(a.applicationDirPath() + "/log4qt.conf"); // 设置配置文件路径
Log4Qt::LogManager::setHandleQtMessages(true); // 设置log4qt输出qt自身的debug信息
```

3. 将配置文件`log4qt.conf`放入执行文件所在的文件夹
