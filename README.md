# MyRealTimeBlurView
[![skin-support](https://img.shields.io/badge/release-v1.0.0-green.svg)](http://jcenter.bintray.com/skin/support)

## 介绍

MyRealTimeBlurView: 高斯模糊动态化处理：

## 用法

   ### 导入:

Add it in your root build.gradle at the end of repositories:
```xml
allprojects {
    repositories {
       ...
       maven { url 'https://jitpack.io' }
    }
}
```
Add the dependency
```xml
dependencies {
    implementation 'com.github.colinlibrary:MyRealTimeBlurView:1.0.0'
}
```

Add app gradle
```xml
    defaultConfig {
        ...
        renderscriptTargetApi 19
        renderscriptSupportModeEnabled true
    }
```

Add proguard rules if necessary:
```xml
   -keep class android.support.v8.renderscript.** { *; }
   -keep class androidx.renderscript.** { *; }
```

### 使用:
 
布局中引入即可实现动态话效果  
```java
  <com.colin.library.widget.RealtimeBlurView
     android:id="@+id/blur_view"
     android:layout_width="match_parent"
     android:layout_height="match_parent"/>
   
  当然你也可以 选择初始值
  	<declare-styleable name="RealtimeBlurView">
		<attr name="realtimeBlurRadius" format="dimension"/>
		<attr name="realtimeDownsampleFactor" format="float"/>
		<attr name="realtimeOverlayColor" format="color"/>
	</declare-styleable>
```
同样的代码你也可以动态的去改变 这些值
```java
   public void setBlurRadius(float radius) {
		...
	}

	public void setDownsampleFactor(float factor) {
		...
	}

	public void setOverlayColor(int color) {
		...
	}
```

