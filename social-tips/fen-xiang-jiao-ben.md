# 分享脚本

{% code lineNumbers="true" %}
```javascript
// Twitter Fcebook Ins WhatsApp
 function shareToSocial() {
        const shareData = {
            title: document.getElementById('shareTitle').innerText,
            text: '发现这个很棒的产品：',
            url: window.location.href,
        };

        if (navigator.share) {
            navigator.share(shareData)
                .then(() => console.log('分享成功'))
                .catch(err => console.error('分享失败:', err));
        } else {
            // 兼容方案：弹出平台选择
            const platforms = [
                { 
                    name: 'Twitter',
                    url: `https://twitter.com/intent/tweet?text=${encodeURIComponent(shareData.title)}&url=${encodeURIComponent(shareData.url)}`
                },
                {
                    name: 'Facebook',
                    url: `https://www.facebook.com/sharer/sharer.php?u=${encodeURIComponent(shareData.url)}`
                },
                {
                    name: 'Instagram',
                    url: `https://www.instagram.com/`, // 只能引导用户手动分享
                },
                {
                    name: 'WhatsApp',
                    url: `https://wa.me/?text=${encodeURIComponent(shareData.text + ' ' + shareData.url)}`
                }
            ];
            
            const choice = prompt('请选择分享平台：\n1 - Twitter\n2 - Facebook\n3 - Instagram（需手动操作）\n4 - WhatsApp');
            const index = parseInt(choice) - 1;

            if (index === 2) {
                alert('请打开 Instagram 并手动上传产品图片和链接！');
            } else if (index >= 0 && index < platforms.length) {
                window.open(platforms[index].url, '_blank');
            }
        }
    }
```
{% endcode %}
