#  `HPCKit`  社区协作指南
## 概述
欢迎来到 `BoostKit` 社区！本文档旨在为不同角色的社区成员提供清晰的操作指南。无论您是代码贡献者、SIG maintainer，还是项目TC成员，都可以在此找到对应的协作流程。

![1758791739926.png](https://raw.gitcode.com/user-images/assets/7277284/3e91e5bf-005a-4da6-bdd4-8af9e78fe7f3/1758791739926.png '1758791739926.png')

----
## 对于代码贡献者
### 一、如何签署  `BoostKit` 社区贡献者许可协议CLA

在参与社区贡献前，您需要签署[BoostKit 社区贡献者许可协议（CLA）](https://clasign.osinfra.cn/sign/68a817711c58932379902043)
- **个人贡献者**：请选择 **签署个人CLA**
- **企业**：请选择 **签署法人CLA**
- **企业员工**：请选择 **法人贡献者登记**，签署后会收到主题是`Signing CLA on project of xx`的邮件，请联系邮件内容里的`Corporation Managers`进行审批    
<br>    

### 二、如何贡献代码

1.  **Fork 源码仓库**：将目标源码仓库 Fork 到您的个人账号下
2.  **开发与提交**：在您的 Fork 仓库中进行开发，完成后向上游仓库提交 Pull Request (PR)
3.  **通过审查与检查**：您的 PR 必须获得以下四个标签才能被合并：

    - `boostkit-cla/yes`：**CLA协议检查**。机器人会自动检查您 commits 中的邮箱是否已签署 CLA 协议。若已签署，将添加此标签；若未签署，会添加 `boostkit-cla/no` 标签并留言提示
    - `ci-pipeline-passed`：**CI流水线检查**。在 PR 评论区评论 `compile` 以触发 CI。通过后机器人会添加此标签；若失败，则添加 `ci-pipeline-failed` 标签（**根据仓库配置而不一样**）
    - `lgtm`：**技术评审**。CI 通过后，请联系仓库对应 SIG 组的 `sig-info.yaml` 中指定的 **committers**  或者 **maintainers** 审核，通过后并评论 `/lgtm`
    - `approved`：**最终批准**。CI 通过后，请联系仓库对应 SIG 组的 `sig-info.yaml` 中指定的 **committers**  或者 **maintainers** 审核，通过后并评论 `/approve`    
  <br>


### 三、如何撤销已添加的标签

- 撤销`boostkit-cla/yes`标签：仓库管理员评论 `/cla-cancel`
- 撤销`/lgtm`标签 Committer、maintainer或者tc_member评论 `/lgtm cancel`
- 撤销`approved`标签：Committer、maintainer或者tc_member评论 `/approve cancel`

详情请阅：[机器人命令集详情](https://gitcode.com/BoostKit/community/blob/master/command-guide.md)    
  <br>

### 四、如何主动触发检查PR commits 中的邮箱是否签署CLA协议

评论`/check-cla`触发检查CLA协议   
  <br>    

### 五、如何主动触发检查PR是否满足条件合入

评论`/check-pr`触发检查    
  <br>

----
## 对于社区管理者
### 一、如何新增 SIG 组

1.  **Fork 并修改**，在 [boostKit/community/sigs](https://gitcode.com/BoostKit/community/tree/master/sig) 目录下创建新的 **SIG 组目录  (目录名为SIG组名称)**
2.  **创建SIG信息文件**：在该目录中创建 `sig-info.yaml` 文件([参考链接](https://gitcode.com/BoostKit/community/blob/master/sig/README.md))，并配置 maintainers、committers 等信息
3.  **创建代码仓信息文件**:  在SIG组目录下，新建 'boostkit' 文件夹，并按照代码仓首字母逐个完成本SIG组代码仓描述文件的编辑([参考链接](https://gitcode.com/BoostKit/community/blob/master/sig/README.md))
4.  **提交 PR**：提交 PR 至 `master` 分支
5.  **通过审查**：此 PR 需获得 `boostkit-cla/yes`, `lgtm`, `approved` 三个标签。其中`lgtm`, `approved`  需要 **TC member**去审批并评论

**可以参考 SIG：[BoostKit/Infra](https://gitcode.com/BoostKit/community/tree/master/sig/Infra)**    
  <br>
  
### 二、如何调整 SIG 信息文件

1.  **Fork 并修改**：Fork `BoostKit/community` 仓库，修改目标 SIG 的 `sig-info.yaml` 文件([参考链接](https://gitcode.com/BoostKit/community/blob/master/sig/README.md))。
2.  **提交 PR**：向 `BoostKit/community` 仓库的 `master` 分支提交 PR
3.  **通过审查**：此 PR 需获得 `boostkit-cla/yes`, `lgtm`, `approved` 三个标签。其中`lgtm`, `approved`  需要 **TC member**去审批并评论    
  <br>

### 三、如何在社区新增/修改项目

1.  **Fork 并创建**：Fork `BoostKit/community` 仓库。参考现有项目的结构，创建新的项目目录并将该文件名称添加 `sig-info.yaml` 文件 ([参考链接](https://gitcode.com/BoostKit/community/blob/master/sig/README.md))。
2.  **提交 PR**：向 `BoostKit/community` 仓库的 `master` 分支提交 PR
3.  **通过审查**：此 PR 需获得 `boostkit-cla/yes`, `lgtm`, `approved` 三个标签。其中`lgtm`, `approved`  需要 **TC member**去审批并评论       
4. **机器人自动建仓**: PR合入后，机器人会自动创建仓库和分支    
  <br>

---
希望本指南能帮助您更顺畅地参与 `BoostKit` 社区贡献。