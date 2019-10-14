# AWS::SecretsManager::Secret<a name="aws-resource-secretsmanager-secret"></a>

The `AWS::SecretsManager::Secret` resource creates a secret and stores it in Secrets Manager\. For more information, see [Secret](https://docs.aws.amazon.com/secretsmanager/latest/userguide/terms-concepts.html#term_secret) in the *AWS Secrets Manager User Guide*, and the [CreateSecret API](https://docs.aws.amazon.com/secretsmanager/latest/apireference/API_CreateSecret.html) in the *AWS Secrets Manager API Reference*\.

To specify the `SecretString` encrypted value for the secret, specify either the `SecretString` or the `GenerateSecretString` property in this resource\. You must specify one or the other, but you can't specify both\. See the [first two examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secret.html#aws-resource-secretsmanager-secret-hardcoded) later in this topic\.

**Note**  
You can't generate a secret with a `SecretBinary` secret value using AWS CloudFormation\. You can create only a `SecretString` text\-based secret value\.

**Note**  
Do not create a dynamic reference that has a backslash `(\)`as the final value\. AWS CloudFormation cannot resolve those references, which results in a resource failure\. 

After you create the basic secret, you can do any of the following:
+ Configure your secret with details of the [Secrets Manager supported database or service](https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html#full-rotation-support) whose credentials are stored in this secret\. 
+ Attach a resource\-based permissions policy to the secret\. To do this, define a [AWS::SecretsManager::ResourcePolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-resourcepolicy.html) resource type\.
+ You can optionally configure a secret to rotate after a specified number of days\. See [AWS::SecretsManager::RotationSchedule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-rotationschedule.html)\.

## Syntax<a name="aws-resource-secretsmanager-secret-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-secretsmanager-secret-syntax.json"></a>

```
{
  "Type" : "AWS::SecretsManager::Secret",
  "Properties" : {
      "[Description](#cfn-secretsmanager-secret-description)" : String,
      "[GenerateSecretString](#cfn-secretsmanager-secret-generatesecretstring)" : [GenerateSecretString](aws-properties-secretsmanager-secret-generatesecretstring.md),
      "[KmsKeyId](#cfn-secretsmanager-secret-kmskeyid)" : String,
      "[Name](#cfn-secretsmanager-secret-name)" : String,
      "[SecretString](#cfn-secretsmanager-secret-secretstring)" : String,
      "[Tags](#cfn-secretsmanager-secret-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-secretsmanager-secret-syntax.yaml"></a>

```
Type: AWS::SecretsManager::Secret
Properties: 
  [Description](#cfn-secretsmanager-secret-description): String
  [GenerateSecretString](#cfn-secretsmanager-secret-generatesecretstring): 
    [GenerateSecretString](aws-properties-secretsmanager-secret-generatesecretstring.md)
  [KmsKeyId](#cfn-secretsmanager-secret-kmskeyid): String
  [Name](#cfn-secretsmanager-secret-name): String
  [SecretString](#cfn-secretsmanager-secret-secretstring): 
    String
  [Tags](#cfn-secretsmanager-secret-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-secretsmanager-secret-properties"></a>

`Description`  <a name="cfn-secretsmanager-secret-description"></a>
Specifies a user\-provided description of the secret\.  
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GenerateSecretString`  <a name="cfn-secretsmanager-secret-generatesecretstring"></a>
A structure that specifies how to generate a random password by using the functionality of the [GetRandomPassword API](https://docs.aws.amazon.com/secretsmanager/latest/apireference/API_GetRandomPassword.html)\. You can return that string directly to use as the secret value, or you can specify both the `SecretStringTemplate` and the `GenerateSecretKey`parameters\. Secrets Manager uses the value in `GenerateSecretKey`parameters\. Secrets Manager uses the value in `GenerateSecretKey` as the key name and combines it with the randomly generated password to make a JSON key\-value pair\. It then inserts that pair into the JSON structure that's specified in the `SecretStringTemplate`parameter\. Secrets Manager stores the completed string as the secret value in the initial version of the secret\. For more information about how to use this property, see [Secrets Manager Secret GenerateSecretString](https://docs.aws.amazon.com/AWSCloudFormation/latest/userguide/aws-properties-secretsmanager-secret-generatesecretstring.html) and the [first example](https://docs.aws.amazon.com/AWSCloudFormation/latest/userguide/aws-resource-secretsmanager-secret.html#aws-resource-secretsmanager-secret-generated) in the following Examples section\.  
Either `SecretString` or `SecretBinary` must have a value, but not both\. They cannot both be empty\.  
*Required*: No  
*Type*: [GenerateSecretString](aws-properties-secretsmanager-secret-generatesecretstring.md)  
*Minimum*: `0`  
*Maximum*: `7168`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-secretsmanager-secret-kmskeyid"></a>
Specifies Key ID or alias of the AWS KMS customer master key \(CMK\) that's used to encrypt the `SecretString` or `SecretBinary` values for versions of this secret\. If you don't specify this value, then Secrets Manager defaults to the AWS account's CMK \(the one named `aws/secretsmanager`\)\. If an AWS KMS CMK with that name doesn't yet exist, Secrets Manager creates it for you automatically the first time it needs to encrypt a version's `SecretString` or `SecretBinary` fields\.  
You can use the account's default CMK to encrypt and decrypt only if you call this operation using credentials from the same account that owns the secret\.
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-secretsmanager-secret-name"></a>
The friendly name of the secret\. You can use forward slashes in the name to represent a path hierarchy\. For example, `/prod/databases/dbserver1` could represent the secret for a server named `dbserver1` in the folder `databases` in the folder `prod`\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecretString`  <a name="cfn-secretsmanager-secret-secretstring"></a>
Specifies a literal string to use as the secret value for the secret\. You can use any text you like, but remember that Lambda rotation functions require a specific JSON structure to be present in this field\.   
Alternatively, instead of hardcoding the password in this string parameter, we recommend that you use the `GenerateSecretString` parameter instead\.  
You must specify either `SecretString` or `GenerateSecretString`, but not both\.  
Stack updates that modify a `SecretString` property, will immediately change the secret's value\. 
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-secretsmanager-secret-tags"></a>
The list of user\-defined tags that are associated with the secret\. Use tags to manage your AWS resources\. For additional information about tags, see [TagResource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-secretsmanager-secret-return-values"></a>

### Ref<a name="aws-resource-secretsmanager-secret-return-values-ref"></a>

When you pass the logical ID of an `AWS::SecretsManager::Secret` resource to the intrinsic `Ref` function, the function returns the ARN of the secret being configured, such as:

`arn:aws:secretsmanager:us-west-2:123456789012:secret:my-path/my-secret-name-1a2b3c`

If you know the ARN of a secret, you can reference a secret that you created in one part of the stack template from within the definition of another resource in the same template\. You typically use the `Ref` function with the [AWS::SecretsManager::SecretTargetAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secrettargetattachment.html) resource type to get references to both the secret and its associated database\.

For more information about using the `Ref` function, see [Ref](AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

## Examples<a name="aws-resource-secretsmanager-secret--examples"></a>

### Creating a Secret with a Dynamically Generated Password<a name="aws-resource-secretsmanager-secret--examples--Creating_a_Secret_with_a_Dynamically_Generated_Password"></a>

The following example creates a secret, constructing the secret value from a string template that's combined with a dynamically generated random password\. The result of this example is a `SecretString` value that looks like the following:

`{"username": "test-user", "password": "rzDtILsQNfmmHwkJBPsTVhkRvWRtSn" )`

#### JSON<a name="aws-resource-secretsmanager-secret--examples--Creating_a_Secret_with_a_Dynamically_Generated_Password--json"></a>

```
{
  "MySecretA": {
    "Type": "AWS::SecretsManager::Secret",
    "Properties": {
      "Name": "MySecretForAppA",
      "Description": "This secret has a dynamically generated secret password.",
      "GenerateSecretString": {
        "SecretStringTemplate": "{\"username\":\"test-user\"}",
        "GenerateStringKey": "password",
        "PasswordLength": 30,
        "ExcludeCharacters": "\"@/\\"
      },
      "Tags": [
        {
          "Key": "AppName",
          "Value": "AppA"
        }
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-secretsmanager-secret--examples--Creating_a_Secret_with_a_Dynamically_Generated_Password--yaml"></a>

```
#This is a Secret resource with a randomly generated password in its SecretString JSON.
MySecretA:
  Type: 'AWS::SecretsManager::Secret'
  Properties:
    Name: MySecretForAppA
    Description: "This secret has a dynamically generated secret password."
    GenerateSecretString:
      SecretStringTemplate: '{"username": "test-user"}'
      GenerateStringKey: "password"
      PasswordLength: 30
      ExcludeCharacters: '"@/\'
    Tags:
      -
        Key: AppName
        Value: AppA
```

### Creating a Secret with a Hardcoded Password<a name="aws-resource-secretsmanager-secret--examples--Creating_a_Secret_with_a_Hardcoded_Password"></a>

The following example creates a secret and provides the secret value as a literal string that's stored in the secret\. We recommend that you don't hardcode your password this way\. Instead use the [SecretsManager Secret GenerateSecretString](https://docs.aws.amazon.com/AWSCloudFormation/latest/ug/aws-properties-secretsmanager-secret-generatesecretstring.html) property\. See the previous example for the recommended option\.

#### JSON<a name="aws-resource-secretsmanager-secret--examples--Creating_a_Secret_with_a_Hardcoded_Password--json"></a>

```
{
  "MySecretB": {
    "Type": "AWS::SecretsManager::Secret",
    "Properties": {
      "Name": "MySecretForAppB",
      "Description": "This secret has a hardcoded password in SecretString (use GenerateSecretString instead)",
      "SecretString": "{\"username\":\"MasterUsername\",\"password\":\"secret-password\"}",
      "Tags": [
        {
          "Key": "AppName",
          "Value": "AppB"
        }
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-secretsmanager-secret--examples--Creating_a_Secret_with_a_Hardcoded_Password--yaml"></a>

```
  # This is another secret that has its password hardcoded into the template (NOT RECOMMENDED)
  MySecretB:
    Type: 'AWS::SecretsManager::Secret'
    Properties:
      Name: MySecretForAppB
      Description: This secret has a hardcoded password in SecretString (use GenerateSecretString instead)
      SecretString: '{"username":"MasterUsername","password":"secret-password"}'
      Tags:
        -
          Key: AppName
          Value: AppB
```

## See Also<a name="aws-resource-secretsmanager-secret--seealso"></a>
+  [CreateSecret](https://docs.aws.amazon.com/secretsmanager/latest/apireference/API_CreateSecret.html) API in the AWS Secrets Manager API Reference
+  [Secret](https://docs.aws.amazon.com/secretsmanager/latest/userguide/terms-concepts.html#term_secret) in the AWS Secrets Manager User Guide
+  [AWS::SecretsManager::ResourcePolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-resourcepolicy.html)
+  [AWS::SecretsManager::RotationSchedule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-rotationschedule.html)
+  [AWS::SecretsManager::SecretTargetAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secrettargetattachment.html)
