# Android ����淶

> **�κ�һ��ɵ�϶���д��������������Ĵ��롣Ψ��д�������������Ĵ��룬��������ĳ���Ա��     �C Martin Flower**

<br>
�Ŷ�Э����Ŀ��Ϊ�˱��ִ�ҵĴ���һ���ԣ�����һЩ�����ʽ�Ĺ淶��

## 1. ����Ҫ��
 -  ��������ʹ��4���ո񣬲���Tab����
 -  ͳһʹ��UTF-8���룬�����������⡣
 -  ����ע�ͣ������в��������ġ�
 -  ÿ����д�ϱ�Ҫ��ע�ͣ����˵�������ߣ��޸�ʱ�䣬��ϵ��ʽ����ѡ����
 -  Ϊ�������˿������׿�����Ĵ��룬���ڹؼ��ط�����ע�͡�
 -  �����ͺ���������ʹ�á��շ�������������Դ����ļ�����ʹ�á��»�������������
 -  �������õ���**�ַ���**��**��ɫֵ**��**�ؼ��ߴ�**����Դ����ͳһд����Ӧ��xml�ļ��У�strings.xml, colors.xml, values.xml�����������ά���ͽ��Ĺ��ʻ�֧�֡�
 -  **ǿ�ҽ���ʹ��Android Studio����Intellij IDEA��**
 -  **ʹ�� Ctrl+Shift+F ����ʽ�����룬 ʹ�� Ctrl+Shift+O ����ʽ�� Import ����**

## 2. ��Ŀ�ܹ�
 -  ������ѭ**MVP�ܹ�**��Model/View/Presenter����������Դ���û������ҵ���߼�������ν�����Ӵ���ɶ��Ժ�ά���ԣ�Ҳ��ǿ�˴������չ�ԡ�
 -  ��ϸ����ɲο�[Google�ٷ�MVP�ܹ�ʾ��][1]��

## 3. �ְ�����
 -  ��������������ְ��������ǰ�ҵ��ģ�����ְ���ҵ���п��ܻ�䣬����������ǻ�������ġ����⣬�¼���Ŀ�����Ա����ҵ����Ϥ����������Ǻ�����ģ����죬����Ҳ�졣
 -  ������΢��һ�����Ŀ�������Ȱ�ģ��ְ�������ģ�����ٰ���������ͷְ���
 -  �ְ���ʽҲ�ɲο�[Google�ٷ�MVP�ܹ�ʾ��][1]��

        base:��Ż�����İ������������BaseΪǰ׺������BaseActivity��
        activity:���activity�İ���ÿ��activity������Activity��β������MainActivity;
        fragment:���fragment�İ���ÿ��fragment������Fragment��β������ChatFragment;
        receiver:���receiver�İ���
        service:���service�İ���
        adapter:���adapter�İ���ÿ��adapter������Adapter��β������EventItemAdapter;
        common:���һЩ���������������˽ӿڡ�SharedPreferenceKey��IntentExtra��;
        utils:��Ź�����İ������糣���Ĺ����ࣺLogUtils��DateUtils��
        entity:���ʵ����İ���
        widget:����Զ���View�İ���

## 4. �����淶

#### ������
 -  ���÷������������򣬰���ȫ��Сд�������ĵ���ֻ�Ǽ򵥵�������������ʹ���»��ߡ�
 -  һ������Ϊcom����������Ϊxxx�������ǹ�˾�������߸�����������������������Ӧ�ý����������ļ�����Ϊģ������㼶������com.isa.crm.activity��

#### ������
 -  ���շ�����������������д�������⣬��ʹ����д����д�ĵ���ÿ����ĸ����д��
 -  �����Ĺ����ཨ����Utils��ManagerΪ��׺����LogUtils���ӿ�������ѭ����ԭ����IΪǰ׺������able��ibleΪ��׺��

#### ��������

 - **��Ա��������**
   С�շ����������Ƽ�ʹ�ùȸ��ǰ���m�ı��������ʹ���Ŷ���ʹ��m����ͳһʹ�ã���

 - **��ʱ��������**
   С�շ�������

 - **��������**
    ����ÿ����ĸ����д������֮���»������ӡ�

#### ��������
С�շ�������ʹ�ö��ʻ����ʡ�

#### ��Դ�ļ�����

 - **�����ļ�����**
    {���\_����}���»���������ȫ��Сд���磺activity_login

 - **�ؼ�id����**
    {�ؼ�\_��Χ\_����}�� �»���������ȫ��Сд���磺et_login_password

 - **�ַ���id����**
    {�ؼ�����\_����}�� �磺btn_login
    ҳ����⣬������ʽΪ��title_{ҳ��}
    ��ť���֣�������ʽΪ��btn_{��ť�¼�}
    ��ǩ���֣�������ʽΪ��label_{��ǩ����}
    ѡ����֣�������ʽΪ��tab_{ѡ�����}
    ��Ϣ�����֣�������ʽΪ��toast_{��Ϣ}
    �༭�����ʾ���֣�������ʽΪ��hint_{��ʾ��Ϣ}
    ͼƬ���������֣�������ʽΪ��desc_{ͼƬ����}
    �Ի�������֣�������ʽΪ��dialog_{����}
           
 - **ͼƬ��Դ����**
    ͼ����Դ��icΪǰ׺������ic_chat��ָ����ͼ�ꣻ
    ����ͼƬ��bgΪǰ׺������bg_login��ָ���ǵ�¼ҳ�ı���ͼ��
    ��ťͼƬ��btnΪǰ׺������btn_login��ָ���ǵ�¼��ť��ͼƬ��������ֻ��һ��״̬����Ҫ����״̬�Ŀ����ں�����ӣ�����btn_login_pressed����ʾ��¼��ť���µ�ͼƬ��
    ��ʹ��shape��selector�ļ�Ϊ�������߰�ťʱ��������������˵����
          

 - **�����ļ�����**
    {��������\_��������}���»�����������ȫ��Сд���磺fade_in


#### ���ÿؼ���д

�ؼ� | ��д
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
           
     

## ����

 1. �������ݲμ��ȸ����淶
	����<http://blog.sina.com.cn/s/blog_48d491300100zwzg.html#use-todo-comments>
	Ӣ��<http://source.android.com/source/code-style.html>

 2. ����δд���Ļ�ӭ���䣬���е����ɻ�Ļ�ӭ���ʣ���ȱ��Ļ�ӭ���������޸ġ�

<br><br><br><br>

# ����΢��Android SDK Java����淶 ##

����淶����Ҫ�Բ��Զ���������һ�㹫˾����̫���Ӵ���淶���ڴ����߶���ʱ������û��ͳһ�Ĺ淶������ÿ���˶���Ϊ�Լ�д���ǶԵġ�

�ڲ鿴����΢��Android SDK�����ʱ�򣬷����˸�[codestyle��][2]��һ����С������CodingRuler��ȴ�����˱Ƚ�ȫ���Java����淶��

����������һ�¡���Ȼ�������Ҫ����ϸ�ģ�д�Բ鿴 [Google Java Style][3]

 1. **weibo_android_sdk/demo-src/WeiboSDK/src/com/sina/weibo/sdk/codestyle/CodingRuler.java**

        /*
         * �ļ�������ѡ������ CodingRuler.java
         * 
         * �汾��Ϣ����ѡ�����磺@version 1.0.0
         * 
         * ��Ȩ��������Դ����һ�㶼��Ҫ��ӣ����磺Copyright (C) 2010-2013 SINA Corporation.
         */

        package com.sina.weibo.sdk.codestyle;

        /**
         * ��Ĵ��������������
         * 
         * <p>
         * <b>NOTE�����²���Ϊһ����Ҫ�ı���淶������淶��ο� ORACLE �ٷ��ĵ���</b><br>
         * ��ַ��http://www.oracle.com/technetwork/java/codeconventions-150003.pdf<br>
         * ���⣬��ʹ�� UTF-8 ��ʽ���鿴���룬��������������롣<br>
         * <b>����ע��Ӧ��ʹ�����Ļ���Ӣ�ģ����Լ��о��������ݹ�˾����Ŀ��Ҫ��������Ƽ�ʹ��Ӣ�ġ�</b><br>
         * </p>
         * <h3>1. �������</h3>
         * <ul>
         *    <li>1.1. Java �����в���������ھ��棬�޷������ľ���Ҫ�� @SuppressWarnings��
         *    <li>1.2. ȥ�����õİ��������������ȣ����ٽ�ʬ���롣
         *    <li>1.3. ʹ�� Lint �������鿴����������ʹ���
         *    <li>1.4. ʹ�� Ctrl+Shift+F ����ʽ�����룬Ȼ���ٽ��е�����
         *    <li>1.5. ʹ�� Ctrl+Shift+O ����ʽ�� Import ����
         * </ul>
         * 
         * <h3>2. ��������</h3>
         *    <h3>2.1. ����ԭ��</h3>
         *    <ul>
         *         <li>2.1.1. ������������������Ҫ���壬�ϸ��ֹʹ�� name1, name2 ��������
         *         <li>2.1.2. ��������̫�����ʵ�ʹ�ü�д����д������ò�Ҫ���� 25 ����ĸ��
         *         <li>2.1.3. ��������Сд��ĸ��ʼ���Ժ�ÿ����������ĸ��д��
         *         <li>2.1.4. ����ʹ�����ƻ��߽��ڴ�Сд������������֡�
         *         <li>2.1.5. ����ʹ�����֣������� 2 ���� to���� 4 ���� for �ȣ��� go2Clean��
         *    </ul>
         *    
         *    <h3>2.2. �ࡢ�ӿ�</h3>
         *    <ul>
         *         <li>2.2.1. ���е�������ĸ����д��ʹ����ȷ�з�Ӧ���ࡢ�ӿں��塢���ܵȵĴʡ�һ��������ʡ�
         *         <li>2.2.2. �ӿڴ� I ǰ׺����able, ible, er�Ⱥ�׺����ISeriable��
         *    </ul>
         *    
         *    <h3>2.3. �ֶΡ�����</h3>
         *    <ul>
         *         <li>2.3.1. ��Ա������ m ��ͷ����̬������ s ��ͷ���� mUserName, sInstance��
         *         <li>2.3.2. ����ȫ����д���ڴ����֮ǰ���»������ӣ��� MAX_NUMBER��
         *         <li>2.3.3. �����н�ֹʹ��Ӳ���룬��һЩ���ֻ��ַ�������ɳ�������
         *         <li>2.3.4. ���ڷ������õĺ�����Ϊ�˱��ּ����ԣ�ͨ����� @Deprecated���� {@link #doSomething()}
         *    </ul>
         *         
         * <h3>3. ע��</h3>
         *    ��ο� {@link #SampleCode} ���ע�͡�
         *    <ul>
         *    <li>3.1. ����ע�ͣ��μ� {@link #ACTION_MAIN} 
         *    <li>3.2. ����ע�ͣ��μ� {@link #mObject0} 
         *    <li>3.3. ����ע�ͣ��μ� {@link #doSomething(int, float, String)}
         *    </ul> 
         *    
         * <h3>4. Class �ڲ�˳����߼�</h3>
         * <ul>
         *    <li>4.1. ÿ�� class ��Ӧ�ð���һ�����߼��ṹ�����л���Ա�������������ڲ���ȣ�
         *             �Ӷ��ﵽ���õĿɶ��ԡ�
         *    <li>4.2. ��������˵��Ҫ������ public, �� protected, ��� private, �������Ų�
         *             ҲӦ����һ���߼����Ⱥ�˳�����ص��ᡣ
         *    <li>4.3. ����˳��ɹ��ο���
         *         ���� TAG��һ��Ϊ private����ѡ��<br>
         *         ���� public ����<br>
         *         ���� private �������ڲ���<br>
         *         ���� private ����<br>
         *         ���� public ����<br>
         *         ���� protected ����<br>
         *         ���� private ����<br>
         * </ul>        
         * 
         * <h3>5. ���ʽ�����</h3>
         *    <h3>5.1. ����ԭ�򣺲��ý����ͷ������д����</h3>
         *    <h3>5.2. ϸ��</h3>
         *    <ul>
         *         <li>5.2.1. ������ʾʽ���μ� {@link #conditionFun(boolean)} 
         *         <li>5.2.2. switch ��䣬�μ� {@link #switchFun(int)}
         *         <li>5.2.3. ѭ����䣬�μ� {@link #circulationFun(boolean)}
         *         <li>5.2.4. �������쳣���μ� {@link #exceptionFun()}
         *         <li>5.2.5. ����μ� {@link #otherFun()}
         *         <li>5.2.6. ��ע���μ� {@link #doSomething(int, float, String)}
         *    </ul>
         * 
         * @author ������
         * @since 2013-XX-XX
         */
        @SuppressWarnings("unused")
        public class CodingRuler {

        	/** ���еĳ���ע�� */
        	public static final String ACTION_MAIN = "android.intent.action.MAIN";

        	/** ˽�еĳ���ע�ͣ�ͬ���͵ĳ������Էֿ鲢���ն��壩 */
        	private static final int MSG_AUTH_NONE    = 0;
        	private static final int MSG_AUTH_SUCCESS = 1;
        	private static final int MSG_AUTH_FAILED  = 2;

        	/** �����ĳ�Ա����ע�� */
        	protected Object mObject0;

        	/** ˽�еĳ�Ա���� mObject1 ע�ͣ�ͬ���͵ĳ�Ա�������Էֿ鲢���ն��壩 */
        	private Object mObject1;
        	/** ˽�еĳ�Ա���� mObject2 ע�� */
        	private Object mObject2;
        	/** ˽�еĳ�Ա���� mObject3 ע�� */
        	private Object mObject3;

        	/**
        	 * ����ע�Ͷ���һ�еģ��������ַ�ʽ��
        	 * ����ñ���
        	 */
        	private Object mObject4;

        	/**
        	 * ���з�������...
        	 * 
        	 * @param param1  ����1����...
        	 * @param param2  ����2����...
        	 * @param paramXX ����XX����... ��ע�⣺�뽫���������������룩
        	 */
        	public void doSomething(int param1, float param2, String paramXX) {
                // ����ע�ͱ�ǩ����ͨ��Eclipse���õ�Task�������
                // TODO  ʹ��TODO����Ǵ��룬˵����ʶ���й��ܴ������д
                // FIXME ʹ��FIXME����Ǵ��룬˵����ʶ��������Ҫ����������������
                //       ����ģ����ܹ�������Ҫ�޸�
                // XXX   ʹ��XXX����Ǵ��룬˵����ʶ��������Ȼʵ���˹��ܣ�����ʵ��
                //       �ķ����д���ȶ��ϣ�������ܸĽ�
        	}

        	/**
        	 * ������������...
        	 */
        	@Deprecated
        	protected void doSomething() {
                // ...implementation
        	}

        	/**
        	 * ˽�з�������...
        	 * 
        	 * @param param1  ����1����...
        	 * @param param2  ����2����...
        	 */
        	private void doSomethingInternal(int param1, float param2) {
                // ...implementation        
        	}

        	/**
        	 * �������ʽԭ��
        	 */
        	private void conditionFun() {
                boolean condition1 = true;
                boolean condition2 = false;
                boolean condition3 = false;
                boolean condition4 = false;
                boolean condition5 = false;
                boolean condition6 = false;

                // ԭ�� 1. ���� if �������� {} ��������������ֻ��һ�䣬��ֹʹ�ò���{}�����
                //       2. �ں��ж���������ı��ʽ�У�ʹ��Բ������������������ȼ�����
                //       3. �ж������ܶ�ʱ���뽫������������
                if (condition1) {
                	// ...implementation
                }

                if (condition1) {
                	// ...implementation
                } else {
                	// ...implementation
                }

                if (condition1)          /* ��ֹʹ�ò���{}����� */
                	condition3 = true;

                if ((condition1 == condition2) 
                        || (condition3 == condition4)
                        || (condition5 == condition6)) {

                }
        	}

        	/**
        	 * Switch���ԭ��
        	 */
        	private void switchFun() {

                // ԭ�� 1. switch ����У�break ����һ�� case ֮�䣬��һ��
                //       2. ���ڲ���Ҫ break ���ģ���ʹ�� /* Falls through */����ע
                //       3. ��Ĭ��д�� default ��䣬����������
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
        	 * ѭ�����ʽ��
        	 */
        	private void circulationFun() {

                // ԭ�� 1. ����ʹ��for each������ԭʼ��for���
                //       2. ѭ���б�������ֹѭ������������䣬������ѭ��
                //       3. ѭ��Ҫ�����ܵĶ�, �ѳ�ѭ�������ݳ�ȡ��������ȥ
                //       4. Ƕ�ײ�����Ӧ����3��, Ҫ��ѭ�������ɶ�

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
        	 * �쳣����ԭ��
        	 */
        	private void exceptionFun() {

                // ԭ�� 1. ��׽�쳣��Ϊ�˴�������ͨ�����쳣catch��������쳣��Ϣ��
                //       2. ��Դ�ͷŵĹ��������Էŵ� finally �鲿��ȥ������ر� Cursor �ȡ�
                try {
                	// ...implementation
                } catch (Exception e) {
                	e.printStackTrace();
                } finally {

                }
        	}

        	/**
        	 * ����ԭ��������...����
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
         * ��Ĵ��������������
         *         
         * @author ������
         * @since 2013-XX-XX
         */
        @SuppressWarnings("unused")
        public class SampleCode {

        	/** ���еĳ���ע�� */
        	public static final String ACTION_MAIN = "android.intent.action.MAIN";
        	
        	/** ˽�еĳ���ע�ͣ�ͬ���͵ĳ������Էֿ鲢���ն��壩 */
        	private static final int MSG_AUTH_NONE    = 0;
        	private static final int MSG_AUTH_SUCCESS = 1;
        	private static final int MSG_AUTH_FAILED  = 2;
        	
        	/** �����ĳ�Ա����ע�� */
        	protected Object mObject0;
        	
        	/** ˽�еĳ�Ա���� mObject1 ע�ͣ�ͬ���͵ĳ�Ա�������Էֿ鲢���ն��壩 */
        	private Object mObject1;
        	/** ˽�еĳ�Ա���� mObject2 ע�� */
        	private Object mObject2;
        	/** ˽�еĳ�Ա���� mObject3 ע�� */
        	private Object mObject3;
        	
        	/**
        	 * ����ע�Ͷ���һ�еģ��������ַ�ʽ��
        	 * ����ñ���
        	 */
        	private Object mObject4;

        	/**
        	 * ���з�������...
        	 * 
        	 * @param param1  ����1����...
        	 * @param param2  ����2����...
        	 * @param paramXX ����XX����... ��ע�⣺�뽫���������������룩
        	 */
        	public void doSomething(int param1, float param2, String paramXX) {
                // ...implementation
        	}
        	
        	/**
        	 * ������������...
        	 */
        	protected void doSomething() {
                // ...implementation        
        	}
        	
        	/**
        	 * ˽�з�������...
        	 * 
        	 * @param param1  ����1����...
        	 * @param param2  ����2����...
        	 */
        	private void doSomethingInternal(int param1, float param2) {
                // ...implementation        
        	}
        }


  [1]: https://github.com/googlesamples/android-architecture
  [2]: https://github.com/sinaweibosdk/weibo_android_sdk/tree/master/demo-src/WeiboSDK/src/com/sina/weibo/sdk/codestyle
  [3]: http://source.android.com/source/code-style.html