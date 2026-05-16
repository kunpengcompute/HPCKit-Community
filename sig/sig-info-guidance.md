# SIG相关配置的格式化存储

## 1. 背景

本目录下存放的是 `HPCKit` 社区中，所有代码仓与特别兴趣小组（Special Interest Group，以下简称SIG）的配置信息。

本目录下每一个子目录代表一个SIG。每个SIG目录中存在一个`sig-info.yaml`文件，用来配置SIG的成员信息以及SIG管理的仓库。

## 2. 配置管理方式

1. 每个SIG在`HPCKit/community`仓库的`sig`目录中都对应一个独立目录，目录名为`<SIG名称>`
2. 原则上由技术指导委员会（Technical Steering Committee，以下简称TSC）修改和维护。各个SIG对应的`sig-info.yaml`的修改，由该SIG的Maintainer提交PR，经过TC审视后合入。
3. 各SIG目录下的`README.md`为SIG的信息展示区。其中SIG基本信息需按模板留空，由工具自动填充。

## 3. 格式规范

### `sig-info.yaml`文件格式

`sig-info.yaml`文件使用`YAML`格式承载，包含如下属性：

| 字段 | 类型 | 说明 |
|--|--|--|
| `name` | string | SIG组名称，与目录名相同 |
| `description` | string | SIG组描述信息 |
| `maintainers` | sequence | SIG组所有Maintainer的信息 |
| `repositories` | sequence | SIG组管理的仓库信息 |

其中，`repositories`的每一个元素代表一个仓库组（逻辑概念），每个仓库组中的仓库具有相同的Committer：

| 字段 | 类型 |  说明 |
|--|--|--|
| `repo` | sequence | 一组SIG仓库的信息 |
| `committers` | sequence | 仓库组所有Committer的信息 |

根节点下`maintainers`的每一个元素代表SIG中的一位Maintainer，具有SIG下所有仓库的PR合入权限；`repositories`每个元素下的`committers` 的每一个元素分别代表仓库组中的一位Committer；Committer具有该仓库组下所有仓库的PR合入权限

| 字段 | 类型 |  说明 |
|--|--|--|
| `atomgit_id` | string | 用户atomgit ID |
| `name` | string | 用户姓名 |
| `organization` | string | 组织信息 |
| `email` | string | 用户email |

### sig-info.yaml 样例

```yaml
name: Infra # SIG名称，与目录名保持一致
description: "负责HPCKit社区基础设施的配置和维护"
maintainers: # SIG maintainer
  - atomgit_id: georgecao
    name: 曹志
    organization: huawei
    email: george.cao@huawei.com
repositories: # SIG仓库组（逻辑概念）；每个仓库组中的仓库具有相同的committer、member和repo_admin
  - repo:
      - kunpengcompute/hpckit-community
      - kunpengcompute/Infra
    committers: # 仓库committer
      - atomgit_id: yao-xiaobai
        name: 姚孝添
        organization: huawei
        email: 176253319000@163.com
      - atomgit_id: Guangyue-Xu
        name: 许广跃
        organization: huawei
        email: xuguangyue2@huawei.com
```

### 仓库配置信息
`HPCKit` 社区所有代码仓信息都维护在 `sig/<SIG名称>/kunpengcompute` 目录下，并按照代码仓首字母作为子目录进行分类。    
代码仓 `YAML` 文件字段如下:
| 字段 | 类型 |  说明 |
|--|--|--|
| `name` | string | 代码仓名称 |
| `type` | string | 仓库可见性（public&private） |
| `description` | string | 描述信息 |
| `branches` | string | 分支信息 |


| 字段 | 类型 |  说明 |
|--|--|--|
| `name` | string | 分支名称 |
| `type` | string | 分支属性（public&protected） |
| `create_from` | string | 非必要字段，创建分支指定 |

### repo-info.yaml 样例

```yaml
name: HPCKit-Community
type: public
description: "HPCKit社区配置仓库"
branches:
  - name: main
    type: protected
```
