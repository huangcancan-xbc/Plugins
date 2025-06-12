### 免费图床配置

在 Typora 中配置图床的简单稳定方法，推荐使用 **PicGo + GitHub（配合免费 CDN 加速）**。

**方案优势**

- **完全免费**（GitHub 存储 + jsDelivr CDN 加速）
- **稳定可靠**（GitHub 服务稳定，CDN 提升国内访问速度）
- **无缝集成**（Typora 直接调用 PicGo 上传）

| 平台       | 存储限制                    | 其他限制                               |
| :--------- | :-------------------------- | :------------------------------------- |
| **GitHub** | 单个仓库建议 ≤1GB           | 公开仓库免费，大文件需 Git LFS（收费） |
| **Gitee**  | 公开仓库 ≤5GB（需实名认证） | 未实名用户仓库 ≤500MB，有流量访问限制  |

这里可以看到 `gitee` 其实是有存储限制的，`gitee` 单个用户所有仓库总量为 `5GB`，`GitHub` 则没有提及总量，只要求单个仓库容量为 `1GB`。众所周知图片文件的大小一般比代码文件、其他文件要大，所以保险起见，推荐选择 `GitHub` 作为图床，这里还有 **免费的 CDN 加速**，不用担心卡顿，如果实在是网络限制，选择 `gitee` 也是不错之举。

---

#### 配置步骤

**1. 准备工作**

- 安装 [PicGo](https://github.com/Molunerfinn/PicGo/releases)（选择对应系统版本）

![](https://cdn.jsdelivr.net/gh/huangcancan-xbc/Drawing-bed@master/Typora/image-20250222172656601.png)

- 注册 GitHub 账号并新建一个 **公开仓库**（如命名 `image-bed`）

**2. 生成 GitHub Token**

1. 进入 GitHub → Settings → Developer settings → Personal access tokens → Fine-grained tokens → New GitHub App

![image-20250222173030617](https://cdn.jsdelivr.net/gh/huangcancan-xbc/Drawing-bed@master/Typora/image-20250222173030617.png)

![image-20250222173804223](https://cdn.jsdelivr.net/gh/huangcancan-xbc/Drawing-bed@master/Typora/image-20250222173804223.png)

2.   勾选读写权限，生成 Token 并 **复制保存**（**注意关闭页面后无法再次查看！！！**）。

![image-20250222174144327](https://cdn.jsdelivr.net/gh/huangcancan-xbc/Drawing-bed@master/Typora/image-20250222174144327.png)

![image-20250222174522501](https://cdn.jsdelivr.net/gh/huangcancan-xbc/Drawing-bed@master/Typora/image-20250222174522501.png)

**3. 配置 PicGo 的 GitHub 图床**

1. 打开 PicGo → 图床设置 → GitHub 图床
2. 填写以下信息：
   - **仓库名**：`你的GitHub用户名/仓库名`（如 `yourname/image-bed`）
   - **分支名**：`main` 或 `master`（根据仓库实际分支）
   - **Token**：粘贴刚生成的 Token
   - **存储路径**：可选（如 `images/`，图片会存储在仓库的该目录下），可随时修改
   
       -   如果直接是字符（`images`），则会直接上传图片至仓库根目录下（会显得凌乱，当然，不介意、图省事可选）
       -   如果是字符加 `/`（`images/`），则会上传图片至 `images/` 目录下（相较于上一种会有一点条理）
       -   **图片自定义命名：** 将此配置完成后，直接在 Typora 粘贴即可立即上传图片至图床，但是，图片名称通常是一串类似时间表示的数字。想要图片名称自定义，需要先将图片保存至本地进行重命名，再次放入 Typora 就会上传自定义名称的图片了。
   
       ![image-20250222180507950](https://cdn.jsdelivr.net/gh/huangcancan-xbc/Drawing-bed@master/Typora/image-20250222180507950.png)
   
   - **自定义域名**（用于加速）：`https://cdn.jsdelivr.net/gh/你的GitHub用户名/仓库名@分支`（注意 `@` 符号不要丢了！）
   
   ![image-20250222174920717](https://cdn.jsdelivr.net/gh/huangcancan-xbc/Drawing-bed@master/Typora/image-20250222174920717.png)

**4. Typora 配置**

1. 打开 Typora → 偏好设置 → 图像
2. 选择 **PicGo.app**，设置 PicGo 的安装路径。
3. 测试上传：拖拽图片到 Typora，若自动上传成功即配置完成。

此方案兼顾免费与稳定，适合长期使用。若需更详细教程，可参考 [PicGo 官方文档](https://picgo.github.io/PicGo-Doc/)。
