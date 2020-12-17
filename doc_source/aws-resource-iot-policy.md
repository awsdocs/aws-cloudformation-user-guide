# AWS::IoT::Policy<a name="aws-resource-iot-policy"></a>

Use the `AWS::IoT::Policy` resource to declare an AWS IoT policy\. For more information about working with AWS IoT policies, see [Authorization](https://docs.aws.amazon.com/iot/latest/developerguide/authorization.html) in the *AWS IoT Developer Guide*\. 

## Syntax<a name="aws-resource-iot-policy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot-policy-syntax.json"></a>

```
{
  "Type" : "AWS::IoT::Policy",
  "Properties" : {
      "[PolicyDocument](#cfn-iot-policy-policydocument)" : Json,
      "[PolicyName](#cfn-iot-policy-policyname)" : String
    }
}
```

### YAML<a name="aws-resource-iot-policy-syntax.yaml"></a>

```
Type: AWS::IoT::Policy
Properties: 
  [PolicyDocument](#cfn-iot-policy-policydocument): Json
  [PolicyName](#cfn-iot-policy-policyname): String
```

## Properties<a name="aws-resource-iot-policy-properties"></a>

`PolicyDocument`  <a name="cfn-iot-policy-policydocument"></a>
The JSON document that describes the policy\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PolicyName`  <a name="cfn-iot-policy-policyname"></a>
The policy name\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-iot-policy-return-values"></a>

### Ref<a name="aws-resource-iot-policy-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the policy name\. For example:

 `{ "Ref": "MyPolicy" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-iot-policy-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iot-policy-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the AWS IoT policy, such as `arn:aws:iot:us-east-2:123456789012:policy/MyPolicy`\.

## Examples<a name="aws-resource-iot-policy--examples"></a>

### <a name="aws-resource-iot-policy--examples--"></a>

The following example declares an AWS IoT Policy\. This example grants permission to connect to AWS IoT with client ID client1\.

#### JSON<a name="aws-resource-iot-policy--examples----json"></a>

```
            {
   "Type":"AWS::IoT::Policy",
   "Properties":{
      "PolicyDocument":{
         "Version":"2012-10-17",
         "Statement":[
            {
               "Effect":"Allow",
               "Action":[
                  "iot:Connect"
               ],
               "Resource":[
                  "arn:aws:iot:us-east-1:123456789012:client/client1"
               ]
            }
         ]
      },
      "PolicyName":"PolicyName"
   }
}
```

#### YAML<a name="aws-resource-iot-policy--examples----yaml"></a>

```
Type: AWS::IoT::Policy
Properties:
  PolicyDocument:
    Version: '2012-10-17'
    Statement:
    - Effect: Allow
      Action:
      - iot:Connect
      Resource:
      - arn:aws:iot:us-east-1:123456789012:client/client1
  PolicyName: PolicyName
```