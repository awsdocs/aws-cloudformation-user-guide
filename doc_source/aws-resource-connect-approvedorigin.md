# AWS::Connect::ApprovedOrigin<a name="aws-resource-connect-approvedorigin"></a>

The approved origin for the instance\.

## Syntax<a name="aws-resource-connect-approvedorigin-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-connect-approvedorigin-syntax.json"></a>

```
{
  "Type" : "AWS::Connect::ApprovedOrigin",
  "Properties" : {
      "[InstanceId](#cfn-connect-approvedorigin-instanceid)" : String,
      "[Origin](#cfn-connect-approvedorigin-origin)" : String
    }
}
```

### YAML<a name="aws-resource-connect-approvedorigin-syntax.yaml"></a>

```
Type: AWS::Connect::ApprovedOrigin
Properties: 
  [InstanceId](#cfn-connect-approvedorigin-instanceid): String
  [Origin](#cfn-connect-approvedorigin-origin): String
```

## Properties<a name="aws-resource-connect-approvedorigin-properties"></a>

`InstanceId`  <a name="cfn-connect-approvedorigin-instanceid"></a>
The Amazon Resource Name \(ARN\) of the instance\.  
*Minimum*: `1`  
*Maximum*: `100`  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Origin`  <a name="cfn-connect-approvedorigin-origin"></a>
Domain name to be added to the allow\-list of the instance\.  
*Maximum*: `267`  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-connect-approvedorigin-return-values"></a>

### Ref<a name="aws-resource-connect-approvedorigin-return-values-ref"></a>

## Examples<a name="aws-resource-connect-approvedorigin--examples"></a>



### Specify an Approved Origin for an Amazon Connect instance<a name="aws-resource-connect-approvedorigin--examples--Specify_an_Approved_Origin_for_an_Amazon_Connect_instance"></a>

The following example specifies an Approved Origin for an Amazon Connect instance\.

#### YAML<a name="aws-resource-connect-approvedorigin--examples--Specify_an_Approved_Origin_for_an_Amazon_Connect_instance--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Specifies an Approved Origin for an Amazon Connect instance
Resources:
  ApprovedOrigin:
    Type: AWS::Connect::ApprovedOrigin
    Properties:
      InstanceId: arn:aws:connect:region-name:aws-account-id:instance/instance-arn
      Origin: "https://aws.amazon.com"
```