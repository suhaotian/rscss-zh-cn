# 辅助方法

通用类意味着覆盖值，将它们分离进一个文件并且命名以下划线开头。它们都是典型的有 *!important* 属性的标签。应该谨慎使用它们。

```css
._unmargin { margin: 0 !important; }
._center { text-align: center !important; }
._pull-left { float: left !important; }
._pull-right { float: right !important; }
```

## 辅助方法命名
以下划线为前缀会简单的从组件中区别开来。下划线也看起来有一丁点丑，还有另一种效果：当使用过多的时候，会看起来很沮丧： 

  ```html
  <div class='order-graphs -slim _unmargin'>
  </div>
  ```

## 组织辅助方法
将所有辅助方法放进一个叫做 `helpers` 的文件中。你可以将它们分离进不同的文件，保持你的辅助方法精简短小。
