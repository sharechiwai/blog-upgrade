---
title: "ReactJs set base path - "
date: 2020-08-10T00:00:00+08:00
author: ShareChiWai
layout: post
categories:
  - Javascript
  - ReactJs
  - Code Playground
tags:
  - ReactJs
  - config
  - Open Source
---

係 GitHub 用 GitHub Page Host 果個 ReactJs Project  
由於個 Page 係 Subfolder 同 存放  
e.g. https://sharechiwai.github.io/code-playground  
而不是 https://sharechiwai.github.io  
所以當我 reploy ReactApp 到 GitHub Page 上時  
當 click 去任何一條 Link 時..他沒有 suffix code-playground e.g.(contact)  
便 navigate 去了 https://sharechiwai.github.io/contact  
而不是很聰明地 去 https://sharechiwai.github.io/code-playground/contact

那麼怎樣可以解決這個問題

**暫時既解決方法**
我們可以在 `BrowserRouter` 上使用`basename` 這個 property  
e.g.

```
        <BrowserRouter basename='/code-playground'>
          <NavBar />
          <Container maxWidth='xl' className='main-container'>
            <Switch>
              <Route exact path='/' component={Home} />
              <Route exact path='/contact' component={Contact} />
            </Switch>
          </Container>
        </BrowserRouter>
```

Hope you find it useful
