# Plugin示例



> Docsify 基础配置

```javascript
window.$docsify = {
    name: 'docsify-demo',
    repo: '',
    maxLevel: 5, //最大支持渲染的标题层级
    subMaxLevel: 6,
    homepage: 'README.md',
    coverpage: true,
    loadSidebar: true,
    auto2top: true, //切换页面后是否自动跳转到页面顶部
    search: { //全文搜索
        maxAge: 86400000, // 过期时间，单位毫秒，默认一天
        paths: 'auto',
        placeholder: 'Type to search',
        noData: 'No Results!',
        depth: 3, // 搜索标题的最大程级, 1 - 6
        hideOtherSidebarContent: false,
    },
    plugins: [
        EditOnGithubPlugin.create(
            'https://github.com/docsifyjs/docsify/blob/master/docs/',
            'https://github.com/docsifyjs/docsify/blob/develop/docs/',
            function (filename) {
                if (filename.indexOf('zh') !== -1) {
                    return '在Github上编辑'
                } else {
                    return 'Edit On Github'
                }
            }
        )
    ]
}
```



> 在Java中，你可以使用StringBuilder和一个简单的循环来去除字符串中的连续重复字符。以下是一个示例：

```java
public class Main {
    public static void main(String[] args) {
        String str = "aaabbbcccdde";
        System.out.println(removeConsecutiveDuplicates(str));
    }

    public static String removeConsecutiveDuplicates(String str) {
        StringBuilder sb = new StringBuilder();
        char lastChar = '\0';

        for (char c : str.toCharArray()) {
            if (c != lastChar) {
                sb.append(c);
                lastChar = c;
            }
        }

        return sb.toString();
    }
}
```



