+++
toc = true
title = "使用规范"
weight = 3
+++

## 支持项
1. 提供了一主多从的读写分离配置，可独立使用，也可配合分库分表使用。
1. 独立使用读写分离支持SQL透传。
1. 同一线程且同一数据库连接内，如有写入操作，以后的读操作均从主库读取，用于保证数据一致性。
1. Spring命名空间。
1. 基于Hint的强制主库路由。

## 不支持范围
1. 主库和从库的数据同步。
1. 主库和从库的数据同步延迟导致的数据不一致。
1. 主库双写或多写。