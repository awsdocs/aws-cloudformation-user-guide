# AWS::Synthetics::Canary<a name="aws-resource-synthetics-canary"></a>

Creates or updates a canary\. Canaries are scripts that monitor your endpoints and APIs from the outside\-in\. Canaries help you check the availability and latency of your web services and troubleshoot anomalies by investigating load time data, screenshots of the UI, logs, and metrics\. You can set up a canary to run continuously or just once\. 

To create canaries, you must have the `CloudWatchSyntheticsFullAccess` policy\. If you are creating a new IAM role for the canary, you also need the the `iam:CreateRole`, `iam:CreatePolicy` and `iam:AttachRolePolicy` permissions\. For more information, see [Necessary Roles and Permissions](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Synthetics_Canaries_Roles)\.

Do not include secrets or proprietary information in your canary names\. The canary name makes up part of the Amazon Resource Name \(ARN\) for the canary, and the ARN is included in outbound calls over the internet\. For more information, see [Security Considerations for Synthetics Canaries](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/servicelens_canaries_security.html)\.

## Syntax<a name="aws-resource-synthetics-canary-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-synthetics-canary-syntax.json"></a>

```
{
  "Type" : "AWS::Synthetics::Canary",
  "Properties" : {
      "[ArtifactS3Location](#cfn-synthetics-canary-artifacts3location)" : String,
      "[Code](#cfn-synthetics-canary-code)" : Code,
      "[ExecutionRoleArn](#cfn-synthetics-canary-executionrolearn)" : String,
      "[FailureRetentionPeriod](#cfn-synthetics-canary-failureretentionperiod)" : Integer,
      "[Name](#cfn-synthetics-canary-name)" : String,
      "[RunConfig](#cfn-synthetics-canary-runconfig)" : RunConfig,
      "[RuntimeVersion](#cfn-synthetics-canary-runtimeversion)" : String,
      "[Schedule](#cfn-synthetics-canary-schedule)" : Schedule,
      "[StartCanaryAfterCreation](#cfn-synthetics-canary-startcanaryaftercreation)" : Boolean,
      "[SuccessRetentionPeriod](#cfn-synthetics-canary-successretentionperiod)" : Integer,
      "[Tags](#cfn-synthetics-canary-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VPCConfig](#cfn-synthetics-canary-vpcconfig)" : VPCConfig
    }
}
```

### YAML<a name="aws-resource-synthetics-canary-syntax.yaml"></a>

```
Type: AWS::Synthetics::Canary
Properties: 
  [ArtifactS3Location](#cfn-synthetics-canary-artifacts3location): String
  [Code](#cfn-synthetics-canary-code): 
    Code
  [ExecutionRoleArn](#cfn-synthetics-canary-executionrolearn): String
  [FailureRetentionPeriod](#cfn-synthetics-canary-failureretentionperiod): Integer
  [Name](#cfn-synthetics-canary-name): String
  [RunConfig](#cfn-synthetics-canary-runconfig): 
    RunConfig
  [RuntimeVersion](#cfn-synthetics-canary-runtimeversion): String
  [Schedule](#cfn-synthetics-canary-schedule): 
    Schedule
  [StartCanaryAfterCreation](#cfn-synthetics-canary-startcanaryaftercreation): Boolean
  [SuccessRetentionPeriod](#cfn-synthetics-canary-successretentionperiod): Integer
  [Tags](#cfn-synthetics-canary-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VPCConfig](#cfn-synthetics-canary-vpcconfig): 
    VPCConfig
```

## Properties<a name="aws-resource-synthetics-canary-properties"></a>

`ArtifactS3Location`  <a name="cfn-synthetics-canary-artifacts3location"></a>
The location in Amazon S3 where Synthetics stores artifacts from the runs of this canary\. Artifacts include the log file, screenshots, and HAR files\. Specify the full location path, including `s3://` at the beginning of the path\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Code`  <a name="cfn-synthetics-canary-code"></a>
Use this structure to input your script code for the canary\. This structure contains the Lambda handler with the location where the canary should start running the script\. If the script is stored in an S3 bucket, the bucket name, key, and version are also included\. If the script is passed into the canary directly, the script code is contained in the value of `Script`\.   
*Required*: Yes  
*Type*: [Code](aws-properties-synthetics-canary-code.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExecutionRoleArn`  <a name="cfn-synthetics-canary-executionrolearn"></a>
The ARN of the IAM role to be used to run the canary\. This role must already exist, and must include `lambda.amazonaws.com` as a principal in the trust policy\. The role must also have the following permissions:  
+  `s3:PutObject` 
+  `s3:GetBucketLocation` 
+  `s3:ListAllMyBuckets` 
+  `cloudwatch:PutMetricData` 
+  `logs:CreateLogGroup` 
+  `logs:CreateLogStream` 
+  `logs:PutLogEvents` 
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `arn:(aws[a-zA-Z-]*)?:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FailureRetentionPeriod`  <a name="cfn-synthetics-canary-failureretentionperiod"></a>
The number of days to retain data about failed runs of this canary\. If you omit this field, the default of 31 days is used\. The valid range is 1 to 455 days\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-synthetics-canary-name"></a>
The name for this canary\. Be sure to give it a descriptive name that distinguishes it from other canaries in your account\.  
Do not include secrets or proprietary information in your canary names\. The canary name makes up part of the canary ARN, and the ARN is included in outbound calls over the internet\. For more information, see [Security Considerations for Synthetics Canaries](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/servicelens_canaries_security.html)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `21`  
*Pattern*: `^[0-9a-z_\-]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RunConfig`  <a name="cfn-synthetics-canary-runconfig"></a>
A structure that contains input information for a canary run\. If you omit this structure, the frequency of the canary is used as canary's timeout value, up to a maximum of 900 seconds\.  
*Required*: No  
*Type*: [RunConfig](aws-properties-synthetics-canary-runconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuntimeVersion`  <a name="cfn-synthetics-canary-runtimeversion"></a>
Specifies the runtime version to use for the canary\. For more information about runtime versions, see [ Canary Runtime Versions](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Synthetics_Canaries_Library.html)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Schedule`  <a name="cfn-synthetics-canary-schedule"></a>
A structure that contains information about how often the canary is to run, and when these runs are to stop\.  
*Required*: Yes  
*Type*: [Schedule](aws-properties-synthetics-canary-schedule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartCanaryAfterCreation`  <a name="cfn-synthetics-canary-startcanaryaftercreation"></a>
Specify TRUE to have the canary start making runs immediately after it is created\.  
A canary that you create using CloudFormation can't be used to monitor the CloudFormation stack that creates the canary or to roll back that stack if there is a failure\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SuccessRetentionPeriod`  <a name="cfn-synthetics-canary-successretentionperiod"></a>
The number of days to retain data about successful runs of this canary\. If you omit this field, the default of 31 days is used\. The valid range is 1 to 455 days\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-synthetics-canary-tags"></a>
The list of key\-value pairs that are associated with the canary\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VPCConfig`  <a name="cfn-synthetics-canary-vpcconfig"></a>
If this canary is to test an endpoint in a VPC, this structure contains information about the subnet and security groups of the VPC endpoint\. For more information, see [ Running a Canary in a VPC](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Synthetics_Canaries_VPC.html)\.  
*Required*: No  
*Type*: [VPCConfig](aws-properties-synthetics-canary-vpcconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-synthetics-canary-return-values"></a>

### Ref<a name="aws-resource-synthetics-canary-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the canary, such as `MyCanary`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-synthetics-canary-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-synthetics-canary-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
The ID of the canary\.

`State`  <a name="State-fn::getatt"></a>
The state of the canary\. For example, `RUNNING`\.

## Examples<a name="aws-resource-synthetics-canary--examples"></a>



### Canary with script stored in an Amazon S3 bucket<a name="aws-resource-synthetics-canary--examples--Canary_with_script_stored_in_an_Amazon_S3_bucket"></a>

This example creates a canary that uses an existing script stored in an S3 bucket\. The canary is started as soon as it is created\.

#### JSON<a name="aws-resource-synthetics-canary--examples--Canary_with_script_stored_in_an_Amazon_S3_bucket--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "AWS CloudFormation Sample Template for AWS Synthetics: Create a Canary using this template",
    "Resources": {
        "SyntheticsCanary": {
            "Type": "AWS::Synthetics::Canary",
            "Properties": {
                "Name": {
                    "Ref": "samplecanary"
                },
                "ExecutionRoleArn": {
                    "Ref": "arn:aws:iam::123456789012:role/my-lambda-execution-role-to-run-canary"
                },
                "Code": {
                    "Handler": "pageLoadBlueprint.handler",
                    "S3Bucket": "aws-synthetics-code-myaccount-canary1",
                    "S3Key": "my-script-location"
                },
                "ArtifactS3Location": "s3://my-results-bucket",
                "RuntimeVersion": "syn-1.0",
                "Schedule": {
                    "Expression": "rate(1 minute)",
                    "DurationInSeconds": 3600
                },
                "RunConfig": {
                    "TimeoutInSeconds": 60
                },
                "FailureRetentionPeriod": 30,
                "SuccessRetentionPeriod": 30,
                "StartCanaryAfterCreation": true,
                "Tags": [
                    {
                        "Key": "key00AtCreate",
                        "Value": "value001AtCreate"
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-synthetics-canary--examples--Canary_with_script_stored_in_an_Amazon_S3_bucket--yaml"></a>

```
Resources:
    SyntheticsCanary:
        Type: 'AWS::Synthetics::Canary'
        Properties:
            Name: samplecanary
            ExecutionRoleArn: 'arn:aws:iam::123456789012:role/my-lambda-execution-role-to-run-canary'
            Code: {Handler: pageLoadBlueprint.handler, S3Bucket: aws-synthetics-code-myaccount-canary1, S3Key: my-script-location}
            ArtifactS3Location: s3://my-results-bucket
            RuntimeVersion: syn-1.0
            Schedule: {Expression: 'rate(1 minute)', DurationInSeconds: 3600}
            RunConfig: {TimeoutInSeconds: 60}
            FailureRetentionPeriod: 30
            SuccessRetentionPeriod: 30
            Tags: [{Key: key00AtCreate, Value: value001AtCreate}]
            StartCanaryAfterCreation: true
```

### Canary with script passed through CloudFormation<a name="aws-resource-synthetics-canary--examples--Canary_with_script_passed_through_CloudFormation"></a>

This example creates a canary and passes the script code directly into the canary\.

#### JSON<a name="aws-resource-synthetics-canary--examples--Canary_with_script_passed_through_CloudFormation--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "AWS CloudFormation Sample Template for AWS Synthetics: Create a Canary using this template",
    "Resources": {
        "SyntheticsCanary": {
            "Type": "AWS::Synthetics::Canary",
            "Properties": {
                "Name": {
                    "Ref": "samplecanary"
                },
                "ExecutionRoleArn": {
                    "Ref": "arn:aws:iam::123456789012:role/my-lambda-execution-role-to-run-canary"
                },
                "Code": {
                    "Handler": "pageLoadBlueprint.handler",
                    "Script": "var synthetics = require('Synthetics');\nconst log = require('SyntheticsLogger');\n\nconst pageLoadBlueprint = async function () {\n\n    // INSERT URL here\n    const URL = \"https://amazon.com\";\n\n    let page = await synthetics.getPage();\n    const response = await page.goto(URL, {waitUntil: 'domcontentloaded', timeout: 30000});\n    //Wait for page to render.\n    //Increase or decrease wait time based on endpoint being monitored.\n    await page.waitFor(15000);\n    await synthetics.takeScreenshot('loaded', 'loaded');\n    let pageTitle = await page.title();\n    log.info('Page title: ' + pageTitle);\n    if (response.status() !== 200) {\n        throw \"Failed to load page!\";\n    }\n};\n\nexports.handler = async () => {\n    return await pageLoadBlueprint();\n};\n"
                },
                "ArtifactS3Location": "s3://my-results-bucket",
                "RuntimeVersion": "syn-1.0",
                "Schedule": {
                    "Expression": "rate(1 minute)",
                    "DurationInSeconds": 3600
                },
                "RunConfig": {
                    "TimeoutInSeconds": 60
                },
                "FailureRetentionPeriod": 30,
                "SuccessRetentionPeriod": 30,
                "StartCanaryAfterCreation": false,
                "Tags": [
                    {
                        "Id": "key00AtCreate",
                        "Value": "value001AtCreate"
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-synthetics-canary--examples--Canary_with_script_passed_through_CloudFormation--yaml"></a>

```
Resources:
    SyntheticsCanary:
        Type: 'AWS::Synthetics::Canary'
        Properties:
            Name: samplecanary
            ExecutionRoleArn: 'arn:aws:iam::123456789012:role/my-lambda-execution-role-to-run-canary'
            Code: {Handler: pageLoadBlueprint.handler, Script: "var synthetics = require('Synthetics');\nconst log = require('SyntheticsLogger');\nconst pageLoadBlueprint = async function () {\n// INSERT URL here\nconst URL = \"https://amazon.com\";\n\nlet page = await synthetics.getPage();\nconst response = await page.goto(URL, {waitUntil: 'domcontentloaded', timeout: 30000});\n//Wait for page to render.\n//Increase or decrease wait time based on endpoint being monitored.\nawait page.waitFor(15000);\nawait synthetics.takeScreenshot('loaded', 'loaded');\nlet pageTitle = await page.title();\nlog.info('Page title: ' + pageTitle);\nif (response.status() !== 200) {\n     throw \"Failed to load page!\";\n}\n};\n\nexports.handler = async () => {\nreturn await pageLoadBlueprint();\n};\n"}
            ArtifactS3Location: s3://my-results-bucket
            RuntimeVersion: syn-1.0
            Schedule: {Expression: 'rate(1 minute)', DurationInSeconds: 3600}
            RunConfig: {TimeoutInSeconds: 60}
            FailureRetentionPeriod: 30
            SuccessRetentionPeriod: 30
            Tags: [{Key: key00AtCreate, Value: value001AtCreate}]
            StartCanaryAfterCreation: false
```