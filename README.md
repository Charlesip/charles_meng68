# charles_meng68

*A short description of the keyboard/project*

meng68是运行[QMK固件](https://qmk.fm/)的开源键盘，支持VIA图形化界面修改键码

- Keyboard Maintainer: [charles](https://github.com/charlesip)
- Github主页：https://github.com/Charlesip/charles_meng68

键盘固件（[charles_meng68_via.hex](https://github.com/Charlesip/charles_meng68/blob/main/charles_meng68_via.hex)）已提供，需要键盘进入Bootloader模式，使用[QMK Toolbox](https://github.com/qmk/qmk_toolbox)刷入。

注意，键盘进入Bootloader之后，QMK Toolbox会提示如下字符（黄色），此时Flash按钮亮起，方可刷入：

```
*** Atmel DFU device connected (libusb0): Atmel Corp. ATmega32U4 (03EB:2FF4:0000)
```

 关于QMK Toolbox使用的一切问题请参考[官方文档](https://docs.qmk.fm/#/newbs_flashing)

## Bootloader

有2种进入Bootloader的方式（请注意，进入后将会清除via配置）：

* **Bootmagic reset**： 按住位于矩阵 (0,0) 处的按键 （meng68最左上方的按键）然后插上数据线。
* **物理重置按键**：短接位于空格下的reset触点，对于刚焊接好没有固件的键盘，Bootmagic reset将不起作用，必须使用此方式。

下图为刷机过程速览，供参考

![download](https://i.imgur.com/7hsLNDU.gif)



# 高阶用户

对于希望自己编译的用户，本项目亦提供[固件源码](https://github.com/Charlesip/charles_meng68/tree/main/charles_meng68)，可以使用compile（推荐）或make命令编译固件

```
qmk compile -kb charles_meng68 -km via
```

```
make charles_meng68:default
```

## Matrix

```
#define MATRIX_ROW_PINS { B3, B1, F0, F4, F1 }
#define MATRIX_COL_PINS { B2, D0, D1, D2, F7, F6, F5, D4, D6, D7, B4, B5, B6, C6, C7 }
```

![charles_meng68_matrix](https://i.imgur.com/NuNUX67.png)

```
/* This is a shortcut to help you visually see your layout.
 *
 * The first section contains all of the arguments representing the physical
 * layout of the board and position of the keys.
 *
 * The second converts the arguments into a two-dimensional array which
 * represents the switch matrix.
 */
#define LAYOUT( \
	K000, K001, K002, K003, K004, K005, K006, K007, K008, K009, K010, K011, K012, K013, K014, \
	K100, K101, K102, K103, K104, K105, K106, K107, K108, K109, K110, K111, K112, K113, K114, \
	K200, K201, K202, K203, K204, K205, K206, K207, K208, K209, K210, K211,       K213, K214, \
	K300, K301, K302, K303, K304, K305, K306, K307, K308, K309, K310,       K312, K313, K314, \
	K400, K401, K402,             K405,                   K409, K410,       K412, K413, K414  \
) { \
	{ K000,  K001,  K002,  K003,  K004,  K005,  K006,  K007,  K008,  K009,  K010,  K011,  K012,  K013,  K014 }, \
	{ K100,  K101,  K102,  K103,  K104,  K105,  K106,  K107,  K108,  K109,  K110,  K111,  K112,  K113,  K114 }, \
	{ K200,  K201,  K202,  K203,  K204,  K205,  K206,  K207,  K208,  K209,  K210,  K211,  KC_NO, K213,  K214 }, \
	{ K300,  K301,  K302,  K303,  K304,  K305,  K306,  K307,  K308,  K309,  K310,  KC_NO, K312,  K313,  K314 }, \
	{ K400,  K401,  K402,  KC_NO, KC_NO, K405,  KC_NO, KC_NO, KC_NO, K409,  K410,  KC_NO, K412,  K413,  K414 }  \
}
```

