# codelab.club 主站

# 依赖
*  [hugo](http://www.gohugo.org/)
*  theme: [airspace-hugo](https://themes.gohugo.io/theme/airspace-hugo/)

# usage
[Hugo中文文档](http://www.gohugo.org/)
```
hugo new site hugo_demo_site
cd hugo_demo_site
cd themes
git clone https://github.com/themefisher/airspace-hugo
```

将themes/airspace-hugo/exampleSite的文件复制出来

### 结构
*  home
*  blog
+ -> events（work）
+ -> service
*  about
*  contact

### 新增内容
events -> 火星车活动
service -> 已有网站 / 公众号
    OUR SERVICES

# todo
二维码

### 写博客
hugo new blog/first.md

### 浏览
hugo server --theme=airspace-hugo --buildDrafts

### 发布
make push

### 一些资源图片(CC0 License)
*  [be-creative](https://www.pexels.com/photo/close-up-of-human-hand-256514/)

### blog
themes/airspace-hugo/layouts/_default/list.html 模版

使用more注释标签来写摘要

# 栏目
按照yc课程的建议，先start-up，把流程走通

外部连接

使用code clab 卡片式资源入口，带入最好的资源
    以兴趣分流
    *  code club入门课程
        *  cn
    *  makecode
    *  raspberry
    *  志愿者(页脚)
    *  入门,如何让一个人入门
        *  软件，硬件，后续
    *  活动
    *  about


# 提取图片到本地
自托管图片，避免云故障

ack -ho "http://wwj-fig-bed.just4fun.site/.*.png" > /tmp/codelab_blog_png_list.txt

取得图片列表保存下来

```
cd img
```

python3

```python
import subprocess
with open("/tmp/codelab_blog_png_list.txt") as png_url_list:
    urls = png_url_list.readlines()
for url in urls:
    cmd = f"wget {url}"
    # print(cmd)
    subprocess.call(cmd,shell=True)
```



<!--
keyword:

*  blocks
*  creative
*  code
*  game
*  fun
*  peer
*  play
*  passion
*  projects
*  share
*  Imagine
*  create

*  [be-creative](https://www.pexels.com/photo/close-up-of-human-hand-256514/)
*  [play](https://www.pexels.com/photo/depth-of-field-photography-of-p-l-a-y-wooden-letter-decors-on-top-of-beige-wooden-surface-591652/)
*  [peer](https://www.pexels.com/photo/four-toddler-forms-circle-photo-754769/)
*  [child fly](https://www.shutterstock.com/zh/image-photo/portrait-young-businessman-toy-paper-wings-309774686?src=XqATyjMPjKlw-y2P2gqvXw-1-56)
*  [fly](https://www.shutterstock.com/zh/image-photo/happy-child-playing-toy-wings-against-288233360?src=XqATyjMPjKlw-y2P2gqvXw-1-98)
*  [loading](https://www.shutterstock.com/zh/image-vector/design-progress-bar-loading-creativity-248974471?src=XqATyjMPjKlw-y2P2gqvXw-1-43)
*  [peer idea](https://www.shutterstock.com/zh/image-photo/multiethnic-group-people-planning-ideas-193983560?src=XqATyjMPjKlw-y2P2gqvXw-1-99)
*  [child fly](https://www.shutterstock.com/zh/image-photo/portrait-young-child-pretend-be-businessman-691797652?src=XqATyjMPjKlw-y2P2gqvXw-1-39)
*  [maker](https://www.shutterstock.com/search?searchterm=maker&search_source=base_search_form&language=zh&page=1&sort=popular&image_type=all&measurement=px&safe=true)
    *  [maker child](https://www.shutterstock.com/zh/image-photo/berlin-germany-december-2017-young-boy-1032734617?src=iwqCk_8b11qCT6theZ6Flw-1-86)
    *  [maker](https://www.shutterstock.com/zh/image-photo/particle-maker-kit-electronics-project-circuits-489321511?src=iwqCk_8b11qCT6theZ6Flw-1-98)
    *  [maker hand](https://www.shutterstock.com/zh/image-photo/hands-basket-maker-weave-wicker-1100057633?src=iwqCk_8b11qCT6theZ6Flw-1-60)
    *  [maker](https://www.shutterstock.com/zh/image-photo/handsome-joiner-work-carpentry-he-successful-578729953?src=iwqCk_8b11qCT6theZ6Flw-1-28)
    *  [child robot](https://www.shutterstock.com/zh/image-photo/children-creating-robots-school-stem-education-727168123?src=iwqCk_8b11qCT6theZ6Flw-1-7)
        *  https://www.shutterstock.com/zh/image-photo/children-creating-robots-school-stem-education-727168042?src=iwqCk_8b11qCT6theZ6Flw-1-4
        *  https://www.shutterstock.com/zh/image-photo/educational-weaving-knitting-activity-wool-kids-607875302?src=iwqCk_8b11qCT6theZ6Flw-1-0
    *  [maker tool](https://www.shutterstock.com/zh/image-photo/diy-electronic-maker-tools-components-on-489321508?src=iwqCk_8b11qCT6theZ6Flw-1-6)
*  [geek](https://www.shutterstock.com/zh/image-photo/happy-kid-playing-toy-robot-home-324288134?src=Yu0jBb2I8r1EmyokOfQIaw-1-97)
*  code
    *  https://www.shutterstock.com/zh/image-vector/binary-circuit-board-future-technology-green-1027513441?src=JdpM3lIkv3YWNBdsI5rFoQ-1-14
    *  https://www.shutterstock.com/zh/image-vector/computer-code-on-screen-blue-background-717444511?src=JdpM3lIkv3YWNBdsI5rFoQ-1-68
    *  https://www.shutterstock.com/zh/image-vector/modern-vector-illustration-concept-word-coding-603906611?src=JdpM3lIkv3YWNBdsI5rFoQ-1-91
    *  [coding future](https://www.shutterstock.com/zh/image-illustration/3d-illustration-color-bytes-binary-code-1081142213?src=JdpM3lIkv3YWNBdsI5rFoQ-1-10)

# open source logo
*  [openlogos](https://github.com/arasatasaygin/openlogos)
*  [Open Source Logo Vectors Free Download - seeklogo](https://seeklogo.com/free-vector-logos/animal?filter=template)
*  [logo](http://www.logodust.com/)

fire
    https://preview.freelogodesign.org/?lang=en&name=codelab.club&logo=1b4f6cf6-ac20-44d0-bba2-1401d4e37c47
    下载：http://preview.freelogodesign.org/?lang=EN&autodownload=true&logo=1b4f6cf6-ac20-44d0-bba2-1401d4e37c47
    ico: https://tbncdn.freelogodesign.org/efcda770-056b-4bc7-b94f-09cf8fa3ef17.png?1532515026459

potato
    https://preview.freelogodesign.org/?lang=EN&name=codelab.club&logo=6996ca75-2ed1-4104-94a3-c24ed6802b28
tomato
    
七巧板
或者某个几何集合图形

如何帮助用户！
-->