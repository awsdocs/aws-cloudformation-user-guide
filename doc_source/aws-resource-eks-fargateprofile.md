# AWS::EKS::FargateProfile<a name="aws-resource-eks-fargateprofile"></a>

Creates an AWS Fargate profile for your Amazon EKS cluster\. You must have at least one Fargate profile in a cluster to be able to run pods on Fargate\.

The Fargate profile allows an administrator to declare which pods run on Fargate and specify which pods run on which Fargate profile\. This declaration is done through the profile’s selectors\. Each profile can have up to five selectors that contain a namespace and labels\. A namespace is required for every selector\. The label field consists of multiple optional key\-value pairs\. Pods that match the selectors are scheduled on Fargate\. If a to\-be\-scheduled pod matches any of the selectors in the Fargate profile, then that pod is run on Fargate\.

When you create a Fargate profile, you must specify a pod execution role to use with the pods that are scheduled with the profile\. This role is added to the cluster's Kubernetes [Role Based Access Control](https://kubernetes.io/docs/admin/authorization/rbac/) \(RBAC\) for authorization so that the `kubelet` that is running on the Fargate infrastructure can register with your Amazon EKS cluster so that it can appear in your cluster as a node\. The pod execution role also provides IAM permissions to the Fargate infrastructure to allow read access to Amazon ECR image repositories\. For more information, see [Pod Execution Role](https://docs.aws.amazon.com/eks/latest/userguide/pod-execution-role.html) in the *Amazon EKS User Guide*\.

Fargate profiles are immutable\. However, you can create a new updated profile to replace an existing profile and then delete the original after the updated profile has finished creating\.

If any Fargate profiles in a cluster are in the `DELETING` status, you must wait for that Fargate profile to finish deleting before you can create any other profiles in that cluster\.

For more information, see [AWS Fargate Profile](https://docs.aws.amazon.com/eks/latest/userguide/fargate-profile.html) in the *Amazon EKS User Guide*\.

## Syntax<a name="aws-resource-eks-fargateprofile-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-eks-fargateprofile-syntax.json"></a>

```
{
  "Type" : "AWS::EKS::FargateProfile",
  "Properties" : {
      "[ClusterName](#cfn-eks-fargateprofile-clustername)" : String,
      "[FargateProfileName](#cfn-eks-fargateprofile-fargateprofilename)" : String,
      "[PodExecutionRoleArn](#cfn-eks-fargateprofile-podexecutionrolearn)" : String,
      "[Selectors](#cfn-eks-fargateprofile-selectors)" : [ Selector, ... ],
      "[Subnets](#cfn-eks-fargateprofile-subnets)" : [ String, ... ],
      "[Tags](#cfn-eks-fargateprofile-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-eks-fargateprofile-syntax.yaml"></a>

```
Type: AWS::EKS::FargateProfile
Properties: 
  [ClusterName](#cfn-eks-fargateprofile-clustername): String
  [FargateProfileName](#cfn-eks-fargateprofile-fargateprofilename): String
  [PodExecutionRoleArn](#cfn-eks-fargateprofile-podexecutionrolearn): String
  [Selectors](#cfn-eks-fargateprofile-selectors): 
    - Selector
  [Subnets](#cfn-eks-fargateprofile-subnets): 
    - String
  [Tags](#cfn-eks-fargateprofile-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-eks-fargateprofile-properties"></a>

`ClusterName`  <a name="cfn-eks-fargateprofile-clustername"></a>
The name of the Amazon EKS cluster to apply the Fargate profile to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FargateProfileName`  <a name="cfn-eks-fargateprofile-fargateprofilename"></a>
The name of the Fargate profile\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PodExecutionRoleArn`  <a name="cfn-eks-fargateprofile-podexecutionrolearn"></a>
The Amazon Resource Name \(ARN\) of the pod execution role to use for pods that match the selectors in the Fargate profile\. The pod execution role allows Fargate infrastructure to register with your cluster as a node, and it provides read access to Amazon ECR image repositories\. For more information, see [Pod Execution Role](https://docs.aws.amazon.com/eks/latest/userguide/pod-execution-role.html) in the *Amazon EKS User Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Selectors`  <a name="cfn-eks-fargateprofile-selectors"></a>
The selectors to match for pods to use this Fargate profile\. Each selector must have an associated namespace\. Optionally, you can also specify labels for a namespace\. You may specify up to five selectors in a Fargate profile\.  
*Required*: Yes  
*Type*: List of [Selector](aws-properties-eks-fargateprofile-selector.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Subnets`  <a name="cfn-eks-fargateprofile-subnets"></a>
The IDs of subnets to launch your pods into\. At this time, pods running on Fargate are not assigned public IP addresses, so only private subnets \(with no direct route to an Internet Gateway\) are accepted for this parameter\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-eks-fargateprofile-tags"></a>
The metadata to apply to the Fargate profile to assist with categorization and organization\. Each tag consists of a key and an optional value, both of which you define\. Fargate profile tags do not propagate to any other resources associated with the Fargate profile, such as the pods that are scheduled with it\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-eks-fargateprofile-return-values"></a>

### Ref<a name="aws-resource-eks-fargateprofile-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "myFargateProfile" }` 

For the Fargate profile`myFargateProfile`, Ref returns the physical resource ID of the Fargate profile\. For example, `<cluster_name>/<Fargate_profile_name>`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-eks-fargateprofile-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-eks-fargateprofile-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the cluster, such as `arn:aws:eks:us-west-2:666666666666:fargateprofile/myCluster/myFargateProfile/1cb1a11a-1dc1-1d11-cf11-1111f11fa111`\.

## Examples<a name="aws-resource-eks-fargateprofile--examples"></a>

### Create a Fargate profile<a name="aws-resource-eks-fargateprofile--examples--Create_a_Fargate_profile"></a>

The following example creates a Fargate profile for pods deployed to a namespace with the name `my-namespace` that have a label with a key value pair assigned to them\.

#### JSON<a name="aws-resource-eks-fargateprofile--examples--Create_a_Fargate_profile--json"></a>

```
{
   "Resources" : {
      "EKSFargateProfile" : {
         "Type" : "AWS::EKS::FargateProfile",
         "Properties" : {
            "FargateProfileName" : "my-fargate-profile",
            "ClusterName" : "my-cluster",
            "PodExecutionRoleArn" : "arn:aws:iam::012345678910:role/AmazonEKSFargatePodExecutionRole",
            "Subnets" : [ "subnet-6782e71e", "subnet-e7e761ac" ],
            "Selectors" : [
               {
                  "Namespace" : "my-namespace",
                  "Labels" : [
                     {
                        "Key" : "my-key",
                        "Value" : "my-value"
                     }
                  ]
               }
            ]
         }
      }
   }
}
```

#### YAML<a name="aws-resource-eks-fargateprofile--examples--Create_a_Fargate_profile--yaml"></a>

```
Resources:
  EKSFargateProfile:
    Type: 'AWS::EKS::FargateProfile'
    Properties:
      FargateProfileName: my-fargate-profile
      ClusterName: my-cluster
      PodExecutionRoleArn: 'arn:aws:iam::012345678910:role/AmazonEKSFargatePodExecutionRole'
      Subnets:
        - subnet-6782e71e
        - subnet-e7e761ac
      Selectors:
        - Namespace: my-namespace
          Labels:
            - Key: my-key
              Value: my-value
```

## See also<a name="aws-resource-eks-fargateprofile--seealso"></a>
+  [AWS Fargate profile](https://docs.aws.amazon.com/eks/latest/userguide/fargate-profile.html) in the *Amazon EKS User Guide *\.
+  [CreateFargateProfile](https://docs.aws.amazon.com/eks/latest/APIReference/API_CreateFargateProfile.html) in the *Amazon EKS API Reference *\.