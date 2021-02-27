#  hexo-deployer-ali-oss-extend部署器使用说明

在hexo项目下执行安装命令：

```
    npm i hexo-deployer-ali-oss-extend
```

在hexo项目配置文件`_config.yml`中添加如下配置：

```
deploy:
- type: ali-oss
  region: <您的oss 区域代码>
  accessKeyId: <您的oss  accessKeyId>
  accessKeySecret: <您的oss accessKeySecret>
  bucket: <您的bucket name>
  cacheControl:
    images: <图片文件HTTP响应头Cache-Control>，留空为no-cache
    css: <CSS文件HTTP响应头Cache-Control>，留空为no-cache
    js: <JS文件HTTP响应头Cache-Control>，留空为no-cache
    html: <HTML文件HTTP响应头Cache-Control>，留空为no-cache
    other: <其它文件HTTP响应头Cache-Control>，留空为no-cache
  
```

就这么简单 然后执行部署命令：

```
hexo d
```

即可将项目部署到oss中 ，默认情况下，将文件上传到bucket的根目录下，如果需要部署到其他目录，请在deploy下添加remotePath选项进行指定

```
	remotePath:<您要部署的目录>
```

--------
修改自：https://github.com/wertycn/hexo-deployer-ali-oss


