欢迎使用 COS（对象存储服务） API 文档参考指南。本指南介绍了 COS 应用程序编程接口（API）。文档中详细描述了各个 API 接口的相关请求和响应结构以及错误代码。


当您在查看 API 文档之前，请先阅读以下有关身份验证和访问控制的相关信息。

您可以使用被认证或者匿名的账号请求访问 COS（对象存储服务）。通过被认证的请求时，需要有 COS 可以用来验证您的请求的凭证。当您的代码直接调用 REST API 调用时，您可以使用有效凭证创建签名，并且每次访问请求中都包含您的签名。有关各种身份验证方法和签名计算的信息，请参阅[验证请求]()。

直接从您的代码进行 REST API 调用可能很麻烦。它需要你编写必要的代码来计算一个有效的签名来验证您的请求。我们推荐以下替代方案供您选择：



- 使用 COS SDK发送您的请求（请参阅[示例代码库]()）。使用此选项，您不需要编写代码来计算请求身份验证的签名，因为 SDK 客户端通过使用您提供的访问密钥来验证您的请求。如有您选择接受，那么系统将默认使用SDK。


- 使用 COS CLI 进行 COS API调用 。有关 COS CLI 如何设置和 COS 的命令示例请参阅以下指南：

请在 COS 对象存储服务开发指南。[设置 COS CLI]()

请在 COS 命令行界面用户指南使用 [COS命令行接口]()

您可以使用有效的凭据来验证您的请求，您必须拥有权限，否则将无法创建或访问 COS 资源。例如，您必须具有创建 COS 存储桶或从存储桶中获取对象的权限。如果使用 COS 帐户的根凭据，则拥有所有权限。但是，不推荐使用根凭证。相反，我们建议您在帐户中创建 IAM 用户并管理用户权限。有关详细信息，请参阅 “ COS 开发人员指南”中的[管理 COS 资源的访问权限]()。