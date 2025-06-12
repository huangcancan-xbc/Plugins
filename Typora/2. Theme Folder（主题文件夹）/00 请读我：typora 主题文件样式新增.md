### typora 主题文件样式新增

要修改 Typora 中行内代码的颜色和背景颜色，你需要编辑 Typora 的 CSS 文件。这里我认为 `github.css` 文件的行内代码不好看，想要达到下面图片的效果，于是我做了以下修改：

![内敛代码（行内代码）样式](https://cdn.jsdelivr.net/gh/huangcancan-xbc/Drawing-bed@master/Typora/%E5%86%85%E6%95%9B%E4%BB%A3%E7%A0%81%EF%BC%88%E8%A1%8C%E5%86%85%E4%BB%A3%E7%A0%81%EF%BC%89%E6%A0%B7%E5%BC%8F.png)

### 修改步骤

1. **打开 CSS 文件**  
    找到 Typora 的主题配置文件夹（也可直接打开 Typora 的偏好设置 → 外观 → 打开主题文件夹），通常位于：
    
    - Windows: `C:\Users\<YourUsername>\AppData\Roaming\Typora\themes\`
      
    - macOS: `~/Library/Application Support/Typora/themes/`
      
    - Linux: `~/.config/typora/themes/`
      
    
    找到并打开 `github.css` 文件（推荐使用 vscode 进行打开）。
2. **定位代码块样式**  
    `CTRL+F` 在文件中找到以下代码块：
    
    ```css
    code {
        background-color: #f3f4f4;
        padding: 0 2px 0 2px;
    }
    ```
3. **修改颜色和背景颜色**  
    将其修改为：
    ```css
    code {
        color: #C7254E; /* 设置行内代码的颜色 */
        background-color: #F9F2F4; /* 设置行内代码的背景颜色 */
        padding: 0 2px 0 2px; /* 保持原有的内边距 */
    }
    ```
4. **保存文件**  
    `CTRL+S` 保存修改后的 `github.css` 文件。
5. **重启 Typora**  
    关闭并重新启动 Typora，就会应用新的样式。

### 修改后的效果

- 行内代码的字体颜色将变为 `#C7254E`（深红色）。
- 行内代码的背景颜色将变为 `#F9F2F4`（浅粉色）。