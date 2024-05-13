# vscode-mouseless
***Best vim experience in VS Code and programming like a pro***  

This settings doesn't change the default VS Code keyboard shortcuts much, it does not intend to make it become Neovim flavor.  

After you install the [vscodevim extension](https://marketplace.visualstudio.com/items?itemName=vscodevim.vim) and apply the settings. You will not experience any uncomfortable when typing, but have the ability to embrace the efficient VIM motions.  

***Be familair with VS Code keyboard shortcuts and VIM basics is a prequistion by the way***  

Launch VS code > Help > [Keyboard shortcuts Reference](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)  
And refer to [VIM cheatsheet](https://vim.rtorr.com/)

## 1. Download .vscodevimrc file into your $HOME folder
The purpuse of this file it's to make the copy / cut naturally in VIM performing like the nomral operation system does.(VIM unique clipboard matters)
## 2. Remap the CapsLock key to Ctrl key
For windows users, It's easy to achive this by [AutoHotkey](https://www.autohotkey.com/).
- Create new AutoHotkey Script
  ```
  *CapsLock::Ctrl
  ```
- May consider to put the script into your system startup folder, then it will automactically run with your windows boots.
## 3. Keybindings customized
### 3.1 VIM keybindings in ***settings.json***
Insert mode keybindings  
| modifier | key  | description |
| -------- | ---- | ----------- |
|          | jj   | Esc         |
| ctrl     | h    | Left        |
| ctrl     | l    | Right       |
| ctrl     | j    | Down        |
| ctrl     | k    | Up          |
| ctrl     | m    | Backspace   |

  
Normal mode keybindings  
| modifier   | key  | description              |
| ---------- | ---- | ------------------------ |
|            | tab  | Next tab 切换到下一个标签         |
| shift      | tab  | Previous tab 切换到上一个标签         |
| leader     | m    | Mark Bookmarks当前位置打上书签         |
| leader     | b    | Bookmark lists查看全部书签             |
|            | g d  | Got to definition跳到定义处               |
|            | g h  | Show detail 显示详情                 |
| shift      | k    | Show detail 显示详情                 |
| shift      | j    | Merge the next line 合并下面行               |
| shift      | h    | Move cursor to screen top 光标向上移动满屏         |
| shift      | l    | Move cursor to screen bottom 光标向下移动满屏         |
| ctrl       | j    | easy motion 垂直向下搜索 |
| ctrl       | k    | easy motion 垂直向上搜索 |
| leader     | s    | easy motion 搜索         |
| leader     | n    | Erase search highlight 清除搜索高亮             |
| leader     | p    | Format file 格式化文件               |
| leader     | w    | Save file 保存文件                 |
| leader     | x    | Close file 关闭当前文件             |
| leader     | q    | Close VS Code 关闭VS code              |
| ctrl       | \    | Vertical Split 垂直拆分窗口             |
| ctrl+alt   | \    | Horizontal Split 水平拆分窗口             |
|leader|h,j,k,l|navigate to left, right, up, down of split windows 聚焦拆分窗口|
| leader     | i    | toggle true/false        |
| leader     | c a  | toggle code action       |
| ctrl       | .    | toggle code action       |
| [          | d    | previous code problem      |
| ]          | d    | next code problem      |
| z          | a    | fold code 折叠代码                 |
| ctrl shift | \    | match bracket 括号匹配                 |

  Visual mode keybindings  
  | modifier | key  | des      |
| -------- | ---- | -------- |
|          | >    | 向右缩进 |
|          | <    | 向左缩进 |

  Vim-surround  
| Surround command             | Description                                              |
| ---------------------------- | -------------------------------------------------------- |
| y s （motion） （desired）   | Add desired surround around text defined by <motion>     |
| d s （existing）             | Delete existing surround                                 |
| c s （existing） （desired） | Change existing surround to desired                      |
| S （desired）                | Surround when in visual modes (surrounds full selection) |

  vim-easymotion  
| Motion command | Description             |
| -------------- | ----------------------- |
| leader + s     | Search character        |
| Ctrl + j       | Start of line forwards  |
| Ctrl+  k       | Start of line backwards |

  vim-sneak  
| Motion command                | Description                                                  |
| ----------------------------- | ------------------------------------------------------------ |
| s （char）（char）            | Move forward to the first occurrence of `<char><char>`       |
| S （char）（char）            | Move backward to the first occurrence of `<char><char>`      |
| （operator）z（char）（char） | Perform `<operator>` forward to the first occurrence of `<char><char>` |
| （operator）Z（char）（char） | Perform `<operator>` backward to the first occurrence of `<char><char>` |

  ### 3.2 VS Code keybindings customization in ***keybindings.json***
  | Description                  | modifier  | key        |
| ---------------------------- | --------- | ---------- |
| 将光标移动到行尾             | ctrl      | u          |
| 将光标移动到行首             | ctrl      | y          |
| 选择下一个                   | ctrl      | j          |
| 选择前一个                   | ctrl      | k          |
| 在上面插入空行               | shift     | enter      |
| 在下面插入空行               | ctrl      | enter      |
| 调出终端窗口(terminal pane)  | ctrl      | ;          |
| 调出错误列表(problem pane)   | ctrl      | '          |
| 在文件树和编辑器之间切换焦点 | ctrl      | e          |
| 在文件树 折叠文件夹          |           | h          |
| 在文件树 向下移动            |           | j          |
| 在文件树 向上移动            |           | k          |
| 在文件树 选择文件打开        |           | l or enter |
| 在文件树 在编辑器显示文件    |           | o          |
| 在文件树 重命名文件          |           | r          |
| 在文件树 新建文件            |           | a          |
| 在文件树 新建文件夹          | shift     | a          |
| 在文件树 删除                |           | d          |
| 在文件树 剪切                |           | x          |
| 在文件树 粘贴                |           | y or p     |
|                              |           |            |
| 输入状态下 隐藏提示框        | ctrl      | c          |
| 显示 code action             | ctrl      | .          |
| 将整行往下移                 | alt       | j          |
| 将整行往上移                 | alt       | k          |
| 将整行 复制 往下移           | shift alt | j          |
| 将整行 复制 往上移           | shift alt | k          |
|                              |           |            |
| project manager list         | ctrl      | n          |
| expand region                | ctrl      | w          |
| when terminal focus          |           |            |
| create new terminal          | ctrl      | n          |
| focus next terminal          | ctrl      | a          |
| focus previous terminal      | ctrl      | b          |
| close current terminal       | ctrl      | w          |
| split terminal               | ctrl      | \          |
| navigate to left terminal    | ctrl      | h          |
| navigate to right terminal   | ctrl      | l          |

  ## 4. Useful VS Code shortcuts
  | command                    | key            |
| -------------------------- | -------------- |
| Delete line                | ctrl+shift+K   |
| Cut line (empty selection) | ctrl+X         |
| Jump to matching bracket   | ctrl+shift+\   |
| toggle word wrap           | alt+Z          |
| Format document            | shift+alt+F    |
| delete a word              | ctrl+BackSpace |
| Go back/forward            | alt+Left/Right |
| Vertical split             | ctrl+\         |
| Horizontal split           | ctrl+alt+\     |
