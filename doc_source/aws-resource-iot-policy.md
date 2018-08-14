# AWS::IoT::Policy<a name="aws-resource-iot-policy"></a>

Use the `AWS::IoT::Policy` resource to declare an AWS IoT policy\.

For information about working with AWS IoT policies, see [Authorization](http://docs.aws.amazon.com/iot/latest/developerguide/authorization.html) in the *AWS IoT Developer Guide*\.

## Syntax<a name="aws-resource-iot-policy-syntax"></a>

### JSON<a name="aws-resource-iot-policy-syntax.json"></a>

```
{
   "Type": "AWS::IoT::Policy",
   "Properties": {
      "[PolicyDocument](#cfn-iot-policy-policydocument)": JSON object,
      "[PolicyName](#cfn-iot-policy-policyname)": String
    }
}
```

### YAML<a name="aws-resource-iot-policy-syntax.yaml"></a>

```
Type: "AWS::IoT::Policy"
Properties:
  [PolicyDocument](#cfn-iot-policy-policydocument): JSON object
  [PolicyName](#cfn-iot-policy-policyname): String
```

## Properties<a name="aws-resource-iot-policy-properties"></a>

`PolicyDocument`  <a name="cfn-iot-policy-policydocument"></a>
The JSON document that describes the policy\.  
*Required*: Yes  
*Type*: JSON object  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`PolicyName`  <a name="cfn-iot-policy-policyname"></a>
The name \(the physical ID\) of the AWS IoT policy\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="aws-resource-iot-policy-returnvalues"></a>

### Ref<a name="aws-resource-iot-policy-ref"></a>

When you provide the logical ID of this resource to the `Ref` intrinsic function, `Ref` returns the policy name\. For example:

```
{ "Ref": "MyPolicy" }
```

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="aws-resource-iot-policy-getatt"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Arn`  
The Amazon Resource Name \(ARN\) of the AWS IoT policy, such as `arn:aws:iot:us-east-2:123456789012:policy/MyPolicy`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Example<a name="aws-resource-iot-policy-examples"></a>

The following example declares an AWS IoT policy\.

### JSON<a name="aws-resource-iot-policy-example.json"></a>

```
{
   "AWSTemplateFormatVersion": "2010-09-09",
   "Resources": {
      "MyPolicy": {
         "Type": "AWS::IoT::Policy",
         "Properties": {
            "PolicyName": {
               "Ref": "NameParameter"
            },
            "PolicyDocument": {
               "Version": "2012-10-17",
               "Statement": [{
                  "Effect": "Allow",
                  "Action": [
                     "iot:Connect"
                  ],
                  "Resource": [
                     "*"
                  ]
               }]
            }
         }
      }
   },
   "Parameters": {
      "NameParameter": {
         "Type": "String"
      }
   }
}
```

### YAML<a name="aws-resource-iot-policy-example.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
  MyPolicy: 
    Type: "AWS::IoT::Policy"
    Properties: 
      PolicyName: 
        Ref: "NameParameter"
      PolicyDocument: 
        Version: "2012-10-17"
        Statement: 
          - 
            Effect: "Allow"
            Action: 
              - "iot:Connect"
            Resource: 
              - "*"
Parameters: 
  NameParameter: 
    Type: "String"
```