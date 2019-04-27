# AWS Lambda Function Code<a name="aws-properties-lambda-function-code"></a>

`Code` is a property of the [AWS::Lambda::Function](aws-resource-lambda-function.md) resource that specifies the code for a Lambda function\. For all runtimes, you can specify the location of a deployment package in Amazon S3\. For Node\.js and Python functions, you can also specify the function code inline in the template\.

**Note**  
Changes to a deployment package in Amazon S3 are not detected automatically\. To update the function code, change the object key, or use object versioning and change the version number in the template\.

## Syntax<a name="w2922ab1c21c10d166c21c17b7"></a>

### JSON<a name="aws-properties-lambda-function-code-syntax.json"></a>

```
{
  "[S3Bucket](#cfn-lambda-function-code-s3bucket)" : String,
  "[S3Key](#cfn-lambda-function-code-s3key)" : String,
  "[S3ObjectVersion](#cfn-lambda-function-code-s3objectversion)" : String,
  "[ZipFile](#cfn-lambda-function-code-zipfile)" : String
}
```

### YAML<a name="aws-properties-lambda-function-code-syntax.yaml"></a>

```
[S3Bucket](#cfn-lambda-function-code-s3bucket): String
[S3Key](#cfn-lambda-function-code-s3key): String
[S3ObjectVersion](#cfn-lambda-function-code-s3objectversion): String
[ZipFile](#cfn-lambda-function-code-zipfile): String
```

## Properties<a name="w2922ab1c21c10d166c21c17b9"></a>

`S3Bucket`  <a name="cfn-lambda-function-code-s3bucket"></a>
An Amazon S3 bucket in the same region as your function\. The bucket can be in a different AWS account\.  
The `cfn-response` module isn't available for source code that's stored in Amazon S3 buckets\. To send responses, write your own functions\.
*Required*: Conditional\. Specify both the `S3Bucket` and `S3Key` properties, or specify the `ZipFile` property\.  
*Type*: String

`S3Key`  <a name="cfn-lambda-function-code-s3key"></a>
The Amazon S3 key of the deployment package\.  
*Required*: Conditional\. You must specify both the `S3Bucket` and `S3Key` properties, or specify the `ZipFile` property\.  
*Type*: String

`S3ObjectVersion`  <a name="cfn-lambda-function-code-s3objectversion"></a>
For versioned objects, the version of the deployment package object to use\.  
*Required*: No  
*Type*: String

`ZipFile`  <a name="cfn-lambda-function-code-zipfile"></a>
\(Node\.js and Python\) The source code of your Lambda function\. If you include your function source inline with this parameter, AWS CloudFormation places it in a file named `index` and zips it to create a [deployment package](https://docs.aws.amazon.com/lambda/latest/dg/deployment-package-v2.html)\. For the `Handler` property, the first part of the handler identifier must be `index`\. For example, `index.handler`\.  
Your source code can contain up to 4096 characters\. For JSON, you must escape quotes and special characters such as newline \(`\n`\) with a backslash\.  
If you specify a function that interacts with an AWS CloudFormation custom resource, you don't have to write your own functions to send responses to the custom resource that invoked the function\. AWS CloudFormation provides a response module that simplifies sending responses\. For more information, see [`cfn-response` Module](#cfn-lambda-function-code-cfnresponsemodule)\.  
*Required*: Conditional\. You must specify both the `S3Bucket` and `S3Key` properties, or specify the `ZipFile` property\.  
*Type*: String

## `cfn-response` Module<a name="cfn-lambda-function-code-cfnresponsemodule"></a>

When you use the `ZipFile` property to specify your function's source code and that function interacts with an AWS CloudFormation custom resource, you can load the `cfn-response` module to send responses to those resources\. The module contains a `send` method, which sends a [response object](crpg-ref-responses.md) to a custom resource by way of an Amazon S3 presigned URL \(the `ResponseURL`\)\.

After executing the `send` method, the Lambda function terminates, so anything you write after that method is ignored\.

**Note**  
The `cfn-response` module is available only when you use the `ZipFile` property to write your source code\. It isn't available for source code that's stored in Amazon S3 buckets\. For code in buckets, you must write your own functions to send responses\.

### Loading the `cfn-response` Module<a name="w2922ab1c21c10d166c21c17c11b9"></a>

For Node\.js functions, use the `require()` function to load the `cfn-response` module\. For example, the following code example creates a `cfn-response` object with the name `response`:

```
var response = require('cfn-response');
```

For Python, use the `import` statement to load the `cfnresponse` module, as shown in the following example:

**Note**  
Use this exact import statement\. If you use other variants of the import statement, AWS CloudFormation doesn't include the response module\.

```
import cfnresponse
```

### `send` Method Parameters<a name="w2922ab1c21c10d166c21c17c11c11"></a>

You can use the following parameters with the `send` method\.

`event`  
The fields in a [custom resource request](crpg-ref-requesttypes.md)\.

`context`  
An object, specific to Lambda functions, that you can use to specify when the function and any callbacks have completed execution, or to access information from within the Lambda execution environment\. For more information, see [Programming Model \(Node\.js\)](https://docs.aws.amazon.com/lambda/latest/dg/programming-model.html) in the *AWS Lambda Developer Guide*\.

`responseStatus`  
Whether the function successfully completed\. Use the `cfnresponse` module constants to specify the status: `SUCCESS` for successful executions and `FAILED` for failed executions\.

`responseData`  
The `Data` field of a custom resource [response object](crpg-ref-responses.md)\. The data is a list of name\-value pairs\.

`physicalResourceId`  
Optional\. The unique identifier of the custom resource that invoked the function\. By default, the module uses the name of the Amazon CloudWatch Logs log stream that's associated with the Lambda function\.

`noEcho`  
Optional\. Indicates whether to mask the output of the custom resource when it's retrieved by using the `Fn::GetAtt` function\. If set to `true`, all returned values are masked with asterisks \(\*\*\*\*\*\)\. By default, this value is `false`\.

### Examples<a name="w2922ab1c21c10d166c21c17c11c13"></a>

#### Node\.js<a name="w2922ab1c21c10d166c21c17c11c13b3"></a>

In the following Node\.js example, the inline Lambda function takes an input value and multiplies it by 5\. Inline functions are especially useful for smaller functions because they allow you to specify the source code directly in the template, instead of creating a package and uploading it to an Amazon S3 bucket\. The function uses the `cfn-response` `send` method to send the result back to the custom resource that invoked it\.

##### JSON<a name="cfn-lambda-function-code-zipfile-examplenodejs.json"></a>

```
"ZipFile": { "Fn::Join": ["", [
  "var response = require('cfn-response');",
  "exports.handler = function(event, context) {",
  "  var input = parseInt(event.ResourceProperties.Input);",
  "  var responseData = {Value: input * 5};",
  "  response.send(event, context, response.SUCCESS, responseData);",
  "};"
]]}
```

##### YAML<a name="cfn-lambda-function-code-zipfile-examplenodejs.yaml"></a>

```
ZipFile: >
  var response = require('cfn-response');
  exports.handler = function(event, context) {
    var input = parseInt(event.ResourceProperties.Input);
    var responseData = {Value: input * 5};
    response.send(event, context, response.SUCCESS, responseData);
  };
```

#### Python<a name="w2922ab1c21c10d166c21c17c11c13b5"></a>

In the following Python example, the inline Lambda function takes an integer value and multiplies it by 5\.

##### JSON<a name="cfn-lambda-function-code-zipfile-examplepython.json"></a>

```
"ZipFile" : { "Fn::Join" : ["\n", [
  "import json",
  "import cfnresponse",
  "def handler(event, context):",
  "   responseValue = int(event['ResourceProperties']['Input']) * 5",
  "   responseData = {}",
  "   responseData['Data'] = responseValue",
  "   cfnresponse.send(event, context, cfnresponse.SUCCESS, responseData, \"CustomResourcePhysicalID\")"
]]}
```

##### YAML<a name="cfn-lambda-function-code-zipfile-examplepython.yaml"></a>

```
ZipFile: |
  import json
  import cfnresponse
  def handler(event, context):
    responseValue = int(event['ResourceProperties']['Input']) * 5
    responseData = {}
    responseData['Data'] = responseValue
    cfnresponse.send(event, context, cfnresponse.SUCCESS, responseData, "CustomResourcePhysicalID")
```

### Module Source Code<a name="w2922ab1c21c10d166c21c17c11c15"></a>

The following is the response module source code for the Node\.js functions\. Review it to understand what the module does and for help with implementing your own response functions\.

```
/* Copyright 2015 Amazon Web Services, Inc. or its affiliates. All Rights Reserved.
   This file is licensed to you under the AWS Customer Agreement (the "License").
   You may not use this file except in compliance with the License.
   A copy of the License is located at http://aws.amazon.com/agreement/ .
   This file is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, express or implied.
   See the License for the specific language governing permissions and limitations under the License. */

exports.SUCCESS = "SUCCESS";
exports.FAILED = "FAILED";

exports.send = function(event, context, responseStatus, responseData, physicalResourceId, noEcho) {

    var responseBody = JSON.stringify({
        Status: responseStatus,
        Reason: "See the details in CloudWatch Log Stream: " + context.logStreamName,
        PhysicalResourceId: physicalResourceId || context.logStreamName,
        StackId: event.StackId,
        RequestId: event.RequestId,
        LogicalResourceId: event.LogicalResourceId,
        NoEcho: noEcho || false,
        Data: responseData
    });

    console.log("Response body:\n", responseBody);

    var https = require("https");
    var url = require("url");

    var parsedUrl = url.parse(event.ResponseURL);
    var options = {
        hostname: parsedUrl.hostname,
        port: 443,
        path: parsedUrl.path,
        method: "PUT",
        headers: {
            "content-type": "",
            "content-length": responseBody.length
        }
    };

    var request = https.request(options, function(response) {
        console.log("Status code: " + response.statusCode);
        console.log("Status message: " + response.statusMessage);
        context.done();
    });

    request.on("error", function(error) {
        console.log("send(..) failed executing https.request(..): " + error);
        context.done();
    });

    request.write(responseBody);
    request.end();
}
```

The following is the response module source code for Python 3 functions: 

```
#  Copyright 2016 Amazon Web Services, Inc. or its affiliates. All Rights Reserved.
#  This file is licensed to you under the AWS Customer Agreement (the "License").
#  You may not use this file except in compliance with the License.
#  A copy of the License is located at http://aws.amazon.com/agreement/ .
#  This file is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, express or implied.
#  See the License for the specific language governing permissions and limitations under the License.

from botocore.vendored import requests
import json

SUCCESS = "SUCCESS"
FAILED = "FAILED"

def send(event, context, responseStatus, responseData, physicalResourceId=None, noEcho=False):
    responseUrl = event['ResponseURL']

    print(responseUrl)

    responseBody = {}
    responseBody['Status'] = responseStatus
    responseBody['Reason'] = 'See the details in CloudWatch Log Stream: ' + context.log_stream_name
    responseBody['PhysicalResourceId'] = physicalResourceId or context.log_stream_name
    responseBody['StackId'] = event['StackId']
    responseBody['RequestId'] = event['RequestId']
    responseBody['LogicalResourceId'] = event['LogicalResourceId']
    responseBody['NoEcho'] = noEcho
    responseBody['Data'] = responseData

    json_responseBody = json.dumps(responseBody)

    print("Response body:\n" + json_responseBody)

    headers = {
        'content-type' : '',
        'content-length' : str(len(json_responseBody))
    }

    try:
        response = requests.put(responseUrl,
                                data=json_responseBody,
                                headers=headers)
        print("Status code: " + response.reason)
    except Exception as e:
        print("send(..) failed executing requests.put(..): " + str(e))
```

The following is the response module source code for Python 2 functions:

```
#  Copyright 2016 Amazon Web Services, Inc. or its affiliates. All Rights Reserved.
#  This file is licensed to you under the AWS Customer Agreement (the "License").
#  You may not use this file except in compliance with the License.
#  A copy of the License is located at http://aws.amazon.com/agreement/ .
#  This file is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, express or implied.
#  See the License for the specific language governing permissions and limitations under the License.

from botocore.vendored import requests
import json

SUCCESS = "SUCCESS"
FAILED = "FAILED"

def send(event, context, responseStatus, responseData, physicalResourceId=None, noEcho=False):
    responseUrl = event['ResponseURL']

    print responseUrl

    responseBody = {}
    responseBody['Status'] = responseStatus
    responseBody['Reason'] = 'See the details in CloudWatch Log Stream: ' + context.log_stream_name
    responseBody['PhysicalResourceId'] = physicalResourceId or context.log_stream_name
    responseBody['StackId'] = event['StackId']
    responseBody['RequestId'] = event['RequestId']
    responseBody['LogicalResourceId'] = event['LogicalResourceId']
    responseBody['NoEcho'] = noEcho
    responseBody['Data'] = responseData

    json_responseBody = json.dumps(responseBody)
   
    print "Response body:\n" + json_responseBody

    headers = {
        'content-type' : '', 
        'content-length' : str(len(json_responseBody))
    }
    
    try:
        response = requests.put(responseUrl,
                                data=json_responseBody,
                                headers=headers)
        print "Status code: " + response.reason
    except Exception as e:
        print "send(..) failed executing requests.put(..): " + str(e)
```