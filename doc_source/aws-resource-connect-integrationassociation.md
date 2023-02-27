# AWS::Connect::IntegrationAssociation<a name="aws-resource-connect-integrationassociation"></a>

Specifies the association of an AWS resource such as Lex bot \(both v1 and v2\) and Lambda function with an Amazon Connect instance\.

## Syntax<a name="aws-resource-connect-integrationassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-connect-integrationassociation-syntax.json"></a>

```
{
  "Type" : "AWS::Connect::IntegrationAssociation",
  "Properties" : {
      "[InstanceId](#cfn-connect-integrationassociation-instanceid)" : String,
      "[IntegrationArn](#cfn-connect-integrationassociation-integrationarn)" : String,
      "[IntegrationType](#cfn-connect-integrationassociation-integrationtype)" : String
    }
}
```

### YAML<a name="aws-resource-connect-integrationassociation-syntax.yaml"></a>

```
Type: AWS::Connect::IntegrationAssociation
Properties: 
  [InstanceId](#cfn-connect-integrationassociation-instanceid): String
  [IntegrationArn](#cfn-connect-integrationassociation-integrationarn): String
  [IntegrationType](#cfn-connect-integrationassociation-integrationtype): String
```

## Properties<a name="aws-resource-connect-integrationassociation-properties"></a>

`InstanceId`  <a name="cfn-connect-integrationassociation-instanceid"></a>
The Amazon Resource Name \(ARN\) of the instance\.  
*Minimum*: `1`  
*Maximum*: `100`  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IntegrationArn`  <a name="cfn-connect-integrationassociation-integrationarn"></a>
ARN of the integration being associated with the instance\.  
*Minimum*: `1`  
*Maximum*: `140`  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IntegrationType`  <a name="cfn-connect-integrationassociation-integrationtype"></a>
Specifies the integration type to be associated with the instance\.  
*Allowed Values*: `LEX_BOT` \| `LAMBDA_FUNCTION`  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-connect-integrationassociation-return-values"></a>

### Ref<a name="aws-resource-connect-integrationassociation-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-connect-integrationassociation-return-values-fn--getatt"></a>

#### <a name="aws-resource-connect-integrationassociation-return-values-fn--getatt-fn--getatt"></a>

`IntegrationAssociationId`  <a name="IntegrationAssociationId-fn::getatt"></a>
Identifier of the association with an Amazon Connect instance\.

## Examples<a name="aws-resource-connect-integrationassociation--examples"></a>



### Specify a Lex V1 Bot integration<a name="aws-resource-connect-integrationassociation--examples--Specify_a_Lex_V1_Bot_integration"></a>

The following example specifies a Lex V1 Bot integration for an Amazon Connect instance\.

#### YAML<a name="aws-resource-connect-integrationassociation--examples--Specify_a_Lex_V1_Bot_integration--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Specifies a Lex V1 Bot integration for an Amazon Connect instance
Resources:
  IntegrationAssociation:
    Type: AWS::Connect::IntegrationAssociation
    Properties:
      InstanceId: arn:aws:connect:region-name:aws-account-id:instance/instance-arn
      IntegrationType: LEX_BOT
      IntegrationArn: arn:aws:lex:region-name:aws-account-id:bot/bot-name
```

### Specify a Lex V2 Bot integration<a name="aws-resource-connect-integrationassociation--examples--Specify_a_Lex_V2_Bot_integration"></a>

The following example specifies a Lex V2 Bot integration for an Amazon Connect instance\.

#### YAML<a name="aws-resource-connect-integrationassociation--examples--Specify_a_Lex_V2_Bot_integration--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Specifies a Lex V2 Bot integration for an Amazon Connect instance
Resources:
  IntegrationAssociation:
    Type: AWS::Connect::IntegrationAssociation
    Properties:
      InstanceId: arn:aws:connect:region-name:aws-account-id:instance/instance-arn
      IntegrationType: LEX_BOT
      IntegrationArn: arn:aws:lex:region-name:aws-account-id:bot-alias/bot-id/alias-id
```

### Specify a Lambda Function integration<a name="aws-resource-connect-integrationassociation--examples--Specify_a_Lambda_Function_integration"></a>

The following example specifies a Lambda Function for an Amazon Connect instance\.

#### YAML<a name="aws-resource-connect-integrationassociation--examples--Specify_a_Lambda_Function_integration--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Specifies a Lambda Function integration for an Amazon Connect instance
Resources:
  IntegrationAssociation:
    Type: AWS::Connect::IntegrationAssociation
    Properties:
      InstanceId: arn:aws:connect:region-name:aws-account-id:instance/instance-arn
      IntegrationType: LAMBDA_FUNCTION
      IntegrationArn: arn:aws:lambda:region-name:aws-account-id:function:function-arn
```