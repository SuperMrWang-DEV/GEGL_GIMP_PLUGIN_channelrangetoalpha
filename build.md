# 1. 安装编译依赖（Debian/Ubuntu）

sudo apt update
sudo apt install -y meson ninja-build libgegl-dev

# 2. 进入源码目录（请根据实际路径修改）

cd ~/Documents/code/GEGL-GIMP-PLUGIN_Outline_Deluxe-main

# 3. 批量编译所有插件

for plugin in SourceCode/\*/; do
echo "Building $plugin"
    cd "$plugin"
meson setup --buildtype=release build
ninja -C build
cd - > /dev/null
done

# 4. 创建 Flatpak GIMP 的 GEGL 插件目录并复制 .so 文件

mkdir -p ~/.var/app/org.gimp.GIMP/data/gegl-0.4/plug-ins
find SourceCode -name "\*.so" -exec cp {} ~/.var/app/org.gimp.GIMP/data/gegl-0.4/plug-ins/ \;

# 5. 验证安装

ls ~/.var/app/org.gimp.GIMP/data/gegl-0.4/plug-ins/\*.so

# 6. 重启 GIMP 后使用

# 菜单路径：GIMP 2.10 → 滤镜 → GEGL 操作 → "Outline Deluxe"

# GIMP 2.99.16+ → 滤镜 → 文本样式 → Outline Deluxe

#

meson setup --buildtype=release build

ninja -C build
