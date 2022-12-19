针对普通用户提示用户名不在sudoers文件中，此事将被报告，如此解决：


解决办法：

1.  终端输入 `su` 回车，输入 root 密码，回车，切换到 root 用户
2.  打开 sudoers 文件：`vi /etc/sudoers`
3.  找到 `# Allow members of group sudo to execute any command`，在 `%sudo ALL=(ALL:ALL) ALL` 下面添加 `xxx ALL=(ALL:ALL) ALL`，xxx 为前面无法执行 sudo 命令的用户名

vi 给 sudoers 添加内容方法：

1.  光标移动到指定位置，按 `i` 键当前光标位置插入
2.  输入内容
3.  `ESC`
4.  输入 `:wq!` 回车，因为 sudoers 是只读文件，所以要加 `!` 强制保存。