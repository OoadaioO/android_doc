# Android 编码规范

> **任何一个傻瓜都能写出计算机可以理解的代码。唯有写出人类容易理解的代码，才是优秀的程序员。     – Martin Flower**

<br>
团队协作项目，为了保持大家的代码一致性，进行一些代码格式的规范。

## 1. 基本要求
 -  代码缩进使用4个空格，不是Tab键。
 -  统一使用UTF-8编码，避免乱码问题。
 -  除了注释，代码中不出现中文。
 -  每个类写上必要的注释，类的说明，作者，修改时间，联系方式（可选）。
 -  为了让他人可以容易看懂你的代码，请在关键地方做好注释。
 -  变量和函数名命名使用“驼峰命名法”，资源相关文件命名使用“下划线命名法”。
 -  代码中用到的**字符串**、**颜色值**和**控件尺寸**等资源，都统一写到对应的xml文件中（strings.xml, colors.xml, values.xml），方便代码维护和今后的国际化支持。
 -  **强烈建议使用Android Studio或者Intellij IDEA。**
 -  **使用 Ctrl+Shift+F 来格式化代码， 使用 Ctrl+Shift+O 来格式化 Import 包。**

## 2. 项目架构
 -  基本遵循**MVP架构**（Model/View/Presenter），把数据源，用户界面和业务逻辑各个层次解耦，增加代码可读性和维护性，也增强了代码的扩展性。
 -  详细代码可参考[Google官方MVP架构示例][1]。

## 3. 分包管理
 -  按照组件类型来分包，而不是按业务模块来分包。业务有可能会变，但组件类型是基本不变的。另外，新加入的开发人员，对业务不熟悉，但对组件是很清楚的，理解快，入手也快。
 -  对于稍微大一点的项目，可以先按模块分包，在子模块中再按照组件类型分包。
 -  分包格式也可参考[Google官方MVP架构示例][1]。

        base:存放基础类的包，里面的类以Base为前缀，例如BaseActivity；
        activity:存放activity的包，每个activity命名以Activity结尾，例如MainActivity;
        fragment:存放fragment的包，每个fragment命名以Fragment结尾，例如ChatFragment;
        receiver:存放receiver的包；
        service:存放service的包；
        adapter:存放adapter的包，每个adapter命名以Adapter结尾，例如EventItemAdapter;
        common:存放一些公共常量，例如后端接口、SharedPreferenceKey、IntentExtra等;
        utils:存放工具类的包，比如常见的工具类：LogUtils、DateUtils；
        entity:存放实体类的包；
        widget:存放自定义View的包；

## 4. 命名规范

#### 包命名
 -  采用反域名命名规则，包名全部小写，连续的单词只是简单地连接起来，不使用下划线。
 -  一级包名为com，二级包名为xxx（可以是公司域名或者个人命名），三级包名根据应用进行命名，四级包名为模块名或层级名。如com.isa.crm.activity。

#### 类命名
 -  大驼峰命名。除常见的缩写单词以外，不使用缩写，缩写的单词每个字母都大写。
 -  公共的工具类建议以Utils、Manager为后缀，如LogUtils。接口命名遵循以上原则，以I为前缀，或以able或ible为后缀。

#### 变量命名

 - **成员变量命名**
   小驼峰命名。不推荐使用谷歌的前面加m的编码风格（如果使用团队中使用m，则统一使用）。

 - **临时变量命名**
   小驼峰命名。

 - **常量命名**
    单词每个字母均大写。单词之间下划线连接。

#### 方法命名
小驼峰命名。使用动词或动名词。

#### 资源文件命名

 - **布局文件命名**
    {组件\_功能}，下划线命名，全部小写。如：activity_login

 - **控件id命名**
    {控件\_范围\_功能}， 下划线命名，全部小写。如：et_login_password

 - **字符串id命名**
    {控件类型\_功能}， 如：btn_login
    页面标题，命名格式为：title_{页面}
    按钮文字，命名格式为：btn_{按钮事件}
    标签文字，命名格式为：label_{标签文字}
    选项卡文字，命名格式为：tab_{选项卡文字}
    消息框文字，命名格式为：toast_{消息}
    编辑框的提示文字，命名格式为：hint_{提示信息}
    图片的描述文字，命名格式为：desc_{图片文字}
    对话框的文字，命名格式为：dialog_{文字}
           
 - **图片资源命名**
    图标资源以ic为前缀，例如ic_chat，指聊天图标；
    背景图片以bg为前缀，例如bg_login，指的是登录页的背景图；
    按钮图片以btn为前缀，例如btn_login，指的是登录按钮的图片，不过这只有一种状态，需要加上状态的可以在后面添加，例如btn_login_pressed，表示登录按钮按下的图片；
    当使用shape和selector文件为背景或者按钮时，命名参照以上说明；
          

 - **动画文件命名**
    {动画类型\_动画方向}，下划线命名法，全部小写。如：fade_in


#### 常用控件缩写

控件 | 缩写
----|------
Linearlayout | ll
RelativeLayout | rl
TextView | tv
EditText | et
Button | btn
ImageButton | imgBtn
ImageView | iv
CheckBox | chb
ListView | lv
GridView | gv
ScrollView | sv
WebView | wv
ProgressBar | proBar
RadioButton | rb
Spinner | spn
           
     

## 其他

 1. 其他内容参见谷歌编码规范
	中文<http://blog.sina.com.cn/s/blog_48d491300100zwzg.html#use-todo-comments>
	英文<http://source.android.com/source/code-style.html>

 2. 其他未写明的欢迎补充，现有的有疑惑的欢迎提问，有缺点的欢迎质疑讨论修改。

<br><br><br><br>

# 新浪微博Android SDK Java代码规范 ##

代码规范的重要性不言而喻，但是一般公司都不太重视代码规范。在代码走读的时候，由于没有统一的规范，导致每个人都认为自己写的是对的。

在查看新浪微博Android SDK代码的时候，发现了个[codestyle包][2]。一个短小精悍的CodingRuler类却包含了比较全面的Java代码规范。

贴出来分享一下。当然，如果想要更详细的，写以查看 [Google Java Style][3]

 1. **weibo_android_sdk/demo-src/WeiboSDK/src/com/sina/weibo/sdk/codestyle/CodingRuler.java**

        /*
         * 文件名（可选），如 CodingRuler.java
         * 
         * 版本信息（可选），如：@version 1.0.0
         * 
         * 版权申明（开源代码一般都需要添加），如：Copyright (C) 2010-2013 SINA Corporation.
         */

        package com.sina.weibo.sdk.codestyle;

        /**
         * 类的大体描述放在这里。
         * 
         * <p>
         * <b>NOTE：以下部分为一个简要的编码规范，更多规范请参考 ORACLE 官方文档。</b><br>
         * 地址：http://www.oracle.com/technetwork/java/codeconventions-150003.pdf<br>
         * 另外，请使用 UTF-8 格式来查看代码，避免出现中文乱码。<br>
         * <b>至于注释应该使用中文还是英文，请自己行决定，根据公司或项目的要求而定，推荐使用英文。</b><br>
         * </p>
         * <h3>1. 整理代码</h3>
         * <ul>
         *    <li>1.1. Java 代码中不允许出现在警告，无法消除的警告要用 @SuppressWarnings。
         *    <li>1.2. 去掉无用的包、方法、变量等，减少僵尸代码。
         *    <li>1.3. 使用 Lint 工具来查看并消除警告和错误。
         *    <li>1.4. 使用 Ctrl+Shift+F 来格式化代码，然后再进行调整。
         *    <li>1.5. 使用 Ctrl+Shift+O 来格式化 Import 包。
         * </ul>
         * 
         * <h3>2. 命名规则</h3>
         *    <h3>2.1. 基本原则</h3>
         *    <ul>
         *         <li>2.1.1. 变量，方法，类命名要表义，严格禁止使用 name1, name2 等命名。
         *         <li>2.1.2. 命名不能太长，适当使用简写或缩写。（最好不要超过 25 个字母）
         *         <li>2.1.3. 方法名以小写字母开始，以后每个单词首字母大写。
         *         <li>2.1.4. 避免使用相似或者仅在大小写上有区别的名字。
         *         <li>2.1.5. 避免使用数字，但可用 2 代替 to，用 4 代替 for 等，如 go2Clean。
         *    </ul>
         *    
         *    <h3>2.2. 类、接口</h3>
         *    <ul>
         *         <li>2.2.1. 所有单词首字母都大写。使用能确切反应该类、接口含义、功能等的词。一般采用名词。
         *         <li>2.2.2. 接口带 I 前缀，或able, ible, er等后缀。如ISeriable。
         *    </ul>
         *    
         *    <h3>2.3. 字段、常量</h3>
         *    <ul>
         *         <li>2.3.1. 成员变量以 m 开头，静态变量以 s 开头，如 mUserName, sInstance。
         *         <li>2.3.2. 常量全部大写，在词与词之前用下划线连接，如 MAX_NUMBER。
         *         <li>2.3.3. 代码中禁止使用硬编码，把一些数字或字符串定义成常用量。
         *         <li>2.3.4. 对于废弃不用的函数，为了保持兼容性，通常添加 @Deprecated，如 {@link #doSomething()}
         *    </ul>
         *         
         * <h3>3. 注释</h3>
         *    请参考 {@link #SampleCode} 类的注释。
         *    <ul>
         *    <li>3.1. 常量注释，参见 {@link #ACTION_MAIN} 
         *    <li>3.2. 变量注释，参见 {@link #mObject0} 
         *    <li>3.3. 函数注释，参见 {@link #doSomething(int, float, String)}
         *    </ul> 
         *    
         * <h3>4. Class 内部顺序和逻辑</h3>
         * <ul>
         *    <li>4.1. 每个 class 都应该按照一定的逻辑结构来排列基成员变量、方法、内部类等，
         *             从而达到良好的可读性。
         *    <li>4.2. 总体上来说，要按照先 public, 后 protected, 最后 private, 函数的排布
         *             也应该有一个逻辑的先后顺序，由重到轻。
         *    <li>4.3. 以下顺序可供参考：
         *         定义 TAG，一般为 private（可选）<br>
         *         定义 public 常量<br>
         *         定义 private 常量、内部类<br>
         *         定义 private 变量<br>
         *         定义 public 方法<br>
         *         定义 protected 方法<br>
         *         定义 private 方法<br>
         * </ul>        
         * 
         * <h3>5. 表达式与语句</h3>
         *    <h3>5.1. 基本原则：采用紧凑型风格来编写代码</h3>
         *    <h3>5.2. 细则</h3>
         *    <ul>
         *         <li>5.2.1. 条件表示式，参见 {@link #conditionFun(boolean)} 
         *         <li>5.2.2. switch 语句，参见 {@link #switchFun(int)}
         *         <li>5.2.3. 循环语句，参见 {@link #circulationFun(boolean)}
         *         <li>5.2.4. 错误与异常，参见 {@link #exceptionFun()}
         *         <li>5.2.5. 杂项，参见 {@link #otherFun()}
         *         <li>5.2.6. 批注，参见 {@link #doSomething(int, float, String)}
         *    </ul>
         * 
         * @author 作者名
         * @since 2013-XX-XX
         */
        @SuppressWarnings("unused")
        public class CodingRuler {

        	/** 公有的常量注释 */
        	public static final String ACTION_MAIN = "android.intent.action.MAIN";

        	/** 私有的常量注释（同类型的常量可以分块并紧凑定义） */
        	private static final int MSG_AUTH_NONE    = 0;
        	private static final int MSG_AUTH_SUCCESS = 1;
        	private static final int MSG_AUTH_FAILED  = 2;

        	/** 保护的成员变量注释 */
        	protected Object mObject0;

        	/** 私有的成员变量 mObject1 注释（同类型的成员变量可以分块并紧凑定义） */
        	private Object mObject1;
        	/** 私有的成员变量 mObject2 注释 */
        	private Object mObject2;
        	/** 私有的成员变量 mObject3 注释 */
        	private Object mObject3;

        	/**
        	 * 对于注释多于一行的，采用这种方式来
        	 * 定义该变量
        	 */
        	private Object mObject4;

        	/**
        	 * 公有方法描述...
        	 * 
        	 * @param param1  参数1描述...
        	 * @param param2  参数2描述...
        	 * @param paramXX 参数XX描述... （注意：请将参数、描述都对齐）
        	 */
        	public void doSomething(int param1, float param2, String paramXX) {
                // 以下注释标签可以通过Eclipse内置的Task插件看到
                // TODO  使用TODO来标记代码，说明标识处有功能代码待编写
                // FIXME 使用FIXME来标记代码，说明标识处代码需要修正，甚至代码是
                //       错误的，不能工作，需要修复
                // XXX   使用XXX来标记代码，说明标识处代码虽然实现了功能，但是实现
                //       的方法有待商榷，希望将来能改进
        	}

        	/**
        	 * 保护方法描述...
        	 */
        	@Deprecated
        	protected void doSomething() {
                // ...implementation
        	}

        	/**
        	 * 私有方法描述...
        	 * 
        	 * @param param1  参数1描述...
        	 * @param param2  参数2描述...
        	 */
        	private void doSomethingInternal(int param1, float param2) {
                // ...implementation        
        	}

        	/**
        	 * 条件表达式原则。
        	 */
        	private void conditionFun() {
                boolean condition1 = true;
                boolean condition2 = false;
                boolean condition3 = false;
                boolean condition4 = false;
                boolean condition5 = false;
                boolean condition6 = false;

                // 原则： 1. 所有 if 语句必须用 {} 包括起来，即便只有一句，禁止使用不带{}的语句
                //       2. 在含有多种运算符的表达式中，使用圆括号来避免运算符优先级问题
                //       3. 判断条件很多时，请将其它条件换行
                if (condition1) {
                	// ...implementation
                }

                if (condition1) {
                	// ...implementation
                } else {
                	// ...implementation
                }

                if (condition1)          /* 禁止使用不带{}的语句 */
                	condition3 = true;

                if ((condition1 == condition2) 
                        || (condition3 == condition4)
                        || (condition5 == condition6)) {

                }
        	}

        	/**
        	 * Switch语句原则。
        	 */
        	private void switchFun() {

                // 原则： 1. switch 语句中，break 与下一条 case 之间，空一行
                //       2. 对于不需要 break 语句的，请使用 /* Falls through */来标注
                //       3. 请默认写上 default 语句，保持完整性
                int code = MSG_AUTH_SUCCESS;
                switch (code) {
                case MSG_AUTH_SUCCESS:
                	break;

                case MSG_AUTH_FAILED:
                	break;

                case MSG_AUTH_NONE:
                	/* Falls through */
                default:
                	break;
                }
        	}

        	/**
        	 * 循环表达式。
        	 */
        	private void circulationFun() {

                // 原则： 1. 尽量使用for each语句代替原始的for语句
                //       2. 循环中必须有终止循环的条件或语句，避免死循环
                //       3. 循环要尽可能的短, 把长循环的内容抽取到方法中去
                //       4. 嵌套层数不应超过3层, 要让循环清晰可读

                int array[] = { 1, 2, 3, 4, 5 };
                for (int data : array) {
                	// ...implementation
                }

                int length = array.length;
                for (int ix = 0; ix < length; ix++) {
                	// ...implementation
                }

                boolean condition = true;
                while (condition) {
                	// ...implementation
                }

                do {
                	// ...implementation
                } while (condition);
        	}

        	/**
        	 * 异常捕获原则。
        	 */
        	private void exceptionFun() {

                // 原则： 1. 捕捉异常是为了处理它，通常在异常catch块中输出异常信息。
                //       2. 资源释放的工作，可以放到 finally 块部分去做。如关闭 Cursor 等。
                try {
                	// ...implementation
                } catch (Exception e) {
                	e.printStackTrace();
                } finally {

                }
        	}

        	/**
        	 * 其它原则（整理中...）。
        	 */
        	private void otherFun() {
                // TODO
        	}    
        }

 2. **weibo_android_sdk/demo-src/WeiboSDK/src/com/sina/weibo/sdk/codestyle/SampleCode.java**

        /*
         * Copyright (C) 2010-2013 The SINA WEIBO Open Source Project
         *
         * Licensed under the Apache License, Version 2.0 (the "License");
         * you may not use this file except in compliance with the License.
         * You may obtain a copy of the License at
         *
         *      http://www.apache.org/licenses/LICENSE-2.0
         *
         * Unless required by applicable law or agreed to in writing, software
         * distributed under the License is distributed on an "AS IS" BASIS,
         * WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
         * See the License for the specific language governing permissions and
         * limitations under the License.
         */

        package com.sina.weibo.sdk.codestyle;

        /**
         * 类的大体描述放在这里。
         *         
         * @author 作者名
         * @since 2013-XX-XX
         */
        @SuppressWarnings("unused")
        public class SampleCode {

        	/** 公有的常量注释 */
        	public static final String ACTION_MAIN = "android.intent.action.MAIN";
        	
        	/** 私有的常量注释（同类型的常量可以分块并紧凑定义） */
        	private static final int MSG_AUTH_NONE    = 0;
        	private static final int MSG_AUTH_SUCCESS = 1;
        	private static final int MSG_AUTH_FAILED  = 2;
        	
        	/** 保护的成员变量注释 */
        	protected Object mObject0;
        	
        	/** 私有的成员变量 mObject1 注释（同类型的成员变量可以分块并紧凑定义） */
        	private Object mObject1;
        	/** 私有的成员变量 mObject2 注释 */
        	private Object mObject2;
        	/** 私有的成员变量 mObject3 注释 */
        	private Object mObject3;
        	
        	/**
        	 * 对于注释多于一行的，采用这种方式来
        	 * 定义该变量
        	 */
        	private Object mObject4;

        	/**
        	 * 公有方法描述...
        	 * 
        	 * @param param1  参数1描述...
        	 * @param param2  参数2描述...
        	 * @param paramXX 参数XX描述... （注意：请将参数、描述都对齐）
        	 */
        	public void doSomething(int param1, float param2, String paramXX) {
                // ...implementation
        	}
        	
        	/**
        	 * 保护方法描述...
        	 */
        	protected void doSomething() {
                // ...implementation        
        	}
        	
        	/**
        	 * 私有方法描述...
        	 * 
        	 * @param param1  参数1描述...
        	 * @param param2  参数2描述...
        	 */
        	private void doSomethingInternal(int param1, float param2) {
                // ...implementation        
        	}
        }


  [1]: https://github.com/googlesamples/android-architecture
  [2]: https://github.com/sinaweibosdk/weibo_android_sdk/tree/master/demo-src/WeiboSDK/src/com/sina/weibo/sdk/codestyle
  [3]: http://source.android.com/source/code-style.html