# 布局

![](images/layouts.png)

## 避免定位属性
组件应该在不同的地方都可以重用。所以要避免在组件中使用这些属性：

  * 定位 (`position`, `top`, `left`, `right`, `bottom`)
  * 浮动 (`float`, `clear`)
  * margin (`margin`)
  * 尺寸 (`width`, `height`) *

## 固定尺寸

有些元素可能会是例外，拥有固定的尺寸，比如头像和 logo。

## 定位写在父元素中

如果你需要定义这些避免的属性，你应该写在它们的父元素中。下面的这个例子，注意浮动和宽度是加到 *list* 上的，而不是组件自身。

  ```css
  .article-list {
    & {
      @include clearfix;
    }

    > .article-card {
      width: 33.3%;
      float: left;
    }
  }

  .article-card {
    & { /* ... */ }
    > .image { /* ... */ }
    > .title { /* ... */ }
    > .category { /* ... */ }
  }
  ```

怎么在布局外面添加外边距（margins）？ 尝试使用辅助方法。
[继续 →](helpers.md)
<!-- {p:.pull-box} -->
