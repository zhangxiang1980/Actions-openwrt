# Action🔑 关键变更说明

源码仓库:

owner: 默认为 openwrt

repo: 默认为 openwrt

这是 OpenWrt 官方的源码仓库，而非 ImmortalWrt。

分支版本:

branch: 默认为 openwrt-24.10。

说明: OpenWrt 的版本号格式为 主版本.次版本.修订版 (如 24.10.4)。GitHub 上通常只有大分支（如 openwrt-24.10），具体的小版本（如 24.10.4）是该分支上的一个 Tag 或提交点。

如何获取最新版: 使用 openwrt-24.10 分支会编译出该系列最新的固件（目前可能是 24.10.5 或更高），这通常比固定的 24.10.4 更安全、更稳定。

如何强制指定 24.10.4: 如果你在运行时非常需要 24.10.4 这个特定版本，可以在点击 "Run workflow" 时，手动将 branch 输入框的内容改为 v24.10.4 (前提是该 Tag 存在于官方仓库中)，或者留空默认使用最新分支。

目录结构:

源码目录名从 ImmortalWrt 改为了 openwrt，以匹配官方习惯。

输出路径调整为 openwrt/bin/targets/ramips/mt7621。

设备支持:

确保你的 .config 文件中正确选择了：

Target System: Ramips MIPS architecture

Subtarget: MT7621 based boards

Target Profile: HiWiFi HC5962 (对应配置项 CONFIG_TARGET_ramips_mt7621_DEVICE_hiwifi_hc5962=y)

📥 编译产物
编译成功后，下载的 Artifact (OpenWrt-HiWiFi-HC5962) 中将包含：
openwrt-ramips-mt7621-hiwifi_hc5962-squashfs-sysupgrade.bin (升级用)
openwrt-ramips-mt7621-hiwifi_hc5962-squashfs-factory.bin (原厂刷入用)
文件名中的版本号将反映你编译时的实际版本（例如 openwrt-24.10.5-...）。s-openwrt
