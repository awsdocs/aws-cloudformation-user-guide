# Amazon Simple Notification Service\-backed custom resources<a name="template-custom-resources-sns"></a>

When you associate an Amazon SNS topic with a custom resource, you use Amazon SNS notifications to trigger custom provisioning logic\. With custom resources and Amazon SNS, you can enable scenarios such as adding new resources to a stack and injecting dynamic data into a stack\. For example, when you create a stack, AWS CloudFormation can send a `create` request to a topic that's monitored by an application that's running on an Amazon Elastic Compute Cloud instance\. The Amazon SNS notification triggers the application to carry out additional provisioning tasks, such as retrieve a pool of white\-listed Elastic IPs\. After it's done, the application sends a response \(and any output data\) that notifies AWS CloudFormation to proceed with the stack operation\.

## Walkthrough: Using Amazon Simple Notification Service to create custom resources<a name="walkthrough-custom-resources-sns-adding-nonaws-resource"></a>

This walkthrough will step through the custom resource process, explaining the sequence of events and messages sent and received as a result of custom resource stack creation, updates, and deletion\.

### Step 1: Stack creation<a name="crpg-walkthrough-stack-creation"></a>

1. <a name="crpg-walkthrough-stack-creation-customer-template"></a>The template developer creates an AWS CloudFormation stack that contains a custom resource; in the template example below, we use the custom resource type name `Custom::SeleniumTester` for the custom resource `MySeleniumTest`\. 

   The custom resource type is declared with a *service token*, optional *provider\-specific properties*, and optional [`Fn::GetAtt`](intrinsic-function-reference-getatt.md) attributes that are defined by the custom resource provider\. These properties and attributes can be used to pass information from the template developer to the custom resource provider and vice\-versa\. Custom resource type names must be alphanumeric and can have a maximum length of 60 characters\.

   The following example shows a template that has both custom properties and return attributes:

   ```
   {
      "AWSTemplateFormatVersion" : "2010-09-09",
      "Resources" : {
         "MySeleniumTest" : {
            "Type": "Custom::SeleniumTester",
            "Version" : "1.0",
            "Properties" : {
               "ServiceToken": "arn:aws:sns:us-west-2:123456789012:CRTest",
               "seleniumTester" : "SeleniumTest()",
               "endpoints" : [ "http://mysite.com", "http://myecommercesite.com/", "http://search.mysite.com" ],
               "frequencyOfTestsPerHour" : [ "3", "2", "4" ]
            }
         }
      },
      "Outputs" : {
         "topItem" : {
            "Value" : { "Fn::GetAtt" : ["MySeleniumTest", "resultsPage"] }
         },
         "numRespondents" : {
            "Value" : { "Fn::GetAtt" : ["MySeleniumTest", "lastUpdate"] }
         }
      }
   }
   ```
**Note**  
The names and values of the data accessed with `Fn::GetAtt` are returned by the custom resource provider during the provider's response to AWS CloudFormation\. If the custom resource provider is a third\-party, then the template developer must obtain the names of these return values from the custom resource provider\.

1. <a name="crpg-walkthrough-stack-creation-provider-request"></a>AWS CloudFormation sends an Amazon SNS notification to the resource provider with a `"RequestType" : "Create"` that contains information about the stack, the custom resource properties from the stack template, and an S3 URL for the response\. 

   The SNS topic that is used to send the notification is embedded in the template in the `ServiceToken` property\. To avoid using a hard\-coded value, a template developer can use a template parameter so that the value is entered at the time the stack is launched\.

   The following example shows a custom resource `Create` request which includes a custom resource type name, `Custom::SeleniumTester`, created with a `LogicalResourceId` of `MySeleniumTester`: 

   ```
   {
      "RequestType" : "Create",
      "ResponseURL" : "http://pre-signed-S3-url-for-response",
      "StackId" : "arn:aws:cloudformation:us-west-2:123456789012:stack/stack-name/guid",
      "RequestId" : "unique id for this create request",
      "ResourceType" : "Custom::SeleniumTester",
      "LogicalResourceId" : "MySeleniumTester",
      "ResourceProperties" : {
         "seleniumTester" : "SeleniumTest()",
         "endpoints" : [ "http://mysite.com", "http://myecommercesite.com/", "http://search.mysite.com" ],
         "frequencyOfTestsPerHour" : [ "3", "2", "4" ]
      }
   }
   ```

1. <a name="crpg-walkthrough-stack-creation-provider-response"></a>The custom resource provider processes the data sent by the template developer and determines whether the `Create` request was successful\. The resource provider then uses the S3 URL sent by AWS CloudFormation to send a response of either `SUCCESS` or `FAILED`\. 

   Depending on the response type, different response fields will be expected by AWS CloudFormation\. Refer to the Responses section in the reference topic for the RequestType that is being processed\. 

   In response to a create or update request, the custom resource provider can return data elements in the [Data](crpg-ref-responses.md#crpg-ref-responses-data) field of the response\. These are name/value pairs, and the *names* correspond to the `Fn::GetAtt` attributes used with the custom resource in the stack template\. The *values* are the data that is returned when the template developer calls `Fn::GetAtt` on the resource with the attribute name\.

   The following is an example of a custom resource response:

   ```
   {
      "Status" : "SUCCESS",
      "PhysicalResourceId" : "Tester1",
      "StackId" : "arn:aws:cloudformation:us-west-2:123456789012:stack/stack-name/guid",
      "RequestId" : "unique id for this create request",
      "LogicalResourceId" : "MySeleniumTester",
      "Data" : {
         "resultsPage" : "http://www.myexampledomain/test-results/guid",
         "lastUpdate" : "2012-11-14T03:30Z",
      }
   }
   ```

   The `StackId`, `RequestId`, and `LogicalResourceId` fields must be copied verbatim from the request\.

1. <a name="crpg-walkthrough-stack-creation-stack-status"></a> AWS CloudFormation declares the stack status as `CREATE_COMPLETE` or `CREATE_FAILED`\. If the stack was successfully created, the template developer can use the output values of the created custom resource by accessing them with [`Fn::GetAtt`](intrinsic-function-reference-getatt.md)\.

   For example, the custom resource template used for illustration used `Fn::GetAtt` to copy resource outputs into the stack outputs:

   ```
   "Outputs" : {
      "topItem" : {
         "Value" : { "Fn::GetAtt" : ["MySeleniumTest", "resultsPage"] }
      },
      "numRespondents" : {
         "Value" : { "Fn::GetAtt" : ["MySeleniumTest", "lastUpdate"] }
      }
   }
   ```

For detailed information about the request and response objects involved in `Create` requests, see [Create](crpg-ref-requesttypes-create.md) in the [Custom Resource Reference](crpg-ref.md)\.

### Step 2: Stack updates<a name="crpg-walkthrough-stack-updates"></a>

To update an existing stack, you must submit a template that specifies updates for the properties of resources in the stack, as shown in the example below\. AWS CloudFormation updates only the resources that have changes specified in the template\. For more information about updating stacks, see [AWS CloudFormation stack updates](using-cfn-updating-stacks.md)\.

You can update custom resources that require a replacement of the underlying physical resource\. When you update a custom resource in an AWS CloudFormation template, AWS CloudFormation sends an update request to that custom resource\. If a custom resource requires a replacement, the new custom resource must send a response with the new physical ID\. When AWS CloudFormation receives the response, it compares the `PhysicalResourceId` between the old and new custom resources\. If they are different, AWS CloudFormation recognizes the update as a replacement and sends a delete request to the old resource, as shown in [Step 3: Stack deletion](#crpg-walkthrough-stack-deletion)\. 

**Note**  
If you didn't make changes to the custom resource, AWS CloudFormation won't send requests to it during a stack update\.

1. <a name="crpg-walkthrough-stack-updates-customer-template"></a>The template developer initiates an update to the stack that contains a custom resource\. During an update, the template developer can specify new Properties in the stack template\.

   The following is an example of an `Update` to the stack template using a custom resource type:

   ```
   {
      "AWSTemplateFormatVersion" : "2010-09-09",
      "Resources" : {
         "MySeleniumTest" : {
            "Type": "Custom::SeleniumTester",
            "Version" : "1.0",
            "Properties" : {
               "ServiceToken": "arn:aws:sns:us-west-2:123456789012:CRTest",
               "seleniumTester" : "SeleniumTest()",
               "endpoints" : [ "http://mysite.com", "http://myecommercesite.com/", "http://search.mysite.com",
                  "http://mynewsite.com" ],
               "frequencyOfTestsPerHour" : [ "3", "2", "4", "3" ]
            }
         }
      },
      "Outputs" : {
         "topItem" : {
            "Value" : { "Fn::GetAtt" : ["MySeleniumTest", "resultsPage"] }
         },
         "numRespondents" : {
            "Value" : { "Fn::GetAtt" : ["MySeleniumTest", "lastUpdate"] }
         }
      }
   }
   ```

1. <a name="crpg-walkthrough-stack-updates-provider-request"></a>AWS CloudFormation sends an Amazon SNS notification to the resource provider with a `"RequestType" : "Update"` that contains similar information to the `Create` call, except that the `OldResourceProperties` field contains the old resource properties, and ResourceProperties contains the updated \(if any\) resource properties\.

   The following is an example of an `Update` request:

   ```
   {
      "RequestType" : "Update",
      "ResponseURL" : "http://pre-signed-S3-url-for-response",
      "StackId" : "arn:aws:cloudformation:us-west-2:123456789012:stack/stack-name/guid",
      "RequestId" : "uniqueid for this update request",
      "LogicalResourceId" : "MySeleniumTester",
      "ResourceType" : "Custom::SeleniumTester",  
      "PhysicalResourceId" : "Tester1",
      "ResourceProperties" : {
         "seleniumTester" : "SeleniumTest()",
         "endpoints" : [ "http://mysite.com", "http://myecommercesite.com/", "http://search.mysite.com",
            "http://mynewsite.com" ],
         "frequencyOfTestsPerHour" : [ "3", "2", "4", "3" ]
      },
      "OldResourceProperties" : {
         "seleniumTester" : "SeleniumTest()",
         "endpoints" : [ "http://mysite.com", "http://myecommercesite.com/", "http://search.mysite.com" ],
         "frequencyOfTestsPerHour" : [ "3", "2", "4" ]
      }
   }
   ```

1. <a name="crpg-walkthrough-stack-updates-provider-response"></a>The custom resource provider processes the data sent by AWS CloudFormation\. The custom resource performs the update and sends a response of either `SUCCESS` or `FAILED` to the S3 URL\. AWS CloudFormation then compares the `PhysicalResourceIDs` of old and new custom resources\. If they are different, AWS CloudFormation recognizes that the update requires a replacement and sends a delete request to the old resource\. The following example demonstrates the custom resource provider response to an `Update` request\. 

   ```
   {
      "Status" : "SUCCESS",
      "StackId" : "arn:aws:cloudformation:us-west-2:123456789012:stack/stack-name/guid",
      "RequestId" : "uniqueid for this update request",
      "LogicalResourceId" : "MySeleniumTester",
      "PhysicalResourceId" : "Tester2"
   }
   ```

   The `StackId`, `RequestId`, and `LogicalResourceId` fields must be copied verbatim from the request\.

1. <a name="crpg-walkthrough-stack-updates-stack-status"></a>AWS CloudFormation declares the stack status as `UPDATE_COMPLETE` or `UPDATE_FAILED`\. If the update fails, the stack rolls back\. If the stack was successfully updated, the template developer can access any new output values of the created custom resource with `Fn::GetAtt`\.

For detailed information about the request and response objects involved in `Update` requests, see [Update](crpg-ref-requesttypes-update.md) in the [Custom Resource Reference](crpg-ref.md)\.

### Step 3: Stack deletion<a name="crpg-walkthrough-stack-deletion"></a>

1. <a name="crpg-walkthrough-stack-deletion-customer-template"></a>The template developer deletes a stack that contains a custom resource\. AWS CloudFormation gets the current properties specified in the stack template along with the SNS topic, and prepares to make a request to the custom resource provider\.

1. <a name="crpg-walkthrough-stack-deletion-provider-request"></a>AWS CloudFormation sends an Amazon SNS notification to the resource provider with a `"RequestType" : "Delete"` that contains current information about the stack, the custom resource properties from the stack template, and an S3 URL for the response\. 

   Whenever you delete a stack or make an update that removes or replaces the custom resource, AWS CloudFormation compares the `PhysicalResourceId` between the old and new custom resources\. If they are different, AWS CloudFormation recognizes the update as a replacement and sends a delete request for the old resource \(`OldPhysicalResource`\), as shown in the following example of a `Delete` request\. 

   ```
   {
      "RequestType" : "Delete",
      "ResponseURL" : "http://pre-signed-S3-url-for-response",
      "StackId" : "arn:aws:cloudformation:us-west-2:123456789012:stack/stack-name/guid",
      "RequestId" : "unique id for this delete request",
      "ResourceType" : "Custom::SeleniumTester",
      "LogicalResourceId" : "MySeleniumTester",
      "PhysicalResourceId" : "Tester1",
      "ResourceProperties" : {
         "seleniumTester" : "SeleniumTest()",
         "endpoints" : [ "http://mysite.com", "http://myecommercesite.com/", "http://search.mysite.com",
            "http://mynewsite.com" ],
         "frequencyOfTestsPerHour" : [ "3", "2", "4", "3" ]
      }
   }
   ```

   `DescribeStackResource`, `DescribeStackResources`, and `ListStackResources` display the user\-defined name if it has been specified\.

1. <a name="crpg-walkthrough-stack-deletion-provider-response"></a>The custom resource provider processes the data sent by AWS CloudFormation and determines whether the `Delete` request was successful\. The resource provider then uses the S3 URL sent by AWS CloudFormation to send a response of either `SUCCESS` or `FAILED`\. To successfully delete a stack with a custom resource, the custom resource provider must respond successfully to a delete request\.

   The following is an example of a custom resource provider response to a `Delete` request:

   ```
   {
      "Status" : "SUCCESS",
      "StackId" : "arn:aws:cloudformation:us-west-2:123456789012:stack/stack-name/guid",
      "RequestId" : "unique id for this delete request",
      "LogicalResourceId" : "MySeleniumTester",
      "PhysicalResourceId" : "Tester1"
   }
   ```

   The `StackId`, `RequestId`, and `LogicalResourceId` fields must be copied verbatim from the request\.

1. <a name="crpg-walkthrough-stack-updates-stack-status-delete"></a>AWS CloudFormation declares the stack status as `DELETE_COMPLETE` or `DELETE_FAILED`\.

For detailed information about the request and response objects involved in `Delete` requests, see [Delete](crpg-ref-requesttypes-delete.md) in the [Custom resource reference](crpg-ref.md)\.

### See also<a name="w7739ab1c27c24c12b5c12"></a>
+ [AWS CloudFormation Custom Resource Reference](crpg-ref.md)
+ [AWS::CloudFormation::CustomResource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cfn-customresource.html)
+ [Fn::GetAtt](intrinsic-function-reference-getatt.md)