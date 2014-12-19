### GridView with Header and Footer

![Screen Shot](https://raw.githubusercontent.com/liaohuqiu/android-GridViewWithHeaderAndFooter/master/screen-shot.png)

只有一个文件，你可以将源代码放入你的项目中。另外项目发布到了Maven中央库，你可以通过`pom`或者`gradle`引入。

#### Maven

```xml
<dependency>
    <groupId>in.srain.cube</groupId>
    <artifactId>grid-view-with-header-footer</artifactId>
    <type>jar</type>
    <version>1.0.9</version>
</dependency>
```

#### Gradle

``` groovy
compile 'in.srain.cube:grid-view-with-header-footer:1.0.9'
```

### 使用示例

```java
GridViewWithHeaderAndFooter gridView = (GridViewWithHeaderAndFooter) v.findViewById(R.id.ly_image_list_grid);

LayoutInflater layoutInflater = LayoutInflater.from(this);
View headerView = layoutInflater.inflate(R.layout.test_header_view, null);
View footerView = layoutInflater.inflate(R.layout.test_footer_view, null);
gridView.addHeaderView(headerView);
gridView.addFooterView(footerView);
```

#### 滑到底部之后，加载更多

从`1.0.4`之后版本开始支持。

```
public void tryToScrollToBottomSmoothly();
public void tryToScrollToBottomSmoothly(int duration);
```

When scroll to the bottom, you may need to show the footer view when loading data from server.

```java
mFooterView.setVisibility(View.VISIBLE);
mGridView.post(new Runnable() {
    @Override
    public void run() {
        mGridView.tryToScrollToBottomSmoothly(100);
    }
});
mGridView.postDelay(new Runnable() {
    @Override
    public void run() {
    // 处理加载更多
    }
}, 150);
```

### Thanks

[HeaderGridView](https://android.googlesource.com/platform/packages/apps/Gallery2/+/idea133/src/com/android/photos/views/HeaderGridView.java)

### License

Apache 2

### 联系方式 / 帮助支持

Please fell free to contact me if there is any problem when using the library.

* srain@php.net
* twitter: https://twitter.com/liaohuqiu
* 微博: http://weibo.com/liaohuqiu
* QQ 群: 271918140
