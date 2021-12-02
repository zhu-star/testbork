
---
title: 【vue】跨域解决方案之proxyTable
date: 2017-12-28
tags:
- vue
- webpack
---
## 一

### 配置

​     module.exports = {  title: "vuepress-theme-reco",  //这里是博客标题  description: 'A simple and beautiful vuepress blog theme .',  //博客描述  dest: 'public',  //博客部署时输出的文件夹  head: [    ['link', { rel: 'icon', href: '/favicon.ico' }],  //favicon图标设置    ['meta', { name: 'viewport', content: 'width=device-width,initial-scale=1,user-scalable=no' }]  ]  theme: 'reco',  //vuepress挂载的主题  themeConfig: {      //导航栏    nav: [      { text: 'Home', link: '/', icon: 'reco-home' },  //text:导航标题内容，icon：图标样式      { text: 'TimeLine', link: '/timeline/', icon: 'reco-date' },      { text: 'Docs',         icon: 'reco-message',        items: [          { text: 'vuepress-reco', link: '/docs/theme-reco/' }  //item： 子导航        ]      },      { text: 'Contact',         icon: 'reco-message',        items: [          { text: 'GitHub', link: 'https://github.com/recoluan', icon: 'reco-github' }        ]      }    ],    //侧边栏设置    sidebar: {      '/docs/theme-reco/': [        '',        'theme',        'plugin',        'api'      ]    },      type: 'blog',    // 博客设置    blogConfig: {      category: {        location: 2, // 在导航栏菜单中所占的位置，默认2        text: 'Category' // 默认 “分类”      },      tag: {        location: 3, // 在导航栏菜单中所占的位置，默认3        text: 'Tag' // 默认 “标签”      }    },   //友情链接    friendLink: [      {        title: '午后南杂',        desc: 'Enjoy when you can, and endure when you must.',        email: '1156743527@qq.com',        link: 'https://www.recoluan.com'      },      {        title: 'vuepress-theme-reco',        desc: 'A simple and beautiful vuepress Blog & Doc theme.',        avatar: "https://vuepress-theme-reco.recoluan.com/icon_vuepress_reco.png",        link: 'https://vuepress-theme-reco.recoluan.com'      },    ],      //博客自定义LOGO    logo: '/logo.png',    // 搜索设置    search: true,    searchMaxSuggestions: 10,    // 自动形成侧边导航    // sidebar: 'auto',    // 最后更新时间    lastUpdated: 'Last Updated',    // 作者    author: 'reco_luan',    // 作者头像    authorAvatar: '/avatar.png',    // 备案号    record: 'xxxx',    // 项目开始时间    startYear: '2017'    /**     * 密钥 (if your blog is private)     */   //私有仓库key和密码    // keyPage: {    //   keys: ['your password'],    //   color: '#42b983',    //   lineColor: '#42b983'    // },     /**     *评论     * valine 设置 (if you need valine comment )     */     // valineConfig: {    //   appId: '...',// your appId    //   appKey: '...', // your appKey    // }  },  markdown: {    lineNumbers: true  } }

