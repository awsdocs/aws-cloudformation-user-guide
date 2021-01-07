# `cfn-response` module<a name="cfn-lambda-function-code-cfnresponsemodule"></a>

When you use the `ZipFile` property to specify your [function's](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-function.html) source code and that function interacts with an AWS CloudFormation custom resource, you can load the `cfn-response` module to send responses to those resources\. The module contains a `send` method, which sends a [response object](crpg-ref-responses.md) to a custom resource by way of an Amazon S3 presigned URL \(the `ResponseURL`\)\.

After executing the `send` method, the Lambda function terminates, so anything you write after that method is ignored\.

**Note**  
The `cfn-response` module is available only when you use the `ZipFile` property to write your source code\. It isn't available for source code that's stored in Amazon S3 buckets\. For code in buckets, you must write your own functions to send responses\.

## Loading the `cfn-response` module<a name="w7739ab1c27c24c14b9b9"></a>

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

## `send` method parameters<a name="w7739ab1c27c24c14b9c11"></a>

You can use the following parameters with the `send` method\.

`event`  
The fields in a [custom resource request](crpg-ref-requesttypes.md)\.

`context`  
An object, specific to Lambda functions, that you can use to specify when the function and any callbacks have completed execution, or to access information from within the Lambda execution environment\. For more information, see [Programming model \(Node\.js\)](https://docs.aws.amazon.com/lambda/latest/dg/programming-model.html) in the *AWS Lambda Developer Guide*\.

`responseStatus`  
Whether the function successfully completed\. Use the `cfnresponse` module constants to specify the status: `SUCCESS` for successful executions and `FAILED` for failed executions\.

`responseData`  
The `Data` field of a custom resource [response object](crpg-ref-responses.md)\. The data is a list of name\-value pairs\.

`physicalResourceId`  
Optional\. The unique identifier of the custom resource that invoked the function\. By default, the module uses the name of the Amazon CloudWatch Logs log stream that's associated with the Lambda function\.

`noEcho`  
Optional\. Indicates whether to mask the output of the custom resource when it's retrieved by using the `Fn::GetAtt` function\. If set to `true`, all returned values are masked with asterisks \(\*\*\*\*\*\), except for information stored in the locations specified below\. By default, this value is `false`\.  
Using the `NoEcho` attribute does not mask any information stored in the following:  
+ The `Metadata` template section\. CloudFormation does not transform, modify, or redact any information you include in the `Metadata` section\. For more information, see [Metadata](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/metadata-section-structure.html)\.
+ The `Outputs` template section\. For more information, see [Outputs](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/outputs-section-structure.html)\.
+ The `Metadata` attribute of a resource definition\. For more information, [Metadata attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-metadata.html)\.
We strongly recommend you do not use these mechanisms to include sensitive information, such as passwords or secrets\.
For more information about using `NoEcho` to mask sensitive information, see the [Do not embed credentials in your templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/best-practices.html#creds) best practice\.

## Examples<a name="w7739ab1c27c24c14b9c13"></a>

### Node\.js<a name="w7739ab1c27c24c14b9c13b3"></a>

In the following Node\.js example, the inline Lambda function takes an input value and multiplies it by 5\. Inline functions are especially useful for smaller functions because they allow you to specify the source code directly in the template, instead of creating a package and uploading it to an Amazon S3 bucket\. The function uses the `cfn-response` `send` method to send the result back to the custom resource that invoked it\.

#### JSON<a name="cfn-lambda-function-code-zipfile-examplenodejs.json"></a>

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

#### YAML<a name="cfn-lambda-function-code-zipfile-examplenodejs.yaml"></a>

```
ZipFile: >
  var response = require('cfn-response');
  exports.handler = function(event, context) {
    var input = parseInt(event.ResourceProperties.Input);
    var responseData = {Value: input * 5};
    response.send(event, context, response.SUCCESS, responseData);
  };
```

### Python<a name="w7739ab1c27c24c14b9c13b5"></a>

In the following Python example, the inline Lambda function takes an integer value and multiplies it by 5\.

#### JSON<a name="cfn-lambda-function-code-zipfile-examplepython.json"></a>

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

#### YAML<a name="cfn-lambda-function-code-zipfile-examplepython.yaml"></a>

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

## Module source code<a name="w7739ab1c27c24c14b9c15"></a>

The following is the response module source code for the Node\.js functions\. Review it to understand what the module does and for help with implementing your own response functions\.

```
// Copyright Amazon.com, Inc. or its affiliates. All Rights Reserved.
// SPDX-License-Identifier: MIT-0
 
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

The following is the response module source code for Python 2 and 3 functions: 

```
# Copyright Amazon.com, Inc. or its affiliates. All Rights Reserved.
# SPDX-License-Identifier: MIT-0
 
from __future__ import print_function
import urllib3
import json

SUCCESS = "SUCCESS"
FAILED = "FAILED"

http = urllib3.PoolManager()


def send(event, context, responseStatus, responseData, physicalResourceId=None, noEcho=False, reason=None):
    responseUrl = event['ResponseURL']

    print(responseUrl)

    responseBody = {
        'Status' : responseStatus,
        'Reason' : reason or "See the details in CloudWatch Log Stream: {}".format(context.log_stream_name),
        'PhysicalResourceId' : physicalResourceId or context.log_stream_name,
        'StackId' : event['StackId'],
        'RequestId' : event['RequestId'],
        'LogicalResourceId' : event['LogicalResourceId'],
        'NoEcho' : noEcho,
        'Data' : responseData
    }

    json_responseBody = json.dumps(responseBody)

    print("Response body:")
    print(json_responseBody)

    headers = {
        'content-type' : '',
        'content-length' : str(len(json_responseBody))
    }

    try:
        response = http.request('PUT', responseUrl, headers=headers, body=json_responseBody)
        print("Status code:", response.status)


    except Exception as e:

        print("send(..) failed executing http.request(..):", e)
```