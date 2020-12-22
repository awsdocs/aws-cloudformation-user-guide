# AWS::IoTSiteWise::AccessPolicy<a name="aws-resource-iotsitewise-accesspolicy"></a>

Creates an access policy that grants the specified identity \(AWS SSO user, AWS SSO group, or IAM user\) access to the specified AWS IoT SiteWise Monitor portal or project resource\.

## Syntax<a name="aws-resource-iotsitewise-accesspolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotsitewise-accesspolicy-syntax.json"></a>

```
{
  "Type" : "AWS::IoTSiteWise::AccessPolicy",
  "Properties" : {
      "[AccessPolicyIdentity](#cfn-iotsitewise-accesspolicy-accesspolicyidentity)" : AccessPolicyIdentity,
      "[AccessPolicyPermission](#cfn-iotsitewise-accesspolicy-accesspolicypermission)" : String,
      "[AccessPolicyResource](#cfn-iotsitewise-accesspolicy-accesspolicyresource)" : AccessPolicyResource
    }
}
```

### YAML<a name="aws-resource-iotsitewise-accesspolicy-syntax.yaml"></a>

```
Type: AWS::IoTSiteWise::AccessPolicy
Properties: 
  [AccessPolicyIdentity](#cfn-iotsitewise-accesspolicy-accesspolicyidentity): 
    AccessPolicyIdentity
  [AccessPolicyPermission](#cfn-iotsitewise-accesspolicy-accesspolicypermission): String
  [AccessPolicyResource](#cfn-iotsitewise-accesspolicy-accesspolicyresource): 
    AccessPolicyResource
```

## Properties<a name="aws-resource-iotsitewise-accesspolicy-properties"></a>

`AccessPolicyIdentity`  <a name="cfn-iotsitewise-accesspolicy-accesspolicyidentity"></a>
The identity for this access policy\. Choose an AWS SSO user, an AWS SSO group, or an IAM user\.  
*Required*: Yes  
*Type*: [AccessPolicyIdentity](aws-properties-iotsitewise-accesspolicy-accesspolicyidentity.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AccessPolicyPermission`  <a name="cfn-iotsitewise-accesspolicy-accesspolicypermission"></a>
The permission level for this access policy\. Choose either a `ADMINISTRATOR` or `VIEWER`\. Note that a project `ADMINISTRATOR` is also known as a project owner\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AccessPolicyResource`  <a name="cfn-iotsitewise-accesspolicy-accesspolicyresource"></a>
The AWS IoT SiteWise Monitor resource for this access policy\. Choose either a portal or a project\.  
*Required*: Yes  
*Type*: [AccessPolicyResource](aws-properties-iotsitewise-accesspolicy-accesspolicyresource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iotsitewise-accesspolicy-return-values"></a>

### Ref<a name="aws-resource-iotsitewise-accesspolicy-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `AccessPolicyId`\.

### Fn::GetAtt<a name="aws-resource-iotsitewise-accesspolicy-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iotsitewise-accesspolicy-return-values-fn--getatt-fn--getatt"></a>

`AccessPolicyArn`  <a name="AccessPolicyArn-fn::getatt"></a>
The [ARN](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) of the access policy, which has the following format\.  
`arn:${Partition}:iotsitewise:${Region}:${Account}:access-policy/${AccessPolicyId}`  
For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

`AccessPolicyId`  <a name="AccessPolicyId-fn::getatt"></a>
The ID of the access policy\.  
For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.