## Vi自学报告



### Vi/Vim的基本使用

vi/vim 共分为三种模式，分别是**命令模式（Command mode）**，**输入模式（Insert mode）**和**底线命令模式（Last line mode）**。 

1. 命令模式：
用户刚刚启动 vi/vim，便进入了命令模式。此状态下敲击键盘动作会被Vim识别为命令，而非输入字符。比如我们此时按下i，并不会输入一个字符，i被当作了一个命令。以下是常用的几个命令：
   - i 切换到输入模式，以输入字符。
   - x 删除当前光标所在处的字符。
   - : 切换到底线命令模式，以在最底一行输入命令。

> 若想要编辑文本：启动Vim，进入了命令模式，按下i，切换到输入模式。          
> 命令模式只有一些最基本的命令，因此仍要依靠底线命令模式输入更多命令。

2. 输入模式:
在命令模式下按下i就进入了输入模式。在输入模式中，可以使用以下按键：
   - 字符按键以及Shift组合，输入字符
   - ENTER，回车键，换行
   - BACK SPACE，退格键，删除光标前一个字符
   - DEL，删除键，删除光标后一个字符
   - 方向键，在文本中移动光标
   - HOME/END，移动光标到行首/行尾
   - Page Up/Page Down，上/下翻页
   - Insert，切换光标为输入/替换模式，光标将变成竖线/下划线
   - ESC，退出输入模式，切换到命令模式

3. 底线命令模式:
在命令模式下按下:（英文冒号）就进入了底线命令模式。底线命令模式可以输入单个或多个字符的命令，可用的命令非常多。在底线命令模式中，基本的命令有（已经省略了冒号）：
   - q 退出程序
   - w 保存文件

> 按ESC键可随时退出底线命令模式。

### Vi/Vim中模式的切换总结：

三个模式：命令模式、输入模式、底线命令模式

- 进入命令模式：使用vi filename 或vim filename
- 命令模式进入输入模式：输入i、a、o。
- 输入模式返回命令模式：ESC键
- 命令模式进入底线命令模式：输入“：”
- 底线命令模式返回命令模式：ESC键
- 退出命令模式：输入“：”进入底线命令模式，输入wq回车，保存并离开。

### 简单案例：

首先创建了一个vim_test.txt文件，然后使用vim编辑器进行编辑，输入i进入输入模式。

![1](img/1.png)

然后输入完后，esc加：进入底层命令模式，然后wq保存退出。

![2](img/2.png)

最后使用cat查看文件内容。

![3](img/3.png)