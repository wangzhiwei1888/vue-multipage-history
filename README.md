# vue-multipage-history

> A Vue.js project

```

网上好的多入口使用 vue-cli 构建的例子
但是都不能用 history ，
此项目 未使用  vue-cli构建，只是单纯的 在页面中引入 vue.js 和 vue-router.js
在一个项目中 采用多入口 实现 history的模式。

访问路径
http://127.0.0.1/p2p/index/bar
http://127.0.0.1/p2p/a/bar


nginx 配置

location /p2p/a/ {
            
    try_files $uri $uri/ /p2p/a/index.html;
    root   html;
    index  index.html index.htm;

}

location /p2p/index/ {
    
    try_files $uri $uri/ /p2p/index/index.html;
    root   html;
    index  index.html index.htm;

}

项目目录

├── a
│   ├── a.js
│   └── index.html
├── bank
│   └── index.html
├── index
│   ├── index.html
│   └── index.js
└── static
    └── vue-router.js


后续如果采用 vue-cli 可以将项目构建成上面的目录，就可以了。





```