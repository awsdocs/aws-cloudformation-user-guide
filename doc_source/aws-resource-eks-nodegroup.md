# AWS::EKS::Nodegroup<a name="aws-resource-eks-nodegroup"></a>

Creates a managed node group for an Amazon EKS cluster\. You can only create a node group for your cluster that is equal to the current Kubernetes version for the cluster\. All node groups are created with the latest AMI release version for the respective minor Kubernetes version of the cluster, unless you deploy a custom AMI using a launch template\. For more information about using launch templates, see [Launch template support](https://docs.aws.amazon.com/eks/latest/userguide/launch-templates.html)\.

An Amazon EKS managed node group is an Amazon EC2 Auto Scaling group and associated Amazon EC2 instances that are managed by AWS for an Amazon EKS cluster\. Each node group uses a version of the Amazon EKS optimized Amazon Linux 2 AMI\. For more information, see [Managed Node Groups](https://docs.aws.amazon.com/eks/latest/userguide/managed-node-groups.html) in the *Amazon EKS User Guide*\. 

## Syntax<a name="aws-resource-eks-nodegroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-eks-nodegroup-syntax.json"></a>

```
{
  "Type" : "AWS::EKS::Nodegroup",
  "Properties" : {
      "[AmiType](#cfn-eks-nodegroup-amitype)" : String,
      "[CapacityType](#cfn-eks-nodegroup-capacitytype)" : String,
      "[ClusterName](#cfn-eks-nodegroup-clustername)" : String,
      "[DiskSize](#cfn-eks-nodegroup-disksize)" : Double,
      "[ForceUpdateEnabled](#cfn-eks-nodegroup-forceupdateenabled)" : Boolean,
      "[InstanceTypes](#cfn-eks-nodegroup-instancetypes)" : [ String, ... ],
      "[Labels](#cfn-eks-nodegroup-labels)" : Json,
      "[LaunchTemplate](#cfn-eks-nodegroup-launchtemplate)" : LaunchTemplateSpecification,
      "[NodegroupName](#cfn-eks-nodegroup-nodegroupname)" : String,
      "[NodeRole](#cfn-eks-nodegroup-noderole)" : String,
      "[ReleaseVersion](#cfn-eks-nodegroup-releaseversion)" : String,
      "[RemoteAccess](#cfn-eks-nodegroup-remoteaccess)" : RemoteAccess,
      "[ScalingConfig](#cfn-eks-nodegroup-scalingconfig)" : ScalingConfig,
      "[Subnets](#cfn-eks-nodegroup-subnets)" : [ String, ... ],
      "[Tags](#cfn-eks-nodegroup-tags)" : Json,
      "[Version](#cfn-eks-nodegroup-version)" : String
    }
}
```

### YAML<a name="aws-resource-eks-nodegroup-syntax.yaml"></a>

```
Type: AWS::EKS::Nodegroup
Properties: 
  [AmiType](#cfn-eks-nodegroup-amitype): String
  [CapacityType](#cfn-eks-nodegroup-capacitytype): String
  [ClusterName](#cfn-eks-nodegroup-clustername): String
  [DiskSize](#cfn-eks-nodegroup-disksize): Double
  [ForceUpdateEnabled](#cfn-eks-nodegroup-forceupdateenabled): Boolean
  [InstanceTypes](#cfn-eks-nodegroup-instancetypes): 
    - String
  [Labels](#cfn-eks-nodegroup-labels): Json
  [LaunchTemplate](#cfn-eks-nodegroup-launchtemplate): 
    LaunchTemplateSpecification
  [NodegroupName](#cfn-eks-nodegroup-nodegroupname): String
  [NodeRole](#cfn-eks-nodegroup-noderole): String
  [ReleaseVersion](#cfn-eks-nodegroup-releaseversion): String
  [RemoteAccess](#cfn-eks-nodegroup-remoteaccess): 
    RemoteAccess
  [ScalingConfig](#cfn-eks-nodegroup-scalingconfig): 
    ScalingConfig
  [Subnets](#cfn-eks-nodegroup-subnets): 
    - String
  [Tags](#cfn-eks-nodegroup-tags): Json
  [Version](#cfn-eks-nodegroup-version): String
```

## Properties<a name="aws-resource-eks-nodegroup-properties"></a>

`AmiType`  <a name="cfn-eks-nodegroup-amitype"></a>
The AMI type for your node group\. GPU instance types should use the `AL2_x86_64_GPU` AMI type\. Non\-GPU instances should use the `AL2_x86_64` AMI type\. Arm instances should use the `AL2_ARM_64` AMI type\. All types use the Amazon EKS optimized Amazon Linux 2 AMI\. If you specify `launchTemplate`, and your launch template uses a custom AMI, then don't specify `amiType`, or the node group deployment will fail\. For more information about using launch templates with Amazon EKS, see [Launch template support](https://docs.aws.amazon.com/eks/latest/userguide/launch-templates.html) in the Amazon EKS User Guide\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AL2_ARM_64 | AL2_x86_64 | AL2_x86_64_GPU`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CapacityType`  <a name="cfn-eks-nodegroup-capacitytype"></a>
The capacity type of your managed node group\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ON_DEMAND | SPOT`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClusterName`  <a name="cfn-eks-nodegroup-clustername"></a>
The name of the cluster to create the node group in\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DiskSize`  <a name="cfn-eks-nodegroup-disksize"></a>
The root device disk size \(in GiB\) for your node group instances\. The default disk size is 20 GiB\. If you specify `launchTemplate`, then don't specify `diskSize`, or the node group deployment will fail\. For more information about using launch templates with Amazon EKS, see [Launch template support](https://docs.aws.amazon.com/eks/latest/userguide/launch-templates.html) in the Amazon EKS User Guide\.  
*Required*: No  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ForceUpdateEnabled`  <a name="cfn-eks-nodegroup-forceupdateenabled"></a>
Force the update if the existing node group's pods are unable to be drained due to a pod disruption budget issue\. If an update fails because pods could not be drained, you can force the update after it fails to terminate the old node whether or not any pods are running on the node\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceTypes`  <a name="cfn-eks-nodegroup-instancetypes"></a>
Specify the instance types for a node group\. If you specify a GPU instance type, be sure to specify `AL2_x86_64_GPU` with the `amiType` parameter\. If you specify `launchTemplate`, then you can specify zero or one instance type in your launch template *or* you can specify 0\-20 instance types for `instanceTypes`\. If however, you specify an instance type in your launch template *and* specify any `instanceTypes`, the node group deployment will fail\. If you don't specify an instance type in a launch template or for `instanceTypes`, then `t3.medium` is used, by default\. If you specify `Spot` for `capacityType`, then we recommend specifying multiple values for `instanceTypes`\. For more information, see [Managed node group capacity types](https://docs.aws.amazon.com/eks/latest/userguide/managed-node-groups.html#managed-node-group-capacity-types) and [Launch template support](https://docs.aws.amazon.com/eks/latest/userguide/launch-templates.html) in the *Amazon EKS User Guide*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Labels`  <a name="cfn-eks-nodegroup-labels"></a>
The Kubernetes labels to be applied to the nodes in the node group when they are created\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchTemplate`  <a name="cfn-eks-nodegroup-launchtemplate"></a>
An object representing a node group's launch template specification\. If specified, then do not specify `instanceTypes`, `diskSize`, or `remoteAccess` and make sure that the launch template meets the requirements in `launchTemplateSpecification`\.  
*Required*: No  
*Type*: [LaunchTemplateSpecification](aws-properties-eks-nodegroup-launchtemplatespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NodegroupName`  <a name="cfn-eks-nodegroup-nodegroupname"></a>
The unique name to give your node group\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NodeRole`  <a name="cfn-eks-nodegroup-noderole"></a>
The Amazon Resource Name \(ARN\) of the IAM role to associate with your node group\. The Amazon EKS worker node `kubelet` daemon makes calls to AWS APIs on your behalf\. Nodes receive permissions for these API calls through an IAM instance profile and associated policies\. Before you can launch nodes and register them into a cluster, you must create an IAM role for those nodes to use when they are launched\. For more information, see [Amazon EKS node IAM role](https://docs.aws.amazon.com/eks/latest/userguide/worker_node_IAM_role.html) in the * *Amazon EKS User Guide* *\. If you specify `launchTemplate`, then don't specify [ `IamInstanceProfile` ](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_IamInstanceProfile.html) in your launch template, or the node group deployment will fail\. For more information about using launch templates with Amazon EKS, see [Launch template support](https://docs.aws.amazon.com/eks/latest/userguide/launch-templates.html) in the Amazon EKS User Guide\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ReleaseVersion`  <a name="cfn-eks-nodegroup-releaseversion"></a>
The AMI version of the Amazon EKS\-optimized AMI to use with your node group \(for example, `1.14.7-YYYYMMDD`\)\. By default, the latest available AMI version for the node group's current Kubernetes version is used\. For more information, see [Amazon EKS\-Optimized Linux AMI Versions](https://docs.aws.amazon.com/eks/latest/userguide/eks-linux-ami-versions.html) in the *Amazon EKS User Guide*\.  
Changing this value triggers an update of the node group if one is available\. However, only the latest available AMI release version is valid as an input\. You cannot roll back to a previous AMI release version\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RemoteAccess`  <a name="cfn-eks-nodegroup-remoteaccess"></a>
The remote access \(SSH\) configuration to use with your node group\. If you specify `launchTemplate`, then don't specify `remoteAccess`, or the node group deployment will fail\. For more information about using launch templates with Amazon EKS, see [Launch template support](https://docs.aws.amazon.com/eks/latest/userguide/launch-templates.html) in the Amazon EKS User Guide\.  
*Required*: No  
*Type*: [RemoteAccess](aws-properties-eks-nodegroup-remoteaccess.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ScalingConfig`  <a name="cfn-eks-nodegroup-scalingconfig"></a>
The scaling configuration details for the Auto Scaling group that is created for your node group\.  
*Required*: No  
*Type*: [ScalingConfig](aws-properties-eks-nodegroup-scalingconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subnets`  <a name="cfn-eks-nodegroup-subnets"></a>
The subnets to use for the Auto Scaling group that is created for your node group\. These subnets must have the tag key `kubernetes.io/cluster/CLUSTER_NAME` with a value of `shared`, where `CLUSTER_NAME` is replaced with the name of your cluster\. If you specify `launchTemplate`, then don't specify [ `SubnetId` ](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateNetworkInterface.html) in your launch template, or the node group deployment will fail\. For more information about using launch templates with Amazon EKS, see [Launch template support](https://docs.aws.amazon.com/eks/latest/userguide/launch-templates.html) in the Amazon EKS User Guide\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-eks-nodegroup-tags"></a>
The metadata to apply to the node group to assist with categorization and organization\. Each tag consists of a key and an optional value, both of which you define\. Node group tags do not propagate to any other resources associated with the node group, such as the Amazon EC2 instances or subnets\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-eks-nodegroup-version"></a>
The Kubernetes version to use for your managed nodes\. By default, the Kubernetes version of the cluster is used, and this is the only accepted specified value\. If you specify `launchTemplate`, and your launch template uses a custom AMI, then don't specify `version`, or the node group deployment will fail\. For more information about using launch templates with Amazon EKS, see [Launch template support](https://docs.aws.amazon.com/eks/latest/userguide/launch-templates.html) in the Amazon EKS User Guide\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-eks-nodegroup-return-values"></a>

### Ref<a name="aws-resource-eks-nodegroup-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "myNodegroup" }` 

For the Amazon EKS node group `myNodegroup`, Ref returns the physical resource ID of the node group\. For example, `<cluster_name>/<nodegroup_name>`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-eks-nodegroup-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-eks-nodegroup-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) associated with the managed node group\.

`ClusterName`  <a name="ClusterName-fn::getatt"></a>
The name of the cluster that the managed node group resides in\.

`NodegroupName`  <a name="NodegroupName-fn::getatt"></a>
The name associated with an Amazon EKS managed node group\.

## Examples<a name="aws-resource-eks-nodegroup--examples"></a>

### Create a managed node group<a name="aws-resource-eks-nodegroup--examples--Create_a_managed_node_group"></a>

The following example creates an Amazon EKS managed node group called `standard` in the `prod` cluster\.

#### JSON<a name="aws-resource-eks-nodegroup--examples--Create_a_managed_node_group--json"></a>

```
{
    "Resources": {
        "EKSNodegroup": {
            "Type": "AWS::EKS::Nodegroup",
            "Properties": {
                "ClusterName": "prod",
                "NodeRole": "arn:aws:iam::012345678910:role/eksInstanceRole",
                "ScalingConfig": {
                    "MinSize": 3,
                    "DesiredSize": 5,
                    "MaxSize": 7
                },
                "Labels": {
                    "Key1": "Value1",
                    "Key2": "Value2"
                },
                "Subnets": [
                    "subnet-6782e71e",
                    "subnet-e7e761ac"
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-eks-nodegroup--examples--Create_a_managed_node_group--yaml"></a>

```
Resources:
  EKSNodegroup:
    Type: 'AWS::EKS::Nodegroup'
    Properties:
      ClusterName: prod
      NodeRole: 'arn:aws:iam::012345678910:role/eksInstanceRole'
      ScalingConfig:
        MinSize: 3
        DesiredSize: 5
        MaxSize: 7
      Labels:
        Key1: Value1
        Key2: Value2
      Subnets:
        - subnet-6782e71e
        - subnet-e7e761ac
```

## See also<a name="aws-resource-eks-nodegroup--seealso"></a>
+  [Managed Node Groups](https://docs.aws.amazon.com/eks/latest/userguide/managed-node-groups.html) in the *Amazon EKS User Guide *\.
+  [CreateNodegroup](https://docs.aws.amazon.com/eks/latest/APIReference/API_CreateNodegroup.html) in the *Amazon EKS API Reference *\.