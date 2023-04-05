# AWS::VpcLattice::ServiceNetwork<a name="aws-resource-vpclattice-servicenetwork"></a>

Creates a service network\. A service network is a logical boundary for a collection of services\. You can associate services and VPCs with a service network\.

For more information, see [Service networks](https://docs.aws.amazon.com/vpc-lattice/latest/ug/service-networks.html) in the *Amazon VPC Lattice User Guide*\.

## Syntax<a name="aws-resource-vpclattice-servicenetwork-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-vpclattice-servicenetwork-syntax.json"></a>

```
{
  "Type" : "AWS::VpcLattice::ServiceNetwork",
  "Properties" : {
      "[AuthType](#cfn-vpclattice-servicenetwork-authtype)" : String,
      "[Name](#cfn-vpclattice-servicenetwork-name)" : String,
      "[Tags](#cfn-vpclattice-servicenetwork-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-vpclattice-servicenetwork-syntax.yaml"></a>

```
Type: AWS::VpcLattice::ServiceNetwork
Properties: 
  [AuthType](#cfn-vpclattice-servicenetwork-authtype): String
  [Name](#cfn-vpclattice-servicenetwork-name): String
  [Tags](#cfn-vpclattice-servicenetwork-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-vpclattice-servicenetwork-properties"></a>

`AuthType`  <a name="cfn-vpclattice-servicenetwork-authtype"></a>
The type of IAM policy\.  
+ `NONE`: The resource does not use an IAM policy\. This is the default\.
+ `AWS_IAM`: The resource uses an IAM policy\. When this type is used, auth is enabled and an auth policy is required\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-vpclattice-servicenetwork-name"></a>
The name of the service network\. The name must be unique to the account\. The valid characters are a\-z, 0\-9, and hyphens \(\-\)\. You can't use a hyphen as the first or last character, or immediately after another hyphen\.  
If you don't specify a name, CloudFormation generates one\. However, if you specify a name, and later want to replace the resource, you must specify a new name\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-vpclattice-servicenetwork-tags"></a>
The tags for the service network\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-vpclattice-servicenetwork-return-values"></a>

### Ref<a name="aws-resource-vpclattice-servicenetwork-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the service network\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-vpclattice-servicenetwork-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-vpclattice-servicenetwork-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the service network\.

`CreatedAt`  <a name="CreatedAt-fn::getatt"></a>
The date and time that the service network was created, specified in ISO\-8601 format\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the service network\.

`LastUpdatedAt`  <a name="LastUpdatedAt-fn::getatt"></a>
The date and time of the last update, specified in ISO\-8601 format\.