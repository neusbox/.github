<p align="center">
  <a href="https://github.com/neusbox/neu_box">
    <img src="https://raw.githubusercontent.com/neusbox/neu_box/main/docs/neu_box.png" alt="Neu Box Logo" width="150">
  </a>
</p>

<h1 align="center">Neu Box</h1>

<p align="center">
  面向 Linux 异构计算节点的轻量级设备资源仲裁、沙盒隔离与任务执行系统
</p>

<p align="center">
  Worker · WebUI · CLI · Agent Skill
</p>

Neu Box 为 GPU、NPU 等异构计算节点提供统一的资源入口，将设备分配、cgroup v2
隔离、eBPF 访问控制、异步任务执行和可回滚运维整合为一套轻量系统。

## 项目组成

| 仓库 | 职责 | 入口 |
|---|---|---|
| [**neu_box**](https://github.com/neusbox/neu_box) | 核心 Worker、设备沙盒、任务队列、安装与升级 | [部署文档](https://github.com/neusbox/neu_box/blob/main/docs/deployment.md) · [Releases](https://github.com/neusbox/neu_box/releases) |
| [**neu_box_webui**](https://github.com/neusbox/neu_box_webui) | 多节点管理、任务转发、实验记录和 Web 界面 | [使用说明](https://github.com/neusbox/neu_box_webui#readme) |
| [**neu_box_goClient**](https://github.com/neusbox/neu_box_goClient) | `neu-sbox` CLI、终端沙盒、任务跟踪和 Agent skill | [使用说明](https://github.com/neusbox/neu_box_goClient#readme) |

三个仓库独立维护、独立发版，不共享运行时代码，仅通过版本化 HTTP 契约协作。
核心仓库使用 submodule 固定经过验证的 WebUI 与 CLI 配套提交。

## 能力概览

- 为宿主机终端或现有 Docker 容器分配独占设备沙盒
- 通过 cgroup v2 与 eBPF 管理设备访问边界
- 提交带优先级、资源约束和持久化日志的异步任务
- 使用 WebUI 管理节点池、任务和实验记录
- 使用 `neu-sbox` 或标准 `curl` 直接接入 Worker API v2
- 支持版本化安装、GitHub 在线更新、数据库迁移和失败回滚

## 快速入口

- [开始部署 Worker](https://github.com/neusbox/neu_box#快速开始)
- [Worker HTTP API v2](https://github.com/neusbox/neu_box/blob/main/docs/worker-api.md)
- [安装 `neu-sbox`](https://github.com/neusbox/neu_box_goClient#安装)
- [运行 WebUI](https://github.com/neusbox/neu_box_webui#直接运行)
- [提交问题与建议](https://github.com/neusbox/neu_box/issues)

<p align="center">
  <sub>Built for practical accelerator sharing on Linux.</sub>
</p>
