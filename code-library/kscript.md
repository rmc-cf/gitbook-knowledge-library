---
description: 关于KScript的一些代码片段
---

# KScript



```javascript
// 保存Base64
export function saveBase64(input: string, file: string): KScript.FileInfo {
    const base64Rule = /^data:([\w\/]+);base64,(.+)$/i;
    let base64 = input;
    const match = base64.match(base64Rule);
    let filename = file;
    let contentType = "image/png";
    let base64Data = base64;
    if (match) {
        contentType = match[1];
        base64Data = match[2];
    }
    try {
        const ext = k.utils.mime.getExtensions(contentType)[0];
        if (ext) {
            filename = filename.substring(0, filename.lastIndexOf('.') + 1) + ext;
        }
    } catch (error) {
        k.logger.warning("SaveBase64", error);
    }
    const bytes = k.security.decodeBase64(base64Data);
    return writeFile(filename, bytes);
}
```

{% code title="" overflow="wrap" lineNumbers="true" %}
```javascript
// 图片转webp
export const imgToWebpUrl = (url: string, size?: string | number): string => {
    // 参数检查
    if (!url) return ''
    // 检查特殊格式
    if (url.startsWith('data:image') || url.startsWith('blob:')) {
        return url
    }
    // 检查是否已经是 webp 格式
    if (url.toLowerCase().endsWith('.webp')) {
        return url
    }
    // 准备参数数组
    const params: string[] = []
    // 处理 format 参数
    const formatRegex = /[?&]format=[^&]+/i
    if (formatRegex.test(url)) {
        url = url.replace(formatRegex, '')
    }
    params.push('format=webp') 
    // 处理尺寸参数
    if (size) {
        // 移除已存在的 width 和 height 参数
        const sizeRegex = /[?&](width|height)=\d+/gi
        url = url.replace(sizeRegex, '')
        // 添加新的尺寸参数
        const sizeValue = String(size).replace('px', '')
        params.push(`width=${sizeValue}`)
    }
    // 组合 URL
    const connector = url.includes('?') ? '&' : '?'
    return url + connector + params.join('&')
}
```
{% endcode %}

<pre class="language-javascript"><code class="lang-javascript">// 快递100接入
<strong>        param = JSON.stringify(param)
</strong>        // param + key + customer: md5加密
        let rawSign = `${param}${obj.sign}${obj.customer}`
        rawSign = k.security.md5(rawSign)
        let url = `https://poll.kuaidi100.com/poll/query.do?customer=${obj.customer}&#x26;sign=${rawSign}&#x26;param=${param}`
        let result = k.net.url.post(url, {})
        item.logisticsData = JSON.parse(result).data || []
        return item
</code></pre>
