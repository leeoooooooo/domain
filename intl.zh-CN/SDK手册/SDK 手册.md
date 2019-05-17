# SDK 手册 {#concept_hlx_jsw_b2b .concept}

目前，阿里云官方提供的 SDK 分4种语言版本，分别为 Java、Python、PHP、C\#。每个版本的下载安装和使用方法如下：

-   [Java](https://www.alibabacloud.com/support/developer-resources)
-   [Python](https://www.alibabacloud.com/support/developer-resources)
-   [PHP](https://www.alibabacloud.com/support/developer-resources)
-   [C\#](https://www.alibabacloud.com/support/developer-resources)

更多语言版本的 SDK，您可以前往第三方 SDK 服务中进行选择。

## 快速入门 {#section_fzb_ptw_b2b .section}

以Java为例，SDK可以通过如下方式安装和使用：

1.  在阿里云官网创建并管理你的AccessKey。
2.  通过maven安装SDK。
    1.  添加maven库。

        ```
        <repositories>
             <repository>
                 <id>sonatype-nexus-staging</id>
                 <name>Sonatype Nexus Staging</name>
                 <url>https://oss.sonatype.org/service/local/staging/deploy/maven2/</url>
                 <releases>
                     <enabled>true</enabled>
                 </releases>
                 <snapshots>
                     <enabled>true</enabled>
                 </snapshots>
             </repository>
        </repositories>
        ```

    2.  添加jar包依赖。

        ```
        <dependency>
         <groupId>com.aliyun</groupId>
         <artifactId>aliyun-java-sdk-domain-intl</artifactId>
             <version>1.0.0</version>
        </dependency>
        <dependency>
         <groupId>com.aliyun</groupId>
         <artifactId>aliyun-java-sdk-core</artifactId>
             <version>3.5.0</version>
        </dependency>
        ```

    3.  示例代码。下面以批量提交域名注册任务为示例：

        ```
        import java.util.ArrayList;
        import com.aliyuncs.DefaultAcsClient;
        import com.aliyuncs.IAcsClient;
        import com.aliyuncs.domain_intl.model.v20171218.SaveBatchTaskForCreatingOrderActivateRequest;
        import com.aliyuncs.domain_intl.model.v20171218.SaveBatchTaskForCreatingOrderActivateRequest.OrderActivateParam;
        import com.aliyuncs.domain_intl.model.v20171218.SaveBatchTaskForCreatingOrderActivateResponse;
        import com.aliyuncs.exceptions.ClientException;
        import com.aliyuncs.exceptions.ServerException;
        import com.aliyuncs.profile.DefaultProfile;
        import com.aliyuncs.profile.IClientProfile;
        public class DomainSdkDemo {
            private static IAcsClient client = null;
            //初始化client
            static {
                String regionId = "ap-southeast-1"; //域名SDK请使用固定值"ap-southeast-1"
                String accessKeyId = ""; // your accessKey
                String accessKeySecret = "";// your accessSecret
                IClientProfile profile = DefaultProfile.getProfile(regionId, accessKeyId, accessKeySecret);
                // 若报Can not find endpoint to access异常，请添加以下此行代码
                // DefaultProfile.addEndpoint("ap-southeast-1", "ap-southeast-1", "Domain-intl", "domain-intl.aliyuncs.com");
                client = new DefaultAcsClient(profile);
            }
            public static void main(String[] args) {
                //初始化请求
                SaveBatchTaskForCreatingOrderActivateRequest request = new SaveBatchTaskForCreatingOrderActivateRequest();
                // request.setProtocol(ProtocolType.HTTPS); //指定访问协议
                // request.setAcceptFormat(FormatType.JSON); //指定api返回格式
                // request.setMethod(MethodType.POST); //指定请求方法
                ArrayList<OrderActivateParam> list = new ArrayList<OrderActivateParam>();
                OrderActivateParam orderActivateParam = new OrderActivateParam();
                orderActivateParam.setDomainName("yourdomain.com");
                orderActivateParam.setRegistrantProfileId(0L);
                orderActivateParam.setEnableDomainProxy(false);
                orderActivateParam.setSubscriptionDuration(1);
                orderActivateParam.setPermitPremiumActivation(false);
                list.add(orderActivateParam);
                request.setOrderActivateParams(list);
                //发起api调用并解析结果
                try {
                    //IAcsClient提供了两种类型的调用结果返回, 一种方式是通过调用doAction方法获取取得原始的api调用结果, 即返回HttpResponse类型的结果. 示例代码如下：
                    //HttpResponse httpResponse = client.doAction(describeCdnServiceRequest);
                    //System.out.println(httpResponse.getUrl());
                    //System.out.println(new String(httpResponse.getContent()));
                    //另一种方式, 通过调用getAcsResponse方法, 获取反序列化后的对象, 示例代码如下:
                    SaveBatchTaskForCreatingOrderActivateResponse response = client.getAcsResponse(request);
                    System.out.println(response.getTaskNo());
                } catch (ServerException e) {
                    e.printStackTrace();
                } catch (ClientException e) {
                    e.printStackTrace();
                }
            }
        }
        ```


