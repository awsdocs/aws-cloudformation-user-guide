# AWS::EKS::Addon<a name="aws-resource-eks-addon"></a>

Creates an Amazon EKS add\-on\.

Amazon EKS add\-ons help to automate the provisioning and lifecycle management of common operational software for Amazon EKS clusters\. Amazon EKS add\-ons require clusters running version 1\.18 or later because Amazon EKS add\-ons rely on the Server\-side Apply Kubernetes feature, which is only available in Kubernetes 1\.18 and later\. For more information, see [Amazon EKS add\-ons](https://docs.aws.amazon.com/eks/latest/userguide/eks-add-ons.html) in the *Amazon EKS User Guide*\.

## Syntax<a name="aws-resource-eks-addon-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-eks-addon-syntax.json"></a>

```
{
  "Type" : "AWS::EKS::Addon",
  "Properties" : {
      "[AddonName](#cfn-eks-addon-addonname)" : String,
      "[AddonVersion](#cfn-eks-addon-addonversion)" : String,
      "[ClusterName](#cfn-eks-addon-clustername)" : String,
      "[ResolveConflicts](#cfn-eks-addon-resolveconflicts)" : String,
      "[ServiceAccountRoleArn](#cfn-eks-addon-serviceaccountrolearn)" : String,
      "[Tags](#cfn-eks-addon-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-eks-addon-syntax.yaml"></a>

```
Type: AWS::EKS::Addon
Properties: 
  [AddonName](#cfn-eks-addon-addonname): String
  [AddonVersion](#cfn-eks-addon-addonversion): String
  [ClusterName](#cfn-eks-addon-clustername): String
  [ResolveConflicts](#cfn-eks-addon-resolveconflicts): String
  [ServiceAccountRoleArn](#cfn-eks-addon-serviceaccountrolearn): String
  [Tags](#cfn-eks-addon-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-eks-addon-properties"></a>

`AddonName`  <a name="cfn-eks-addon-addonname"></a>
The name of the add\-on\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AddonVersion`  <a name="cfn-eks-addon-addonversion"></a>
The version of the add\-on\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClusterName`  <a name="cfn-eks-addon-clustername"></a>
The name of the cluster\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[0-9A-Za-z][A-Za-z0-9\-_]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResolveConflicts`  <a name="cfn-eks-addon-resolveconflicts"></a>
How to resolve parameter value conflicts when migrating an existing add\-on to an Amazon EKS add\-on\.  
*Required*: No  
*Type*: String  
*Allowed values*: `NONE | OVERWRITE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceAccountRoleArn`  <a name="cfn-eks-addon-serviceaccountrolearn"></a>
The Amazon Resource Name \(ARN\) of an existing IAM role to bind to the add\-on's service account\. The role must be assigned the IAM permissions required by the add\-on\. If you don't specify an existing IAM role, then the add\-on uses the permissions assigned to the node IAM role\. For more information, see [Amazon EKS node IAM role](https://docs.aws.amazon.com/eks/latest/userguide/create-node-role.html) in the *Amazon EKS User Guide*\.  
To specify an existing IAM role, you must have an IAM OpenID Connect \(OIDC\) provider created for your cluster\. For more information, see [Enabling IAM roles for service accounts on your cluster](https://docs.aws.amazon.com/eks/latest/userguide/enable-iam-roles-for-service-accounts.html) in the *Amazon EKS User Guide*\.
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-eks-addon-tags"></a>
The metadata that you apply to the add\-on to assist with categorization and organization\. Each tag consists of a key and an optional value, both of which you define\. Add\-on tags do not propagate to any other resources associated with the cluster\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-eks-addon-return-values"></a>

### Ref<a name="aws-resource-eks-addon-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "vpc-cni" }` 

For the add\-on `vpc-cni`, `Ref` returns the name of the add\-on\. For example, `<cluster_name>|<vpc-cni>`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-eks-addon-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-eks-addon-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the add\-on, such as `arn:aws:eks:us-west-2:111122223333:addon/1-19/vpc-cni/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx`\.