# AWS::CloudFormation::Stack<a name="aws-properties-stack"></a>

The `AWS::CloudFormation::Stack` type nests a stack as a resource in a top\-level template\.

You can add output values from a nested stack within the containing template\. You use the [GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html) function with the nested stack's logical name and the name of the output value in the nested stack in the format `Outputs.NestedStackOutputName`\.

**Important**  
We strongly recommend that updates to nested stacks are run from the parent stack\.

When you apply template changes to update a top\-level stack, CloudFormation updates the top\-level stack and initiates an update to its nested stacks\. CloudFormation updates the resources of modified nested stacks, but does not update the resources of unmodified nested stacks\. For more information, see [CloudFormation stack updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html)\.

**Note**  
You must acknowledge IAM capabilities for nested stacks that contain IAM resources\. Also, verify that you have cancel update stack permissions, which is required if an update rolls back\. For more information about IAM and CloudFormation, see [Controlling access with AWS Identity and Access Management](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-iam-template.html)\.

## Syntax<a name="aws-properties-stack-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-stack-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFormation::Stack",
  "Properties" : {
      "[NotificationARNs](#cfn-cloudformation-stack-notificationarns)" : [ String, ... ],
      "[Parameters](#cfn-cloudformation-stack-parameters)" : {Key : Value, ...},
      "[Tags](#cfn-cloudformation-stack-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TemplateURL](#cfn-cloudformation-stack-templateurl)" : String,
      "[TimeoutInMinutes](#cfn-cloudformation-stack-timeoutinminutes)" : Integer
    }
}
```

### YAML<a name="aws-properties-stack-syntax.yaml"></a>

```
Type: AWS::CloudFormation::Stack
Properties: 
  [NotificationARNs](#cfn-cloudformation-stack-notificationarns): 
    - String
  [Parameters](#cfn-cloudformation-stack-parameters): 
    Key : Value
  [Tags](#cfn-cloudformation-stack-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TemplateURL](#cfn-cloudformation-stack-templateurl): String
  [TimeoutInMinutes](#cfn-cloudformation-stack-timeoutinminutes): Integer
```

## Properties<a name="aws-properties-stack-properties"></a>

`NotificationARNs`  <a name="cfn-cloudformation-stack-notificationarns"></a>
The Simple Notification Service \(SNS\) topic ARNs to publish stack related events\. You can find your SNS topic ARNs using the SNS console or your Command Line Interface \(CLI\)\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-cloudformation-stack-parameters"></a>
The set value pairs that represent the parameters passed to CloudFormation when this nested stack is created\. Each parameter has a name corresponding to a parameter defined in the embedded template and a value representing the value that you want to set for the parameter\.   
If you use the `Ref` function to pass a parameter value to a nested stack, comma\-delimited list parameters must be of type `String`\. In other words, you cannot pass values that are of type `CommaDelimitedList` to nested stacks\.
Conditional\. Required if the nested stack requires input parameters\.  
Whether an update causes interruptions depends on the resources that are being updated\. An update never causes a nested stack to be replaced\.  
*Required*: Conditional  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-cloudformation-stack-tags"></a>
Key\-value pairs to associate with this stack\. AWS CloudFormation also propagates these tags to the resources created in the stack\. A maximum number of 50 tags can be specified\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplateURL`  <a name="cfn-cloudformation-stack-templateurl"></a>
Location of file containing the template body\. The URL must point to a template \(max size: 460,800 bytes\) that is located in an Amazon S3 bucket\. For more information, see [Template anatomy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-anatomy.html)\.  
Whether an update causes interruptions depends on the resources that are being updated\. An update never causes a nested stack to be replaced\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeoutInMinutes`  <a name="cfn-cloudformation-stack-timeoutinminutes"></a>
The length of time, in minutes, that CloudFormation waits for the nested stack to reach the `CREATE_COMPLETE` state\. The default is no timeout\. When CloudFormation detects that the nested stack has reached the `CREATE_COMPLETE` state, it marks the nested stack resource as `CREATE_COMPLETE` in the parent stack and resumes creating the parent stack\. If the timeout period expires before the nested stack reaches `CREATE_COMPLETE`, CloudFormation marks the nested stack as failed and rolls back both the nested stack and parent stack\.  
Updates are not supported\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-properties-stack-return-values"></a>

### Ref<a name="aws-properties-stack-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the stack ID\. For example:

 `arn:aws:cloudformation:us-east-2:123456789012:stack/mystack-mynestedstack-sggfrhxhum7w/f449b250-b969-11e0-a185-5081d0136786` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-properties-stack--examples"></a>



### Specify stack parameters<a name="aws-properties-stack--examples--Specify_stack_parameters"></a>

The sample template EC2ChooseAMI\.template contains the following Parameters section:

#### JSON<a name="aws-properties-stack--examples--Specify_stack_parameters--json"></a>

```
"Parameters" : {
  "InstanceType" : {
    "Type" : "String",
    "Default" : "m1.small",
    "Description" : "EC2 instance type, e.g. m1.small, m1.large, etc."
  },
    "WebServerPort" : {
    "Type" : "String",
    "Default" : "80",
    "Description" : "TCP/IP port of the web server"
  },
  "KeyName" : {
    "Type" : "String",
    "Description" : "Name of an existing EC2 KeyPair to enable SSH access to the web server"
  }
}
```

#### YAML<a name="aws-properties-stack--examples--Specify_stack_parameters--yaml"></a>

```
Parameters: 
  InstanceType: 
    Type: "String"
    Default: "m1.small"
    Description: "EC2 instance type, e.g. m1.small, m1.large, etc."
  WebServerPort: 
    Type: "String"
    Default: "80"
    Description: "TCP/IP port of the web server"
  KeyName: 
    Type: "String"
    Description: "Name of an existing EC2 KeyPair to enable SSH access to the web server"
```

### Nested stack<a name="aws-properties-stack--examples--Nested_stack"></a>

You could use the following template to embed a stack \(myStackWithParams\) using the EC2ChooseAMI\.template and use the Parameters property in the AWS::CloudFormation::Stack resource to specify an InstanceType and KeyName\.

#### JSON<a name="aws-properties-stack--examples--Nested_stack--json"></a>

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",
  "Resources" : {
    "myStackWithParams" : {
      "Type" : "AWS::CloudFormation::Stack",
      "Properties" : {
        "TemplateURL" : "https://s3.amazonaws.com/cloudformation-templates-us-east-2/EC2ChooseAMI.template",
        "Parameters" : {
          "InstanceType" : "t1.micro",
          "KeyName" : "mykey"
        }
      }
    }
  }
}
```

#### YAML<a name="aws-properties-stack--examples--Nested_stack--yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
  myStackWithParams: 
    Type: AWS::CloudFormation::Stack
    Properties: 
      TemplateURL: "https://s3.amazonaws.com/cloudformation-templates-us-east-2/EC2ChooseAMI.template"
      Parameters: 
        InstanceType: "t1.micro"
        KeyName: "mykey"
```

## See also<a name="aws-properties-stack--seealso"></a>
+ For sample template snippets, see Nested Stacks in [CloudFormation template snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-cloudformation.html)\.
+ If you have nested stacks that are stuck in an in\-progress operation, see Troubleshooting Errors in [Troubleshooting AWS CloudFormation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/troubleshooting.html)\.

