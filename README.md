# HPCKit社区

欢迎来到HPCKit社区，社区致力于为业界提供高效的科学与智能计算解决方案，发挥鲲鹏硬件优势。

## 1. 开源项目

<table border="1" style="width: 100%; table-layout: fixed;">
  <colgroup>
    <col style="width: 15%;">
    <col style="width: 60%;">
    <col style="width: 25%;">
  </colgroup>
  <thead>
    <tr>
      <th style="width: 15%;"><div style="text-align: center;">组件</div></th>
      <th style="width: 60%;"><div style="text-align: center;">描述</div></th>
      <th style="width: 25%;"><div style="text-align: center;">源码仓</div></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><div style="text-align: center;">基础加速库</div></td>
      <td>提供基于鲲鹏平台优化的基础加速库。</td>
      <td><a href="https://atomgit.com/kunpengcompute/kupl">kupl</a> <br> <a href="https://atomgit.com/kunpengcompute/hmpi">hmpi</a> <br> <a href="https://atomgit.com/kunpengcompute/hucx">hucx</a> <br> <a href="https://atomgit.com/kunpengcompute/xucg">xucg</a></td>
    </tr>
    <tr>
      <td><div style="text-align: center;">领域加速库</div></td>
      <td>提供针对特定高性能计算场景（如量子色动力学、分子动力学等）在鲲鹏平台上深度优化的加速库。它们利用鲲鹏处理器架构特性，通过指令级优化、算法重构和并行加速等手段，显著提升相应领域应用的运行效率。</td>
      <td><a href="https://atomgit.com/kunpengcompute/kutacc">kutacc</a> <br> <a href="https://atomgit.com/kunpengcompute/kudnn">kudnn</a> <br> <a href="https://atomgit.com/kunpengcompute/kuqcd">kuqcd</a> <br> <a href="https://atomgit.com/kunpengcompute/sglang">sglang</a></td>
    </tr>
    <tr>
      <td><div style="text-align: center;">编程框架</div></td>
      <td>提供基于鲲鹏平台优化的编程框架。</td>
      <td><a href="https://atomgit.com/kunpengcompute/kunpeng-extension-for-pytorch">kunpeng-extension-for-pytorch</a></td>
    </tr>
    <tr>
      <td><div style="text-align: center;">示例代码</div></td>
      <td>提供HPCKit最优编程示例代码。</td>
      <td><a href="https://atomgit.com/kunpengcompute/hpckit-sample">hpckit-sample</a> <br> <a href="https://atomgit.com/kunpengcompute/DeepSeek-V3-Sample">DeepSeek-V3-Sample</a></td>
    </tr>
  </tbody>
</table>

## 2. 关于社区

### 2.1 社区治理架构

HPCKit 社区采用分层协作的治理模式，当前架构主要包括以下组织：

- [技术指导委员会（TSC）](governance/TSC/README.md) —— 负责技术愿景与方向决策
- [特别兴趣小组（SIG）](sig) —— 专注特定技术领域或公共能力建设

### 2.2 社区治理章程

如需了解社区治理章程，请参阅以下文档：

- [技术指导委员会（TSC）治理章程](governance/tsc-governance.md)
- [特别兴趣小组（SIG）治理章程](governance/sig-governance.md)
- [社区角色定义及晋升机制](governance/role-definition-and-promotion-mechanism.md)

## 3. 用户行为准则

参与社区贡献前，请仔细阅读并遵守社区[用户行为准则](contributor/code-of-conduct.md)。您在 HPCKit 社区的所有活动（包括但不限于发表评论、提交 Issue/PR/文档等）均需遵循此准则。

## 4. 参与贡献

- [签署CLA](https://clasign.osinfra.cn/sign/69ca19493107795d582d07fc)：签署个人/法人 CLA。
- [基础贡献](contributor/basic-contribution.md)：包含参与社区会议、社区邮件讨论、提交 Issue 、处理 Issue 任务、提交PR等。
- [进阶贡献](contributor/advanced-contribution.md)：包含新建 SIG、成为核心贡献者、组织会议、新建仓库、引入开源软件、发布新版本或新仓库等。

## 5. 联系我们

- [社区邮件订阅](https://mailweb.hpckit.osinfra.cn/postorius/lists)：选择需要订阅的组织（TSC/SIG等），填写相关信息，进行邮件订阅（邮件推送内容包含：会议通知、会议纪要、内容讨论等），如果您对相关组织有诉求或者问题，也可以通过邮箱途径联系。

## 6. 相关链接

- [鲲鹏社区（HPC专区）](https://www.hikunpeng.com/developer/hpc)
- [鲲鹏论坛（HPC专区）](https://www.hikunpeng.com/forum/forum-0187135482144798003-1.html)

