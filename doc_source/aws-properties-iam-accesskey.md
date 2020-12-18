# AWS::IAM::AccessKey<a name="aws-properties-iam-accesskey"></a>

 Creates a new AWS secret access key and corresponding AWS access key ID for the specified user\. The default status for new keys is `Active`\.

If you do not specify a user name, IAM determines the user name implicitly based on the AWS access key ID signing the request\. This operation works for access keys under the AWS account\. Consequently, you can use this operation to manage AWS account root user credentials\. This is true even if the AWS account has no associated users\.

 For information about limits on the number of keys you can create, see [Limitations on IAM Entities](https://docs.aws.amazon.com/IAM/latest/UserGuide/LimitationsOnEntities.html) in the *IAM User Guide*\.

**Important**  
To ensure the security of your AWS account, the secret access key is accessible only during key and user creation\. You must save the key \(for example, in a text file\) if you want to be able to access it again\. If a secret key is lost, you can delete the access keys for the associated user and then create new keys\.

## Syntax<a name="aws-properties-iam-accesskey-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iam-accesskey-syntax.json"></a>

```
{
  "Type" : "AWS::IAM::AccessKey",
  "Properties" : {
      "[Serial](#cfn-iam-accesskey-serial)" : Integer,
      "[Status](#cfn-iam-accesskey-status)" : String,
      "[UserName](#cfn-iam-accesskey-username)" : String
    }
}
```

### YAML<a name="aws-properties-iam-accesskey-syntax.yaml"></a>

```
Type: AWS::IAM::AccessKey
Properties: 
  [Serial](#cfn-iam-accesskey-serial): Integer
  [Status](#cfn-iam-accesskey-status): String
  [UserName](#cfn-iam-accesskey-username): String
```

## Properties<a name="aws-properties-iam-accesskey-properties"></a>

`Serial`  <a name="cfn-iam-accesskey-serial"></a>
This value is specific to CloudFormation and can only be *incremented*\. Incrementing this value notifies CloudFormation that you want to rotate your access key\. When you update your stack, CloudFormation will replace the existing access key with a new key\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Status`  <a name="cfn-iam-accesskey-status"></a>
The status of the access key\. `Active` means that the key is valid for API calls, while `Inactive` means it is not\.   
*Required*: No  
*Type*: String  
*Allowed values*: `Active | Inactive`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserName`  <a name="cfn-iam-accesskey-username"></a>
The name of the IAM user that the new key will belong to\.  
This parameter allows \(through its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of upper and lowercase alphanumeric characters with no spaces\. You can also include any of the following characters: \_\+=,\.@\-  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\w+=,.@-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-properties-iam-accesskey-return-values"></a>

### Ref<a name="aws-properties-iam-accesskey-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `AccessKeyId`\. For example: `AKIAIOSFODNN7EXAMPLE`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-properties-iam-accesskey-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-properties-iam-accesskey-return-values-fn--getatt-fn--getatt"></a>

`SecretAccessKey`  <a name="SecretAccessKey-fn::getatt"></a>
Returns the secret access key for the specified AWS::IAM::AccessKey resource\. For example: wJalrXUtnFEMI/K7MDENG/bPxRfiCYzEXAMPLEKEY\.

## Examples<a name="aws-properties-iam-accesskey--examples"></a>

### Access Key<a name="aws-properties-iam-accesskey--examples--Access_Key"></a>

In this example, create an access key for the user named "MyUser"\.

#### JSON<a name="aws-properties-iam-accesskey--examples--Access_Key--json"></a>

```
{
   "AWSTemplateFormatVersion": "2010-09-09",
   "Resources": {
      "CFNKeys" : {
         "Type" : "AWS::IAM::AccessKey",
         "Properties" : {
           "UserName" : { "Ref": "MyUser" }
         }
      }
   }            
}
```

#### YAML<a name="aws-properties-iam-accesskey--examples--Access_Key--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  CFNKeys:
    Type: AWS::IAM::AccessKey
    Properties:
      UserName:
        Ref: MyUser
```

## See also<a name="aws-properties-iam-accesskey--seealso"></a>
+ To view `AWS::IAM::AccessKey` template example snippets, see [Declaring an IAM Access Key Resource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-iam.html#scenario-iam-accesskey)\. 
+  [CreateAccessKey](https://docs.aws.amazon.com/IAM/latest/APIReference/API_CreateAccessKey.html) in the *AWS Identity and Access Management API Reference* 

