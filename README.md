# SSJtoMeki_bot
work work
# 开发
## 如何接收消息
### 基于群的处理
如果你希望针对每个群来实现特定的功能，你可以在cqpy.cqgroups个目录新建.py文件，在文件里创建BaseGruop的子类。程序将会自动导入这个目录下的文件，并获取其中所有BaseGruop的子类。

class G114514(BaseGroup):

    def __init__(self):
    
        super().__init__()
        
        self.group_id = 114514


### 基于消息的处理
此功能还未完善

## 如何发送消息

### 发送群消息
获取Cqserver的实例，调用其中的sendGroup(self, group_id:str|int, msg:str)方法可发送消息。

在BaseGroup类中Cqserver的实例为self.server。

在部分Event中Cqserver的实例为self.s。
### 发送私聊消息
