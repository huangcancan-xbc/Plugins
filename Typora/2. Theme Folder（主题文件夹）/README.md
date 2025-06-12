# 使用：直接将此文件夹内容粘贴至Typora的主题文件夹下进行替换即可

⚠️ 注意：这里的GitHub我做了一点修改，具体如下：

# Typora 主题文件样式新增

如果你想修改 Typora 中行内代码的颜色和背景颜色，可以通过编辑 Typora 的 CSS 文件来实现。以下是我在 `github.css` 文件中做的修改，用于优化行内代码的显示效果，达到如下图所示的效果：

![内敛代码（行内代码）样式](https://cdn.jsdelivr.net/gh/huangcancan-xbc/Drawing-bed@master/Typora/%E5%86%85%E6%95%9B%E4%BB%A3%E7%A0%81%EF%BC%88%E8%A1%8C%E5%86%85%E4%BB%A3%E7%A0%81%EF%BC%89%E6%A0%B7%E5%BC%8F.png)

---

## 🛠️ 修改步骤

1. **打开 CSS 文件**  
   找到 Typora 的主题配置文件夹，或者直接通过 Typora 偏好设置打开主题文件夹。路径通常为：
   
    - **Windows**: `C:\Users\<YourUsername>\AppData\Roaming\Typora\themes\`
    - **macOS**: `~/Library/Application Support/Typora/themes/`
    - **Linux**: `~/.config/typora/themes/`
    
    进入后，找到并打开 `github.css` 文件（推荐使用 `vscode` 编辑器打开）。
   
2. **定位代码块样式**  
   使用 `CTRL+F` 在文件中查找以下代码段：
   
    ```css
    code {
        background-color: #f3f4f4;
        padding: 0 2px 0 2px;
    }
    ```
   
3. **修改颜色和背景颜色**  
   将该代码段修改为以下内容：
   
    ```css
    code {
        color: #C7254E; /* 设置行内代码的颜色 */
        background-color: #F9F2F4; /* 设置行内代码的背景颜色 */
        padding: 0 2px 0 2px; /* 保持原有的内边距 */
    }
    ```

4. **保存文件**  
   使用 `CTRL+S` 保存修改后的 `github.css` 文件。

5. **重启 Typora**  
   关闭并重新启动 Typora，即可看到新的行内代码样式生效。

---

## 🔧 修改后的效果

- **行内代码的字体颜色**：将变为 `#C7254E`（深红色）。
- **行内代码的背景颜色**：将变为 `#F9F2F4`（浅粉色）。

这样修改后，行内代码将更加美观，符合个人喜好。
