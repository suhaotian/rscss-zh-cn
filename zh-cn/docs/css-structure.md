# CSS 结构

## 一个组件一个文件
对于每个组件，将它们放在它们自己的文件里面。

  ```scss
  /* css/components/search-form.scss */
  .search-form {
    > .button { /* ... */ }
    > .field { /* ... */ }
    > .label { /* ... */ }

    // variants
    &.-small { /* ... */ }
    &.-wide { /* ... */ }
  }
  ```

## 使用全局匹配
在 sass-rails 和 stylus 中（sass-rails 和 stylus 都是 CSS 预处理器），包含它们是如此简单：

  ```scss
  @import 'components/*';
  ```

## 避免过度的嵌套
嵌套不要超过2级。过多的嵌套会很容易变得不可维护。

  ```scss
  /* ✗ 避免3级嵌套 */
  .image-frame {
    > .description {
      /* ... */

      > .icon {
        /* ... */
      }
    }
  }

  /* ✓ 更好：2级嵌套*/
  .image-frame {
    > .description { /* ... */ }
    > .description > .icon { /* ... */ }
  }
  ```
