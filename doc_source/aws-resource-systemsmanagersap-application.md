# AWS::SystemsManagerSAP::Application<a name="aws-resource-systemsmanagersap-application"></a>

An SAP application registered with AWS Systems Manager for SAP\.

## Syntax<a name="aws-resource-systemsmanagersap-application-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-systemsmanagersap-application-syntax.json"></a>

```
{
  "Type" : "AWS::SystemsManagerSAP::Application",
  "Properties" : {
      "[ApplicationId](#cfn-systemsmanagersap-application-applicationid)" : String,
      "[ApplicationType](#cfn-systemsmanagersap-application-applicationtype)" : String,
      "[Credentials](#cfn-systemsmanagersap-application-credentials)" : [ Credential, ... ],
      "[Instances](#cfn-systemsmanagersap-application-instances)" : [ String, ... ],
      "[SapInstanceNumber](#cfn-systemsmanagersap-application-sapinstancenumber)" : String,
      "[Sid](#cfn-systemsmanagersap-application-sid)" : String,
      "[Tags](#cfn-systemsmanagersap-application-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-systemsmanagersap-application-syntax.yaml"></a>

```
Type: AWS::SystemsManagerSAP::Application
Properties: 
  [ApplicationId](#cfn-systemsmanagersap-application-applicationid): String
  [ApplicationType](#cfn-systemsmanagersap-application-applicationtype): String
  [Credentials](#cfn-systemsmanagersap-application-credentials): 
    - Credential
  [Instances](#cfn-systemsmanagersap-application-instances): 
    - String
  [SapInstanceNumber](#cfn-systemsmanagersap-application-sapinstancenumber): String
  [Sid](#cfn-systemsmanagersap-application-sid): String
  [Tags](#cfn-systemsmanagersap-application-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-systemsmanagersap-application-properties"></a>

`ApplicationId`  <a name="cfn-systemsmanagersap-application-applicationid"></a>
The ID of the application\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `[\w\d]{1,50}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ApplicationType`  <a name="cfn-systemsmanagersap-application-applicationtype"></a>
The type of the application\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `HANA`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Credentials`  <a name="cfn-systemsmanagersap-application-credentials"></a>
The credentials of the SAP application\.  
*Required*: No  
*Type*: List of [Credential](aws-properties-systemsmanagersap-application-credential.md)  
*Maximum*: `20`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Instances`  <a name="cfn-systemsmanagersap-application-instances"></a>
The Amazon EC2 instances on which your SAP application is running\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SapInstanceNumber`  <a name="cfn-systemsmanagersap-application-sapinstancenumber"></a>
The SAP instance number of the application\.  
*Required*: No  
*Type*: String  
*Pattern*: `[0-9]{2}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Sid`  <a name="cfn-systemsmanagersap-application-sid"></a>
The System ID of the application\.  
*Required*: No  
*Type*: String  
*Pattern*: `[A-Z][A-Z0-9]{2}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-systemsmanagersap-application-tags"></a>
The tags on the application\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-systemsmanagersap-application-return-values"></a>

### Ref<a name="aws-resource-systemsmanagersap-application-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a unique identifier for this resource\.

### Fn::GetAtt<a name="aws-resource-systemsmanagersap-application-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-systemsmanagersap-application-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name of the SAP application\.