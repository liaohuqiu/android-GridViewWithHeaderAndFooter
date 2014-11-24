## [中文版文档](https://github.com/liaohuqiu/android-GridViewWithHeaderAndFooter/blob/master/README-cn.md)

### GridView with Header and Footer

![Screen Shot](https://raw.githubusercontent.com/liaohuqiu/android-GridViewWithHeaderAndFooter/master/screen-shot.png)

#### Maven

```xml
<dependency>
    <groupId>in.srain.cube</groupId>
    <artifactId>grid-view-with-header-footer</artifactId>
    <type>jar</type>
    <version>1.0.7</version>
</dependency>
```

#### Gradle

``` groovy
compile 'in.srain.cube:grid-view-with-header-footer:1.0.7'
```

### Usage

```java
GridViewWithHeaderAndFooter gridView = (GridViewWithHeaderAndFooter) v.findViewById(R.id.ly_image_list_grid);

LayoutInflater layoutInflater = LayoutInflater.from(this);
View headerView = layoutInflater.inflate(R.layout.test_header_view, null);
View footerView = layoutInflater.inflate(R.layout.test_footer_view, null);
gridView.addHeaderView(headerView);
gridView.addFooterView(footerView);
```

#### When scroll to bottom to load more data for GridView

since 1.0.4

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
    // load more data
    }
}, 150);
```

### Thanks

[HeaderGridView](https://android.googlesource.com/platform/packages/apps/Gallery2/+/idea133/src/com/android/photos/views/HeaderGridView.java)

### License

Apache 2

### contact or help

Please fell free to contact me if there is any problem when using the library.

* srain@php.net
* twitter: https://twitter.com/liaohuqiu
* weibo: http://weibo.com/liaohuqiu
* QQ tribe: 271918140
