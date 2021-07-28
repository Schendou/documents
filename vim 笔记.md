##### Normal 模式
- i → insert模式，按ESC回到Normal模式
- x → 删除当前光标所在的一个字符
- :wq → 存盘 + 退出 (:w 存盘, :q 退出)   （陈皓注：:w 后可以跟文件名）
- dd → 删除当前行，并把删除的行存到剪贴板里
- p → 粘贴剪贴板
- hjkl (强例推荐使用其移动光标，但不必需) →你也可以使用光标键 (←↓↑→). 注: j 就像下箭头。
- :help <command> → 显示相关命令的帮助。你也可以就输入 :help 而不跟命令。（陈皓注：退出帮助需要输入:q）

##### (进入)写入模式
- a → 在光标后插入
- o → 在当前行后插入一个新行
- O → 在当前行前插入一个新行
- cw → 替换从光标所在位置后到一个单词结尾的字符

##### 移动光标
- 0 → 数字零，到行头
- ^ → 到本行第一个不是blank字符的位置（所谓blank字符就是空格，tab，换行，回车等）
- $ → 到本行行尾
- g_ → 到本行最后一个不是blank字符的位置。
- /pattern → 搜索 pattern 的字符串（陈皓注：如果搜索出多个匹配，可按n键到下一个）

##### 拷贝/粘贴
- P → 粘贴在当前位置之前
- p → 粘贴在当前位置之后
- yy → 拷贝当前行当行于 ddP

##### Undo/Redo
- u → undo
- <C-r> → redo

##### 打开/保存/退出/改变文件(Buffer)
- :e <path/to/file> → 打开一个文件
- :w → 存盘
- :saveas <path/to/file> → 另存为 <path/to/file>
- :x， ZZ 或 :wq → 保存并退出 (:x 表示仅在需要时保存，ZZ不需要输入冒号并回车)
- :q! → 退出不保存 :qa! 强行退出所有的正在编辑的文件，就算别的文件有更改。
- :bn 和 :bp → 你可以同时打开很多文件，使用这两个命令来切换下一个或上一个文件。（我喜欢使用:n到下一个文件）


- . → (小数点) 可以重复上一次的命令
- N<command> → 重复某个命令N次
下面是一个示例，找开一个文件你可以试试下面的命令：

- 2dd → 删除2行
- 3p → 粘贴文本3次
100idesu [ESC] → 会写下 “desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu “
- . → 重复上一个命令—— 100 “desu “.
- 3. → 重复 3 次 “desu” (注意：不是 300，你看，VIM多聪明啊).

你要让你的光标移动更有效率，你一定要了解下面的这些命令，千万别跳过。

- NG → 到第 N 行 （陈皓注：注意命令中的G是大写的，另我一般使用 : N 到第N行，如 :137 到第137行）（也可以使用Ngg）
- gg → 到第一行。（陈皓注：相当于1G，或 :1）
- G → 到最后一行。
- 按单词移动：
- w → 到下一个单词的开头。
- e → 到下一个单词的结尾。

