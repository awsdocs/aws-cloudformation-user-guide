# AWS::IAM::VirtualMFADevice<a name="aws-resource-iam-virtualmfadevice"></a>

Creates a new virtual MFA device for the AWS account\. After creating the virtual MFA, use [EnableMFADevice](https://docs.aws.amazon.com/IAM/latest/APIReference/API_EnableMFADevice.html) to attach the MFA device to an IAM user\. For more information about creating and working with virtual MFA devices, see [Using a virtual MFA device](https://docs.aws.amazon.com/IAM/latest/UserGuide/Using_VirtualMFA.html) in the *IAM User Guide*\.

For information about the maximum number of MFA devices you can create, see [IAM and AWS STS quotas](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_iam-quotas.html) in the *IAM User Guide*\.

**Important**  
The seed information contained in the QR code and the Base32 string should be treated like any other secret access information\. In other words, protect the seed information as you would your AWS access keys or your passwords\. After you provision your virtual device, you should ensure that the information is destroyed following secure procedures\.

## Syntax<a name="aws-resource-iam-virtualmfadevice-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iam-virtualmfadevice-syntax.json"></a>

```
{
  "Type" : "AWS::IAM::VirtualMFADevice",
  "Properties" : {
      "[Path](#cfn-iam-virtualmfadevice-path)" : String,
      "[Tags](#cfn-iam-virtualmfadevice-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Users](#cfn-iam-virtualmfadevice-users)" : [ String, ... ],
      "[VirtualMfaDeviceName](#cfn-iam-virtualmfadevice-virtualmfadevicename)" : String
    }
}
```

### YAML<a name="aws-resource-iam-virtualmfadevice-syntax.yaml"></a>

```
Type: AWS::IAM::VirtualMFADevice
Properties: 
  [Path](#cfn-iam-virtualmfadevice-path): String
  [Tags](#cfn-iam-virtualmfadevice-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Users](#cfn-iam-virtualmfadevice-users): 
    - String
  [VirtualMfaDeviceName](#cfn-iam-virtualmfadevice-virtualmfadevicename): String
```

## Properties<a name="aws-resource-iam-virtualmfadevice-properties"></a>

`Path`  <a name="cfn-iam-virtualmfadevice-path"></a>
 The path for the virtual MFA device\. For more information about paths, see [IAM identifiers](https://docs.aws.amazon.com/IAM/latest/UserGuide/Using_Identifiers.html) in the *IAM User Guide*\.  
This parameter is optional\. If it is not included, it defaults to a slash \(/\)\.  
This parameter allows \(through its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of either a forward slash \(/\) by itself or a string that must begin and end with forward slashes\. In addition, it can contain any ASCII character from the \! \(`\u0021`\) through the DEL character \(`\u007F`\), including most punctuation characters, digits, and upper and lowercased letters\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `(\u002F)|(\u002F[\u0021-\u007F]+\u002F)`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-iam-virtualmfadevice-tags"></a>
A list of tags that you want to attach to the new IAM virtual MFA device\. Each tag consists of a key name and an associated value\. For more information about tagging, see [Tagging IAM resources](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_tags.html) in the *IAM User Guide*\.  
If any one of the tags is invalid or if you exceed the allowed maximum number of tags, then the entire request fails and the resource is not created\.
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Users`  <a name="cfn-iam-virtualmfadevice-users"></a>
The IAM user associated with this virtual MFA device\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VirtualMfaDeviceName`  <a name="cfn-iam-virtualmfadevice-virtualmfadevicename"></a>
The name of the virtual MFA device\. Use with path to uniquely identify a virtual MFA device\.  
This parameter allows \(through its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of upper and lowercase alphanumeric characters with no spaces\. You can also include any of the following characters: \_\+=,\.@\-  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Pattern*: `[\w+=,.@-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-iam-virtualmfadevice-return-values"></a>

### Ref<a name="aws-resource-iam-virtualmfadevice-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `SerialNumber`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-iam-virtualmfadevice-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iam-virtualmfadevice-return-values-fn--getatt-fn--getatt"></a>

`SerialNumber`  <a name="SerialNumber-fn::getatt"></a>
Returns the serial number for the specified `AWS::IAM::VirtualMFADevice` resource\.