# AWS::SSMContacts::Contact<a name="aws-resource-ssmcontacts-contact"></a>

The `AWS::SSMContacts::Contact` resource specifies a contact or escalation plan\. Incident Manager contacts are a subset of actions and data types that you can use for managing responder engagement and interaction\.

## Syntax<a name="aws-resource-ssmcontacts-contact-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssmcontacts-contact-syntax.json"></a>

```
{
  "Type" : "AWS::SSMContacts::Contact",
  "Properties" : {
      "[Alias](#cfn-ssmcontacts-contact-alias)" : String,
      "[DisplayName](#cfn-ssmcontacts-contact-displayname)" : String,
      "[Plan](#cfn-ssmcontacts-contact-plan)" : [ Stage, ... ],
      "[Type](#cfn-ssmcontacts-contact-type)" : String
    }
}
```

### YAML<a name="aws-resource-ssmcontacts-contact-syntax.yaml"></a>

```
Type: AWS::SSMContacts::Contact
Properties: 
  [Alias](#cfn-ssmcontacts-contact-alias): String
  [DisplayName](#cfn-ssmcontacts-contact-displayname): String
  [Plan](#cfn-ssmcontacts-contact-plan): 
    - Stage
  [Type](#cfn-ssmcontacts-contact-type): String
```

## Properties<a name="aws-resource-ssmcontacts-contact-properties"></a>

`Alias`  <a name="cfn-ssmcontacts-contact-alias"></a>
The unique and identifiable alias of the contact or escalation plan\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `^[a-z0-9_\-]*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DisplayName`  <a name="cfn-ssmcontacts-contact-displayname"></a>
The full name of the contact or escalation plan\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `255`  
*Pattern*: `^[\p{L}\p{Z}\p{N}_.\-]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Plan`  <a name="cfn-ssmcontacts-contact-plan"></a>
A list of stages\. A contact has an engagement plan with stages that contact specified contact channels\. An escalation plan uses stages that contact specified contacts\.   
*Required*: Yes  
*Type*: List of [Stage](aws-properties-ssmcontacts-contact-stage.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-ssmcontacts-contact-type"></a>
Refers to the type of contact\. A single contact is type `PERSONAL` and an escalation plan is type `ESCALATION`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ESCALATION | PERSONAL`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ssmcontacts-contact-return-values"></a>

### Ref<a name="aws-resource-ssmcontacts-contact-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the resource\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ssmcontacts-contact-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ssmcontacts-contact-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the `Contact` resource, such as `arn:aws:ssm-contacts:us-west-2:123456789012:contact/contactalias`\.