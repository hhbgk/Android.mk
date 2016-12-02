将NDK编译的第三方静态拷贝到JNI目录下,在Android.mk中添加如下代码

以openssl静态库（libcrypto-static.a）为例

第一种链接方法：LOCAL_LDFLAGS := libcrypto-static.a

第二种链接方法：LOCAL_LDLIBS := libcrypto-static.a

第三种链接方法：

include $(CLEAR_VARS)

LOCAL_MODULE := third_static_lib (可以随便起一个名字)

LOCAL_SRC_FILES := libcrypto-static.a

include $(PREBUILT_STATIC_LIBRARY)

//在你要编译的模块中引用third_static_lib

LOCAL_STATIC_LIBRARIES := third_static_lib

###refrence
[NDK 链接第三方静态库的方法](http://www.cnblogs.com/fengfeng/p/3272896.html)
