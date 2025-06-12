# 推荐设置

![](https://github.com/huangcancan-xbc/Drawing-bed/blob/master/Typora/Typora%E6%96%87%E4%BB%B6%E8%AE%BE%E7%BD%AE20250226225417188.png?raw=true)

![image-20250222195824150](https://cdn.jsdelivr.net/gh/huangcancan-xbc/Drawing-bed@master/Typora/image-20250222195824150.png)  

![image-20250226225639349](https://cdn.jsdelivr.net/gh/huangcancan-xbc/Drawing-bed@master/Typora/20250226225639465.png)

![image-20250222195934213](https://cdn.jsdelivr.net/gh/huangcancan-xbc/Drawing-bed@master/Typora/image-20250222195934213.png)

![image-20250222200024785](https://cdn.jsdelivr.net/gh/huangcancan-xbc/Drawing-bed@master/Typora/image-20250222200024785.png)

# 图片变白了，怎么办？

以下是一些建议步骤：

## 1. **备份文件**

- 在删除之前，建议先备份 `IconCache.db` 文件，以防万一需要恢复。
- 将文件复制到其他位置（如桌面或外部存储设备）。

## 2. **删除文件**

- 按下 `Win + R`，输入 `%localappdata%`，然后按回车。
- 找到 `IconCache.db` 文件，右键点击并选择“删除”。

## 3. **重启资源管理器**

- 按下 `Ctrl + Shift + Esc` 打开任务管理器。
- 找到“Windows 资源管理器”进程，右键点击并选择“重新启动”。

## 4. **重启电脑**

- 如果上述步骤无效，尝试重启电脑。Windows 会在启动时自动重建图标缓存。

## 5. **检查图标显示**

- 删除文件后，系统会重新生成图标缓存。如果图标仍然显示异常，可以尝试以下方法：

    - **清理图标缓存**：在命令提示符中运行以下命令：
      
      ```cmd
      ie4uinit.exe -show
      ```

    - **更新显卡驱动**：确保显卡驱动程序是最新的。

    - **检查系统更新**：确保 Windows 系统已更新到最新版本。

## 注意事项

- 删除 `IconCache.db` 文件不会影响系统正常运行，但可能会导致图标显示暂时异常。
- 如果问题仍然存在，建议联系技术支持或查阅相关论坛获取更多帮助。

---

## 其他方案：

### 1. **重建图标缓存（优先推荐）**

- 新建文本文档，输入以下内容：

    ```bat
    taskkill /f /im explorer.exe
    attrib -h -s -r "%localappdata%\IconCache.db"
    del /f "%localappdata%\IconCache.db"
    start explorer.exe
    ```

- 保存为 `修复图标.bat`，右键选择「以管理员身份运行」

- 完成后重启资源管理器（或直接重启电脑）

### 2. **检查 Typora 启动参数**

- 右键任务栏空白处 → 任务管理器 → 结束 Typora 进程
- 右键 Typora 快捷方式 → 属性 → 在「目标」路径末尾追加：  
  ` --disable-gpu-sandbox`（注意前面有空格）
- 应用后重新启动 Typora

### 3. **系统文件修复**

- 按下 `Win + S` 搜索「cmd」，然后右键选择「以管理员身份运行」
- 依次执行以下命令：

    ```cmd
    sfc /scannow
    DISM /Online /Cleanup-Image /RestoreHealth
    ```

- 完成后重启系统

### 4. **软件修复方案**

- 打开 Typora → 文件 → 偏好设置 → 通用 → 高级设置
- 打开 `conf.user.json` 文件
- 在 JSON 中添加配置：

    ```json
    "flags": [["disable-gpu-sandbox"]]
    ```

- 保存后完全退出程序并重新启动 Typora

### 5. **终极解决方案**

若上述方法无效，请按顺序尝试：

1. 完全卸载 Typora（建议使用 Geek Uninstaller）
2. 手动删除残留文件：
    - `C:\Users\<用户名>\AppData\Roaming\Typora`
    - `C:\Users\<用户名>\AppData\Local\Typora`
3. 从官网下载最新版本并安装
4. 安装时勾选「创建桌面快捷方式」
5. 安装后右键固定到任务栏

---

## 其他注意事项：

- 若使用 Windows 11 Dev 开发版，建议关闭「小组件」功能测试。
- 双显卡用户可在 NVIDIA 控制面板中为 Typora 指定独立显卡。
- 系统缩放比例设置为 125% 时可能出现异常，可尝试调整为 100% 或 150%。

如果问题仍未解决，可能是系统主题服务异常，您可以尝试以下操作：

1. 按下 `Win + R` 输入 `services.msc`
2. 找到「Themes」服务 → 右键重新启动
3. 检查「Windows Audio」服务是否正常运行
