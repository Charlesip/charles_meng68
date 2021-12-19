# charles_meng68

*A short description of the keyboard/project*

- Keyboard Maintainer: [charles](https://github.com/charlesip)
- Github主页：https://github.com/Charlesip/charles_meng68_4key

可以使用compile（推荐）或make命令编译固件（需要具备qmk环境）

```
qmk compile -kb charles_meng68 -km via
```

```
make charles_meng68:default
```

## Bootloader

有2种进入Bootloader的方式：

* **Bootmagic reset**：按住位于矩阵 (0,0) 处的按键 （通常是最左上方的按键或Esc）然后插上数据线，键盘将进入dfu模式，可以在qmk toolbox中看见设备连接提示
* **物理重置按键**：短接位于空格下的reset触点
