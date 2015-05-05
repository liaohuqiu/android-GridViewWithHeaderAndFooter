###### [Please follow me on GitHub, I need your support](http://www.liaohuqiu.net/posts/follow-me-on-github/)

Github: https://github.com/liaohuqiu

twitter: https://twitter.com/liaohuqiu

---

#### [中文版文档](https://github.com/liaohuqiu/android-GridViewWithHeaderAndFooter/blob/master/README-cn.md)

### GridView with Header and Footer

![Screen Shot](https://raw.githubusercontent.com/liaohuqiu/android-GridViewWithHeaderAndFooter/master/screen-shot.png)

This library is contained by `CUBE-SDK`: https://github.com/etao-open-source/cube-sdk. The Demo is HERE: https://github.com/liaohuqiu/android-cube-app . 

#### Maven

```xml
<dependency>
    <groupId>in.srain.cube</groupId>
    <artifactId>grid-view-with-header-footer</artifactId>
    <type>jar</type>
    <version>{lib_version}</version>
</dependency>
```

#### Gradle

``` groovy
compile 'in.srain.cube:grid-view-with-header-footer:{lib_version}'
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
