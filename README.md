### GridView with Header and Footer

![Screen Shot](https://raw.githubusercontent.com/liaohuqiu/android-GridViewWithHeaderAndFooter/master/screen-shot.png)

#### Marven

```xml
<dependency>
    <groupId>in.srain.cube</groupId>
    <artifactId>grid-view-with-header-footer</artifactId>
    <type>jar</type>
    <version>1.0.3</version>
</dependency>
```

#### Gradle

``` groovy
compile 'in.srain.cube:grid-view-with-header-footer:1.0.3'
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