# Prepare a CICD Environment

1. 在github上新建一个项目，将删改后的web项目push上去
2. 注册DaoCloud账号，进入控制台，创建项目，设置代码源为刚刚创建的github项目[repo](https://github.com/changeyoung98/demo-for-cicd)
![dao-set](requirement-1/dao-set.jpg)
3. 设置完成后点进本项目的“流程定义”对测试、构建等进行定义。

   - 测试阶段中无需进行其他安装任务，只需设置基础镜像。我们的image构建的基础镜像是Ubuntu 16.04
   - 构建阶段中，我们选择本地Dockerfile。在github的项目根目录中添加项目运行所需要的java安装文件夹和tomcat安装文件夹。创建一个Dockerfile，并在Dockerfile中配置好jre和tomcat的环境。在FROM处选择maven镜像。然后设置RUN 命令来构建项目并把生成的war包放进tomcat的对应位置。（详细见[Dockerfile](https://github.com/changeyoung98/demo-for-cicd/Dockerfile)代码）

4. 配置完成后即可在执行记录中看到自动的构建。构建成功后会在镜像仓库中看到生成的镜像文件。设置镜像的属性为公开即可拉取运行。