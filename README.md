QX Youtube 无中文字幕机翻方案
提示：仅英文时自动开启，不影响已有中文字幕 @id77_GitHub

#Quantumult X 直接订阅--添加资源列表（重写）强烈推荐-任何语言一律翻译中文
https://raw.githubusercontent.com/id77/QuantumultX/master/rewrite/Youtube_CC.conf, tag=Youtube 文机翻中文, update-interval=172800, opt-parser=false, enabled=true

添加mitm的hostname
www.youtube.com

// 重写，简体；
https:\/\/www.youtube.com\/api\/timedtext\?.+&lang=en.+?((?!&tlang=zh\-Hans).)*$ url request-header \sHTTP/1\.1(\r\n) request-header &tlang=zh-Hans HTTP/1.1$1
// 重写，繁体
https:\/\/www.youtube.com\/api\/timedtext\?.+&lang=en.+?((?!&tlang=zh\-Hant).)*$ url request-header \sHTTP/1\.1(\r\n) request-header &tlang=zh-Hant HTTP/1.1$1
//重写，自定义
https:\/\/www.youtube.com\/api\/timedtext\?.+&lang=待翻译语种.+?((?!&tlang=目标语种).)*$ url request-header \sHTTP/1\.1(\r\n) request-header &tlang=目标语种 HTTP/1.1$1


有多需求的，可以订阅设置
需配合资源解析器

提示lang=xxx可以自行抓包替换

# 所有翻译为中文
https://raw.githubusercontent.com/id77/QuantumultX/master/rewrite/Youtube_CC.conf#replace=lang\=en@lang=

# 只翻译日语为中文
https://raw.githubusercontent.com/id77/QuantumultX/master/rewrite/Youtube_CC.conf#replace=lang\=en@lang=ja

以此类推

感谢大佬 
@id77_GitHub
