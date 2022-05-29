# AWS::DevOpsGuru::ResourceCollection<a name="aws-resource-devopsguru-resourcecollection"></a>

 A collection of AWS resources supported by DevOps Guru\. The one type of AWS resource collection supported is AWS CloudFormation stacks\. DevOps Guru can be configured to analyze only the AWS resources that are defined in the stacks\.

## Syntax<a name="aws-resource-devopsguru-resourcecollection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-devopsguru-resourcecollection-syntax.json"></a>

```
{
  "Type" : "AWS::DevOpsGuru::ResourceCollection",
  "Properties" : {
      "[ResourceCollectionFilter](#cfn-devopsguru-resourcecollection-resourcecollectionfilter)" : ResourceCollectionFilter
    }
}
```

### YAML<a name="aws-resource-devopsguru-resourcecollection-syntax.yaml"></a>

```
Type: AWS::DevOpsGuru::ResourceCollection
Properties: 
  [ResourceCollectionFilter](#cfn-devopsguru-resourcecollection-resourcecollectionfilter): 
    ResourceCollectionFilter
```

## Properties<a name="aws-resource-devopsguru-resourcecollection-properties"></a>

`ResourceCollectionFilter`  <a name="cfn-devopsguru-resourcecollection-resourcecollectionfilter"></a>
 Information about a filter used to specify which AWS resources are analyzed for anomalous behavior by DevOps Guru\.   
*Required*: Yes  
*Type*: [ResourceCollectionFilter](aws-properties-devopsguru-resourcecollection-resourcecollectionfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-devopsguru-resourcecollection-return-values"></a>

### Ref<a name="aws-resource-devopsguru-resourcecollection-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns Amazon Resource Name \(ARN\) of the `ResourceCollection`\. For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

### Fn::GetAtt<a name="aws-resource-devopsguru-resourcecollection-return-values-fn--getatt"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. For more information about using `Fn::GetAtt`, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\. 

#### <a name="aws-resource-devopsguru-resourcecollection-return-values-fn--getatt-fn--getatt"></a>

`ResourceCollectionType`  <a name="ResourceCollectionType-fn::getatt"></a>
The type of AWS resource collections to return\. The one valid value is `CLOUD_FORMATION` for AWS CloudFormation stacks\.

## Examples<a name="aws-resource-devopsguru-resourcecollection--examples"></a>

### Create a resource collection using two CloudFormation stacks<a name="aws-resource-devopsguru-resourcecollection--examples--Create_a_resource_collection_using_two_CloudFormation_stacks"></a>

#### JSON<a name="aws-resource-devopsguru-resourcecollection--examples--Create_a_resource_collection_using_two_CloudFormation_stacks--json"></a>

```
{
  "Resources": {
    "MyResourceCollection": {
      "Type": "AWS::DevOpsGuru::ResourceCollection",
      "Properties": {
        "ResourceCollectionFilter": {
          "CloudFormation": {
            "StackNames": [
              "StackA",
              "StackB"
            ]
          }
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-devopsguru-resourcecollection--examples--Create_a_resource_collection_using_two_CloudFormation_stacks--yaml"></a>

```
Resources:
  MyResourceCollection:
    Type: AWS::DevOpsGuru::ResourceCollection
    Properties:
      ResourceCollectionFilter:
        CloudFormation:
          StackNames:
          - StackA
          - StackB
```

### Create a resource collection with all CloudFormation stacks in your account<a name="aws-resource-devopsguru-resourcecollection--examples--Create_a_resource_collection_with_all_CloudFormation_stacks_in_your_account"></a>

#### JSON<a name="aws-resource-devopsguru-resourcecollection--examples--Create_a_resource_collection_with_all_CloudFormation_stacks_in_your_account--json"></a>

```
{
  "Resources": {
    "MyResourceCollection": {
      "Type": "AWS::DevOpsGuru::ResourceCollection",
      "Properties": {
        "ResourceCollectionFilter": {
          "CloudFormation": {
            "StackNames": [
              "*"
            ]
          }
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-devopsguru-resourcecollection--examples--Create_a_resource_collection_with_all_CloudFormation_stacks_in_your_account--yaml"></a>

```
Resources:
  MyResourceCollection:
    Type: AWS::DevOpsGuru::ResourceCollection
    Properties:
      ResourceCollectionFilter:
        CloudFormation:
          StackNames:
          - "*"
```