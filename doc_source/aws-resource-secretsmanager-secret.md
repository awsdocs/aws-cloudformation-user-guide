# AWS::SecretsManager::Secret<a name="aws-resource-secretsmanager-secret"></a>

The `AWS::SecretsManager::Secret` resource creates a secret and stores it in Secrets Manager\. For more information, see [Secret](https://docs.aws.amazon.com/secretsmanager/latest/userguide/terms-concepts.html#term_secret) in the *AWS Secrets Manager User Guide*, and the [CreateSecret API](https://docs.aws.amazon.com/secretsmanager/latest/apireference/API_CreateSecret.html) in the *AWS Secrets Manager API Reference*\.

To specify the `SecretString` encrypted value for the secret, specify either the `SecretString` or the `GenerateSecretString` property in this resource\. You must specify one or the other, but you can't specify both\. See the [first two examples](#aws-resource-secretsmanager-secret-hardcoded) later in this topic\.

**Note**  
You can't generate a secret with a `SecretBinary` secret value using AWS CloudFormation\. You can create only a `SecretString` text\-based secret value\.

**Note**  
Do not create a dynamic reference that has a backslash \(\\\) as the final value\. AWS CloudFormation cannot resolve those references, which results in a resource failure\.

After you create the basic secret, you can do any of the following:
+ Configure your secret with details of the [Secrets Manager supported database or service](https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html#full-rotation-support) whose credentials are stored in this secret\. After creating the secret, perform these steps in the template:
  + Define the database or service\. In the definition of the database or service, you can retrieve the credentials in the secret by using the "dynamic reference" syntax that's similar to the following example\. Adjust as appropriate for your service\. The following YAML example is appropriate for an Amazon RDS MySQL DB instance\. It gets the `username` and `password` from the `SecretString` field of the secret named `MySecretA`\. This secret already exists \(before running the AWS CloudFormation template\) and uses those credentials as the `MasterUsername` and `MasterUserPassword` for the new database:

    ```
        MasterUsername: '{{resolve:secretsmanager:MySecretA:SecretString:username}}'
        MasterUserPassword: '{{resolve:secretsmanager:MySecretA:SecretString:password}}'
    ```

    Alternatively, if you want to refer to the username and password in a secret that is defined in the same template, then you can use the [Ref](intrinsic-function-reference-ref.md) intrinsic function to retrieve the secret name using the template's logical ID for the secret\. The following YAML example shows how to reference components of a secret that is defined somewhere else in the same template\. It uses the `Fn::Join` intrinsic function to concatenate the parts of the string with the retrieved secret values to make the complete argument string\.

    ```
        MasterUsername: !Join ['', ['{{resolve:secretsmanager:', !Ref MySecret, ':SecretString:username}}' ]]
        MasterUserPassword: !Join ['', ['{{resolve:secretsmanager:', !Ref MySecret, ':SecretString:password}}' ]]
    ```

    The following example shows the same thing in JSON format:

    ```
        "MasterUsername": {"Fn::Join": [ "", 
    ["{{resolve:secretsmanager:",{"Ref": "MySecret"},":SecretString:username}}"]
     ] },
        "MasterUserPassword": {"Fn::Join": [
     "", ["{{resolve:secretsmanager:",{"Ref": "MySecret"},":SecretString:password}}"]
     ] },
    ```

    For more information about using dynamic references to values in other services' resources, see [Using Dynamic References to Specify Template Values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/dynamic-refrences.html)\.
**Important**  
Be careful not to use such resolvable references for sensitive information like the username and password in any location that is logged to avoid accidentally exposing those details\. AWS CloudFormation explicitly prevents logging the `MasterUsername` and `MasterUserPassword` of an Amazon RDS database instance for this reason\.
  + Update the secret to add the connection details of the database or service to the secret value\. To do this, define a [AWS::SecretsManager::SecretTargetAttachment](aws-resource-secretsmanager-secrettargetattachment.md) resource and associate it with both the secret and the database or service\.
+ Attach a resource\-based permissions policy to the secret\. To do this, define a [AWS::SecretsManager::ResourcePolicy](aws-resource-secretsmanager-resourcepolicy.md) resource type\.
+ You can optionally configure a secret to rotate after a specified number of days\. See [AWS::SecretsManager::RotationSchedule](aws-resource-secretsmanager-rotationschedule.md)\.

**Topics**
+ [Syntax](#aws-resource-secretsmanager-secret-syntax)
+ [Properties](#aws-resource-secretsmanager-secret-properties)
+ [Return Values](#aws-resource-secretsmanager-secret-returnvalues)
+ [Examples](#aws-resource-secretsmanager-secret-examples)
+ [See Also](#aws-resource-secretsmanager-secret-seealso)
+ [Secrets Manager Secret GenerateSecretString](aws-properties-secretsmanager-secret-generatesecretstring.md)

## Syntax<a name="aws-resource-secretsmanager-secret-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-secretsmanager-secret-syntax.json"></a>

```
{
  "Type" : "AWS::SecretsManager::Secret",
  "Properties" : {
    "[Description](#cfn-secretsmanager-secret-description)" : String,
    "[KmsKeyId](#cfn-secretsmanager-secret-kmskeyid)" : String,
    "[SecretString](#cfn-secretsmanager-secret-secretstring)" : String,
    "[GenerateSecretString](#cfn-secretsmanager-secret-generatesecretstring)" : [*GenerateSecretString*](aws-properties-secretsmanager-secret-generatesecretstring.md),
    "[Tags](#cfn-secretsmanager-secret-tags)" : [ [*Tag*](aws-properties-resource-tags.md), ... ],
    "[Name](#cfn-secretsmanager-secret-name)" : String
  }
}
```

### YAML<a name="aws-resource-secretsmanager-secret-syntax.yaml"></a>

```
Type: "AWS::SecretsManager::Secret"
Properties:
  [Description](#cfn-secretsmanager-secret-description): String
  [KmsKeyId](#cfn-secretsmanager-secret-kmskeyid): String
  [SecretString](#cfn-secretsmanager-secret-secretstring): String
  [GenerateSecretString](#cfn-secretsmanager-secret-generatesecretstring): 
    [*GenerateSecretString*](aws-properties-secretsmanager-secret-generatesecretstring.md)
  [Tags](#cfn-secretsmanager-secret-tags): 
    - [*Tag*](aws-properties-resource-tags.md)
  [Name](#cfn-secretsmanager-secret-name): String
```

## Properties<a name="aws-resource-secretsmanager-secret-properties"></a>

`Description`  <a name="cfn-secretsmanager-secret-description"></a>
 Specifies a user\-provided description of the secret\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`KmsKeyId`  <a name="cfn-secretsmanager-secret-kmskeyid"></a>
Specifies the ARN, Key ID, or alias of the AWS KMS customer master key \(CMK\) that's used to encrypt the secret values for versions of this secret\. If you don't specify this value, then Secrets Manager defaults to the AWS account's default CMK \(the one named `aws/secretsmanager`\)\. If an AWS KMS CMK with that name doesn't yet exist, Secrets Manager creates it for you automatically the first time it needs to encrypt a version's secret value fields\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SecretString`  <a name="cfn-secretsmanager-secret-secretstring"></a>
Specifies a literal string to use as the secret value in the initial version of this secret\. You can specify any text you like, but remember that Lambda rotation functions require a specific JSON structure to be present in this field\.  
Alternatively, instead of hardcoding the password in this string parameter, we recommend that you use the `GenerateSecretString` parameter instead\.  
You must specify either `SecretString` or `GenerateSecretString`, but not both\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`GenerateSecretString`  <a name="cfn-secretsmanager-secret-generatesecretstring"></a>
A structure that specifies how to generate a random password by using the functionality of the [GetRandomPassword API](https://docs.aws.amazon.com/secretsmanager/latest/apireference/API_GetRandomPassword.html)\. You can return that string directly to use as the secret value, or you can alternatively also specify both the `SecretStringTemplate` and the `GenerateSecretKey` parameters\. Secrets Manager uses the value in `GenerateSecretKey` as the key name and combines it with the randomly generated password to make a JSON key\-value pair\. It then inserts that pair into the JSON structure that's specified in the `SecretStringTemplate` parameter\. Secrets Manager stores the completed string as the secret value in the initial version of the secret\. For more information about how to use this property, see [Secrets Manager Secret GenerateSecretString](aws-properties-secretsmanager-secret-generatesecretstring.md) and the [first example](#aws-resource-secretsmanager-secret-generated) in the following **Examples** section\.  
You must specify either `SecretString` or `GenerateSecretString`, but not both\.  
*Required*: No  
*Type*: [Secrets Manager Secret GenerateSecretString](aws-properties-secretsmanager-secret-generatesecretstring.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Tags`  <a name="cfn-secretsmanager-secret-tags"></a>
Specifies an arbitrary set of tags \(key–value pairs\) to associate with this secret\. Use tags to manage your AWS resources\.  
*Required*: No  
*Type*: List of [Resource Tag](aws-properties-resource-tags.md) property types  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-secretsmanager-secret-name"></a>
Specifies the friendly name of the new secret\. If a `Name` parameter isn't specified, then Secrets Manager generates a name based on the logical resource ID of the secret in the AWS CloudFormation template\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="aws-resource-secretsmanager-secret-returnvalues"></a>

### Ref<a name="aws-resource-secretsmanager-secret-ref"></a>

When you pass the logical ID of an `AWS::SecretsManager::Secret` resource to the intrinsic `Ref` function, the function returns the ARN of the secret being configured, such as:

`arn:aws:secretsmanager:us-west-2:123456789012:secret:my-path/my-secret-name-1a2b3c`

This enables you to reference a secret that you create in one part of the stack template from within the definition of another resource later, in the same template\. You typically use the `Ref` function with the [AWS::SecretsManager::SecretTargetAttachment](aws-resource-secretsmanager-secrettargetattachment.md) resource type to get references to both the secret and its associated database\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-secretsmanager-secret-examples"></a>

**Note**  
The JSON specification doesn't allow any kind of comments\. See the YAML example for comments\.

### Creating a Secret with a Dynamically Generated Password<a name="aws-resource-secretsmanager-secret-generated"></a>

The following example creates a secret, constructing the secret value from a string template that's combined with a dynamically generated random password\. The result of this example is a `SecretString` value that looks like the following:

```
{"username": "test-user", "password": "rzDtILsQNfmmHwkJBPsTVhkRvWRtSn" }
```

For more information, see [Secrets Manager Secret GenerateSecretString](aws-properties-secretsmanager-secret-generatesecretstring.md)\.

#### JSON<a name="aws-resource-secretsmanager-secret-generated.json"></a>

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

#### YAML<a name="aws-resource-secretsmanager-secret-generated.yaml"></a>

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

### Creating a Secret with a Hardcoded Password<a name="aws-resource-secretsmanager-secret-hardcoded"></a>

The following example creates a secret and provides the secret value as a literal string that's stored in the secret\. **We recommend that you don't hardcode your password this way\.** Instead, use the [Secrets Manager Secret GenerateSecretString](aws-properties-secretsmanager-secret-generatesecretstring.md) property\. See the previous example for that improved option\.

#### JSON<a name="aws-resource-secretsmanager-secret-hardcoded.json"></a>

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

#### YAML<a name="aws-resource-secretsmanager-secret-hardcoded.yaml"></a>

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

## See Also<a name="aws-resource-secretsmanager-secret-seealso"></a>
+ [CreateSecret](https://docs.aws.amazon.com/secretsmanager/latest/apireference/API_CreateSecret.html) API in the AWS Secrets Manager API Reference
+ [Secret](https://docs.aws.amazon.com/secretsmanager/latest/userguide/terms-concepts.html#term_secret) in the *AWS Secrets Manager User Guide*
+ [AWS::SecretsManager::SecretTargetAttachment](aws-resource-secretsmanager-secrettargetattachment.md)
+ [AWS::SecretsManager::RotationSchedule](aws-resource-secretsmanager-rotationschedule.md)
+ [AWS::SecretsManager::ResourcePolicy](aws-resource-secretsmanager-resourcepolicy.md)