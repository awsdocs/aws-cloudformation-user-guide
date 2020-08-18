# AWS::EKS::Nodegroup LaunchTemplateSpecification<a name="aws-properties-eks-nodegroup-launchtemplatespecification"></a>

An object representing a node group launch template specification\. The launch template cannot include [ `SubnetId` ](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateNetworkInterface.html), [ `IamInstanceProfile` ](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_IamInstanceProfile.html), [ `RequestSpotInstances` ](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_RequestSpotInstances.html), [ `HibernationOptions` ](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_HibernationOptionsRequest.html), or [ `TerminateInstances` ](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_TerminateInstances.html), or the node group deployment or update will fail\. For more information about launch templates, see [ `CreateLaunchTemplate` ](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateLaunchTemplate.html) in the Amazon EC2 API Reference\. For more information about using launch templates with Amazon EKS, see [Launch template support](https://docs.aws.amazon.com/eks/latest/userguide/launch-templates.html) in the Amazon EKS User Guide\.

Specify either `name` or `id`, but not both\.

## Syntax<a name="aws-properties-eks-nodegroup-launchtemplatespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-eks-nodegroup-launchtemplatespecification-syntax.json"></a>

```
{
  "[Id](#cfn-eks-nodegroup-launchtemplatespecification-id)" : String,
  "[Name](#cfn-eks-nodegroup-launchtemplatespecification-name)" : String,
  "[Version](#cfn-eks-nodegroup-launchtemplatespecification-version)" : String
}
```

### YAML<a name="aws-properties-eks-nodegroup-launchtemplatespecification-syntax.yaml"></a>

```
  [Id](#cfn-eks-nodegroup-launchtemplatespecification-id): String
  [Name](#cfn-eks-nodegroup-launchtemplatespecification-name): String
  [Version](#cfn-eks-nodegroup-launchtemplatespecification-version): String
```

## Properties<a name="aws-properties-eks-nodegroup-launchtemplatespecification-properties"></a>

`Id`  <a name="cfn-eks-nodegroup-launchtemplatespecification-id"></a>
The ID of the launch template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-eks-nodegroup-launchtemplatespecification-name"></a>
The name of the launch template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-eks-nodegroup-launchtemplatespecification-version"></a>
The version of the launch template to use\. If no version is specified, then the template's default version is used\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)