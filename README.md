# GEGL_GIMP_PLUGIN_channelrangetoalpha

## English

### 1. Compile & Install Commands

#### Native Linux (System installed GIMP)

```bash
sh build_linux.sh
cp build/gegl-*.so ~/.local/share/gegl-0.4/plug-ins
```

#### Flatpak Linux (Flatpak GIMP)

```bash
sh build_linux.sh
cp build/gegl-*.so ~/.var/app/org.gimp.GIMP/data/gegl-0.4/plug-ins/
```

### 2. How to Open Plugin in GIMP

Restart GIMP after copying files.
Menu path: `Colors → myfilters → Channel Range To Alpha`
Short access: Press `/` in GIMP and search `channelrangetoalpha`.

---

## 中文

### 1. 编译与安装命令

#### Linux 原生版（系统包安装的GIMP）

```bash
sh build_linux.sh
cp build/gegl-*.so ~/.local/share/gegl-0.4/plug-ins
```

#### Linux Flatpak 容器版（应用商店Flatpak GIMP）

```bash
sh build_linux.sh
cp build/gegl-*.so ~/.var/app/org.gimp.GIMP/data/gegl-0.4/plug-ins/
```

### 2. GIMP 插件打开路径说明

复制文件完成后**重启GIMP**生效。
菜单路径：`颜色 → myfilters → Channel Range To Alpha`
快速调取：GIMP内按下 `/` 快捷键，搜索 `channelrangetoalpha` 直接打开滤镜。
