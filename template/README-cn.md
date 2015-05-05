###### [关注我的GitHub吧，江湖救急，需要你的支持和帮助](http://www.liaohuqiu.net/cn/posts/follow-me-on-github/)

Github: https://github.com/liaohuqiu

微博: http://weibo.com/liaohuqiu

---

### GridView with Header and Footer

![Screen Shot](https://raw.githubusercontent.com/liaohuqiu/android-GridViewWithHeaderAndFooter/master/screen-shot.png)

只有一个文件，你可以将源代码放入你的项目中。另外项目发布到了Maven中央库，你可以通过`pom`或者`gradle`引入。

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

### 使用示例

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

### 联系方式 / 帮助支持

Please fell free to contact me if there is any problem when using the library.

* srain@php.net
* twitter: https://twitter.com/liaohuqiu
* 微博: http://weibo.com/liaohuqiu
* QQ 群: 271918140
