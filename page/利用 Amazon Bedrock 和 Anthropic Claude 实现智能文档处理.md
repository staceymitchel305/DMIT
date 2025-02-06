# 利用 Amazon Bedrock 和 Anthropic Claude 实现智能文档处理

本文将指导您如何使用 Amazon Bedrock 平台上的 **Anthropic Claude 3 Sonnet** 模型构建智能文档处理（IDP）解决方案。我们将逐步演示如何从扫描文档中提取数据，并将其存储到数据库中。

## 关键功能与优势

生成式 AI 不仅推动了创意生成、内容创作和客户服务的创新，还通过自动化流程显著提升了工作效率。**Amazon Bedrock** 作为一项完全托管的服务，集成了包括 Anthropic、Cohere、Meta 等领先 AI 公司的基础模型，为开发者提供了安全、高效的 AI 应用开发平台。

### 生成式 AI 在 IDP 中的应用

- **高级文档理解**：自动识别和提取非结构化文本中的关键信息。
- **高效数据提取**：以结构化格式（如 JSON）输出提取的数据。
- **自动化文档分类**：自动为文档打标签，方便后续检索。
- **无缝信息检索**：快速从大量文档中找到所需数据。

通过结合生成式 AI 和传统 IDP 技术，企业可以实现文档处理流程的高度自动化和可靠性，从而提升生产效率、降低成本并优化决策能力。

👉 [WildCard | 一分钟注册，轻松订阅海外线上服务](https://bbtdd.com/WildCard)

## 解决方案架构

该解决方案基于 Amazon Bedrock 和 Anthropic Claude 3 Sonnet 模型构建，结合了多种亚马逊云科技服务，确保高效、准确地处理扫描文档。

### 架构流程图

![解决方案架构](https://bbtdd.com/img/497491423251245.webp)

### 实施步骤

1. **文档上传**：将扫描文档上传至 **Amazon S3** 存储桶，触发 S3 事件通知。
2. **模型调用**：通过 **AWS Lambda** 调用 Anthropic Claude 3 Sonnet 模型，处理文档并提取数据。
3. **数据提取**：模型以 JSON 格式提取文档中的结构化数据。
4. **消息队列**：提取的数据被发送至 **Amazon SQS** 队列，作为缓冲区以确保系统可扩展性和容错能力。
5. **数据存储**：另一项 Lambda 服务从 SQS 队列中获取数据，并将其存储到 **Amazon DynamoDB** 表中。

## 核心技术与服务

- **Amazon Bedrock**：提供完全托管的生成式 AI 服务，支持调用多种基础模型。
- **Anthropic Claude 3 系列**：包括 Opus、Sonnet 和 Haiku 三个版本，适用于多种智能任务。
- **Amazon DynamoDB**：无服务器的 NoSQL 数据库，支持高并发数据处理。
- **AWS Lambda**：无需管理服务器的计算服务，支持事件驱动的代码执行。
- **Amazon SQS**：完全托管的消息队列服务，确保系统间的可靠通信。
- **Amazon S3**：高度可扩展的对象存储服务，适用于海量数据存储。

## 用例：政府机构出生证明处理

以州政府机构处理出生证明申请为例，传统的手动提取方式耗时且容易出错。通过本文的解决方案，可以自动化处理非英语（如西班牙语）申请表，显著提升效率。

### 实施步骤

1. **创建 S3 存储桶**：上传扫描的出生证明申请表。
2. **创建 SQS 队列**：用于缓冲提取的数据。
3. **配置 Lambda 服务**：调用 Claude 3 模型提取数据并存储至 DynamoDB。
4. **测试解决方案**：上传文档并验证 DynamoDB 中的数据。

## 提示词优化与模型调用

提示词在生成式 AI 应用中至关重要，精心设计的提示词可以提高模型输出的准确性和一致性。以下是用于 JSON 格式输出的提示词示例：

python
prompt = """
This image shows a birth certificate application form. 
Please precisely copy all the relevant information from the form.
Leave the field blank if there is no information in corresponding field.
If the image is not a birth certificate application form, simply return an empty JSON object. 
If the application form is not filled, leave the fees attributes blank. 
Translate any non-English text to English. 
Organize and return the extracted data in a JSON format with the following keys:
{
    "applicantDetails":{
        "applicantName": "",
        "dayPhoneNumber": "",
        "address": "",
        "city": "",
        "state": "",
        "zipCode": "",
        "email":""
    },
    "mailingAddress":{
        "mailingAddressApplicantName": "",
        "mailingAddress": "",
        "mailingAddressCity": "",
        "mailingAddressState": "",
        "mailingAddressZipCode": ""
    },
    "relationToApplicant":[""],
    "purposeOfRequest": "",
    "BirthCertificateDetails":
    {
        "nameOnBirthCertificate": "",
        "dateOfBirth": "",
        "sex": "",
        "cityOfBirth": "",
        "countyOfBirth": "",
        "mothersMaidenName": "",
        "fathersName": "",
        "mothersPlaceOfBirth": "",
        "fathersPlaceOfBirth": "",
        "parentsMarriedAtBirth": "",
        "numberOfChildrenBornInSCToMother": "",
        "diffNameAtBirth":""
    },
    "fees":{
        "searchFee": "",
        "eachAdditionalCopy": "",
        "expediteFee": "",
        "totalFees": ""
    } 
  }
"""


## 总结

本文展示了如何利用 **Amazon Bedrock** 和 **Anthropic Claude 3 Sonnet** 构建智能文档处理解决方案。通过整合亚马逊云科技的无服务器架构和 Claude 3 的多模态能力，企业可以实现文档处理流程的高度自动化，提升运营效率并降低成本。

👉 [WildCard | 一分钟注册，轻松订阅海外线上服务](https://bbtdd.com/WildCard)