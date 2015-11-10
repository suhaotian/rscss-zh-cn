# Pitfalls

## 嵌套组件冲突
要注意拥有相同元素的组件嵌套在一个容器里面的时候：

```html
<article class='article-link'>
 <div class='vote-box'>
    <button class='up'></button>
    <button class='down'></button>
    <span class='count'>4</span>
  </div>

  <h3 class='title'>Article title</h3>
  <p class='count'>3 votes</p>
</article>
```

```scss
.article-link {
  > .title { /* ... */ }
  > .count { /* ... (!!!) */ }
}

.vote-box {
  > .up { /* ... */ }
  > .down { /* ... */ }
  > .count { /* ... */ }
}
```

这个例子中，如果 `.article-link > .count` 没有 `>` 子选择器，那么样式会自动地添加给 `.vode-box .count` 元素。
这也是推荐使用子选择器的原因。
 
