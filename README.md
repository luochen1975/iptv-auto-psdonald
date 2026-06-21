# 📺 港澳台 IPTV 直播源

> 每天北京时间 **8:10** 自动从 GitHub 多个公开仓库抓取港澳台电视台直播源，三级验证可用性后发布。

## 📁 文件说明

| 文件 | 格式 | 用途 |
|------|------|------|
| `output/hk.txt` | TVBox/tv.txt | TVBox、APTV 等APP直接导入 |
| `output/hk.m3u` | M3U | VLC、PotPlayer、IINA 播放 |
| `output/hk.json` | JSON | 开发者接口（含验证结果） |

## 🔗 订阅地址

```
https://raw.githubusercontent.com/40740/iptv-auto/main/output/hk.txt
https://raw.githubusercontent.com/40740/iptv-auto/main/output/hk.m3u
```

## 📺 覆盖频道

- **港台 RTHK**: TV 31-35
- **TVB**: 翡翠台、无线星河、TVB News
- **HOY TV**: HOY TV、資訊台
- **ViuTV**: ViuTV 99
- **凤凰卫视**: 凤凰中文、凤凰资讯、凤凰电影、凤凰香港
- **TVBS**: TVBS亚洲、TVBS新闻台
- **香港卫视**: 香港卫视
- **澳门**: TDM 澳视、澳门有线
- **其他**: 耀才财经、天映经典、Now星影台等

## 🔄 数据源

| 来源 | 说明 |
|------|------|
| [iptv-org](https://github.com/iptv-org/iptv) | 全球最大公开 IPTV 数据库 |
| [imDazui/Tvlist](https://github.com/imDazui/Tvlist-awesome-m3u-m3u8) | 港澳台定期更新合集 |
| [ChinaIPTV](https://github.com/hujingguang/ChinaIPTV) | 中国含港澳台，每15分钟自动更新 |

## ✅ 三级验证

```
Level 1 - HTTP连通: 请求 m3u8 地址, 状态码 < 400
Level 2 - 内容有效: 返回内容含 m3u8 标签或视频数据
Level 3 - 有视频流: 请求第一个 ts 分片, 确认返回 MPEG-TS 视频数据
```

## ⚙️ 手动触发

在仓库 Actions 页面点击 **Run workflow** 即可手动执行一次。

## 📱 使用方法

### TVBox / APTV
设置 → 订阅 → 添加订阅地址:
```
https://raw.githubusercontent.com/40740/iptv-auto/main/output/hk.txt
```

### VLC / PotPlayer / IINA
媒体 → 打开网络串流 / 打开文件:
```
https://raw.githubusercontent.com/40740/iptv-auto/main/output/hk.m3u
```
