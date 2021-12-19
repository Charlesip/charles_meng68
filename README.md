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

* **Bootmagic reset**： 按住位于矩阵 (0,0) 处的按键 （通常是最左上方的按键或Esc）然后插上数据线，键盘将进入dfu模式，可以在qmk toolbox中看见设备连接提示
* **物理重置按键**: 短接位于空格下的reset触点

## Matrix

```
#define MATRIX_ROW_PINS { B3, B1, F0, F4, F1 }
#define MATRIX_COL_PINS { B2, D0, D1, D2, F7, F6, F5, D4, D6, D7, B4, B5, B6, C6, C7 }
```

![charles_meng68_matrix](https://imgur.com/NuNUX67)

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

