# muse-qx-rules

Quantumult X 分流规则：让 Muse 走代理。

## 文件

- `Muse.list` — QX 分流规则，策略为 `proxy`

## QX 远程引用

在 QX 配置文件 `[filter_remote]` 里加一行：

```
https://raw.githubusercontent.com/xian9158/muse-qx-rules/main/Muse.list, tag=Muse, enabled=true
```

## 国内镜像（raw.githubusercontent.com 打不开时用这个）

jsDelivr 国内有节点，QX 里用这行：

```
https://cdn.jsdelivr.net/gh/xian9158/muse-qx-rules@main/Muse.list, tag=Muse, enabled=true
```

备用镜像：

```
https://mirror.ghproxy.com/https://raw.githubusercontent.com/xian9158/muse-qx-rules/main/Muse.list, tag=Muse, enabled=true
```

## QX 本地用法

QX → 配置文件 → 编辑 → 在 `[filter_local]` 里粘贴 `Muse.list` 的内容，保存。

策略组不叫 `proxy` 时，把文件里的 `proxy` 批量替换成你的策略组名。

## 覆盖域名

- `muse.ai`、`meta.ai`、`metaaivm.com`（含 `hatch.metaaivm.com` VM 通道、`hatch-api.meta.ai`、`graph.meta.ai`、`api.meta.ai`）
- Meta 账号登录：`meta.com`、`facebook.com`、`fbcdn.net` 等
- Instagram / Messenger / WhatsApp、Meta CDN、Meta IP 段（AS32934）
