# GamePro Free Shopify 模板使用教程

GamePro Free 是一个可免费使用和二次开发的 Shopify Online Store 2.0 英文主题。仓库只包含主题代码与无品牌演示素材，不包含任何店铺订单、顾客资料、密钥、真实商品数据或第三方应用配置。

## 一、安装前准备

- 一个 Shopify 店铺或开发店铺
- 可选：最新版 Shopify CLI，用于本地开发
- 自己拥有使用权的 Logo、商品图、文案和政策内容

## 二、通过 ZIP 安装

1. 在 GitHub 仓库页面点击 **Code > Download ZIP**。
2. 解压下载的文件。
3. 进入解压后的项目目录，选中其中的 `assets`、`config`、`layout`、`locales`、`sections`、`snippets`、`templates` 等内容，重新压缩为 ZIP。
4. 打开 Shopify 后台的 **Online Store > Themes**。
5. 点击 **Add theme > Upload ZIP file**，上传刚才重新压缩的文件。
6. 先使用 **Preview** 检查，不要直接发布。

ZIP 根目录必须直接包含 `layout/theme.liquid` 和 `config/settings_schema.json`。如果 ZIP 外面还包着一层仓库文件夹，Shopify 会提示缺少必需文件。

## 三、通过 Shopify CLI 预览

```bash
git clone https://github.com/WOOK98/gamepro-free-shopify-theme.git
cd gamepro-free-shopify-theme
shopify theme dev --store=your-store.myshopify.com
```

需要上传为未发布主题时运行：

```bash
shopify theme push --unpublished
```

## 四、建议配置顺序

### 1. 品牌与全局样式

在主题编辑器的 **Theme settings** 中设置 Logo、颜色、字体、按钮、社交链接和浏览器图标。演示主题默认使用英文，发布前请统一检查品牌名与联系方式。

### 2. 导航菜单

在 Shopify 后台的 **Content > Menus** 创建主菜单和页脚菜单，再到 Header 与 Footer 区段选择对应菜单。逐个点击检查 Home、Shop、Contact、Policies 等链接的语义和目标页面。

### 3. 首页 Hero

打开首页的 Hero 区段，替换背景图、标题、副标题和按钮链接。建议使用经过压缩的 WebP 或 AVIF 图片，并确保移动端主体不会被裁掉。

### 4. 连接真实商品

- 在 **Featured product** 中选择一个真实商品。
- 在 **Product grid** 中选择一个真实商品系列。
- 连接商品后关闭演示商品 fallback，避免访客看到占位内容。
- 确认商品已发布到 Online Store 销售渠道，并具有可售库存。

### 5. 商品页与购物流程

检查每个商品的标题、图片、价格、规格、库存、描述、配送信息和退货政策。测试规格切换、数量调整、Add to cart、购物车和 Checkout。

### 6. 页脚和政策

在 Shopify 后台创建并审核 Privacy Policy、Refund Policy、Terms of Service、Shipping Policy 和 Contact Information。模板不会替商家生成合法政策，演示文字不能直接用于正式经营。

### 7. 第三方应用

Shopify Inbox、Shop、评价、订阅弹窗等应用区块不会随开源主题自动安装。请在后台单独安装，并在移动端检查它们是否遮挡购买按钮或锁住页面滚动。

## 五、发布前测试

至少完成以下测试：

- 桌面、iPhone 和 Android 页面布局正常
- 菜单、搜索、账户、购物车和政策链接可用
- 商品图片清晰，规格切换会同步价格、库存和主图
- Add to cart、购物车数量修改和 Checkout 可完成
- 无重复折扣弹窗、聊天按钮遮挡或无法滚动的问题
- 页面没有商家隐私信息、测试邮箱、令牌或真实顾客数据
- 店铺默认语言和所有可见文案符合目标市场

## 六、常见问题

### Shopify 提示缺少主题必需文件

重新制作 ZIP，确保 `layout`、`config` 等目录位于压缩包根目录。

### 商品没有显示

确认商品处于 Active 状态、已发布到 Online Store、具有库存，并且首页区段已经选择正确的商品或系列。

### 菜单跳转错误

菜单链接来自 Shopify 后台，不是硬编码在主题中。请到 **Content > Menus** 修正链接。

### 应用按钮或聊天窗口异常

先在主题编辑器的 **App embeds** 中停用对应应用进行排查。应用本身的布局和关闭行为通常需要在应用后台配置。

## 七、更新与备份

修改主题前先复制当前线上主题。更新开源代码时先推送为未发布主题，在 Preview 中验证后再发布，避免覆盖线上自定义设置。
