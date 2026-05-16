# HPCKit社区组织管理

## 1. 创建SIG组
新建SIG需要向技术指导委员会提交新建SIG申请，议题经技术指导委员会审批通过后，SIG发起人需要完成SIG各类权限配置。

### 1.1 如何向技术委员会提交新建SIG申请
#### 确认SIG符合申请条件
申请之前请确保该SIG符合[SIG治理章程](../governance/sig-governance.md)。

#### 提交申请
向技术委员会（TSC）提交新建SIG申请，需要在技术委员会（TSC）例会申报议题，申报议题方式有两种：
1. 订阅[技术委员会邮箱]()，收到例会通知后，直接回复会议邮件，申报会议议题（例：`1. XXX SIG新建申请 -- 申请人：XXX`）。
2. 直接在技术委员会（TSC）[会议纪要模板]()进行申报，将相关议题和申报人员信息等刷新到对应例会议题中（例：`1. XXX SIG新建申请 -- 申请人：XXX`）。

### 1.2 权限配置
#### SIG代码仓管理权限
 SIG 发起人需修改 Kunpeng/HPCKit-Community 仓库, 配置maintainer, committer名单。

（1）在 sig 目录下创建新的 SIG 组目录；
创建信息文件：在该目录中创建 sig-info.yaml 文件([SIG配置编写指南](../sig/sig-info-guidance.md))，并配置 maintainers、committers 等信息；

（2）提交 PR：提交 PR 至 main 分支（PR描述中需要附加评审纪要）；

（3）✅通过审查并合入pr：此 PR 需获得 hpckit-cla/yes, lgtm, approved 三个标签后自动合入：
- `hpckit-cla/yes`：**CLA协议检查**。机器人会自动检查您 commits 中的邮箱是否已签署 CLA 协议。若已签署，将添加此标签；若未签署，会添加 `hpckit-cla/no` 标签并留言提示；
- `lgtm`：请联系 `governance/TSC/README.md` 文件中列出的 **tsc_members** 进行评审。评审通过后，tsc_member 评论 `/lgtm`，机器人会自动添加标签；
- `approved`：同样联系 **tsc_members** 进行批准。批准后，由tsc_members评论 `/approve`，机器人会自动添加标签。

（4）PR合入后，您需要登录[社区会议平台](https://meeting.hpckit.osinfra.cn)的个人中心将AtomGit账号与华为账号绑定，绑定AtomGit ID后，HPCKit社区SIG maintainer、committer自动拥有创建会议权限。具体会议指导详见[会议指南](https://atomgit.com/kunpengcompute/Infra/blob/main/docs/meeting/meeting.md)。
+ 注意：<font color="red">权限每隔1小时刷新一次，配置后请耐心等待</font>

（5）PR合入后，如果该SIG组需要新建邮件列表，需要maintainer在新建sig提交的PR中[@weixin_43493709](https://atomgit.com/weixin_43493709)，并描述："你好，需要新建邮件列表，邮件列表名为xxx@hpckit.osinfra.cn"（其中xxx代表sig名）。


## 2. SIG组变更(任免 maintainer committer)
### 2.1 变更流程
任免 maintainer committer流程详见[SIG治理章程](../governance/sig-governance.md)。

### 2.2 权限配置
1.  Fork 并修改：Fork `Kunpeng/HPCKit-Community` 仓库到您的个人账号，修改对应SIG组目录中 `sig-info.yaml` （[SIG配置编写指南](../sig/sig-info-guidance.md)）里面的人员信息。；
2.  提交 PR：向 `Kunpeng/HPCKit-Community` 仓库的 `main` 分支提交 PR（PR描述中需要附加评审纪要）；
3.  ✅  通过审查并合入pr：您的 PR 需要获得以下三个标签才能被合并：

    - `hpckit-cla/yes`：**CLA协议检查**。机器人会自动检查您 commits 中的邮箱是否已签署 CLA 协议。若已签署，将添加此标签；若未签署，会添加 `hpckit-cla/no` 标签并留言提示；
    - `lgtm`：请联系 `governance/TSC/README.md` 文件中列出的 **tsc_members** 进行评审。评审通过后，tsc_member 评论 `/lgtm`，机器人会自动添加标签；
    - `approved`：同样联系 **tsc_members** 进行批准。批准后，由tsc_members评论 `/approve`，机器人会自动添加标签。


## 3. SIG组终止
### 3.1 变更流程
终止SIG流程详见[SIG治理章程](../governance/sig-governance.md)。

### 3.2 权限配置
1.  Fork 并修改：Fork `Kunpeng/HPCKit-Community` 仓库到您的个人账号，删除 sig 目录下对应SIG组目录；
2.  提交 PR：向 `Kunpeng/HPCKit-Community` 仓库的 `main` 分支提交 PR（PR描述中需要附加评审纪要）；
3.  ✅  通过审查并合入pr：您的 PR 需要获得以下三个标签才能被合并：

    - `hpckit-cla/yes`：**CLA协议检查**。机器人会自动检查您 commits 中的邮箱是否已签署 CLA 协议。若已签署，将添加此标签；若未签署，会添加 `hpckit-cla/no` 标签并留言提示；
    - `lgtm`：请联系 `governance/TSC/README.md` 文件中列出的 **tsc_members** 进行评审。评审通过后，tsc_member 评论 `/lgtm`，机器人会自动添加标签；
    - `approved`：同样联系 **tsc_members** 进行批准。批准后，由tsc_members评论 `/approve`，机器人会自动添加标签。


## 4. TSC成员变更
### 4.1 变更流程
TSC变更流程详见[TSC治理章程](../governance/tsc-governance.md)。

### 4.2 权限配置
1.  Fork 并修改：Fork `Kunpeng/HPCKit-Community` 仓库到您的个人账号，修改 `governance/TSC/README.md` ；
2.  提交 PR：向 `Kunpeng/HPCKit-Community` 仓库的 `main` 分支提交 PR；
3.  ✅  通过审查并合入pr：您的 PR 需要获得以下三个标签才能被合并：

    - `hpckit-cla/yes`：**CLA协议检查**。机器人会自动检查您 commits 中的邮箱是否已签署 CLA 协议。若已签署，将添加此标签；若未签署，会添加 `hpckit-cla/no` 标签并留言提示；
    - `lgtm`：请联系 `governance/TSC/README.md` 文件中列出的 **tsc_members** 进行评审。评审通过后，tsc_member 评论 `/lgtm`，机器人会自动添加标签；
    - `approved`：同样联系 **tsc_members** 进行批准。批准后，由tsc_members评论 `/approve`，机器人会自动添加标签。
