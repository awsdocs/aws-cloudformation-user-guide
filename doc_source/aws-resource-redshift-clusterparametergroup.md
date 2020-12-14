# AWS::Redshift::ClusterParameterGroup<a name="aws-resource-redshift-clusterparametergroup"></a>

Describes a parameter group\.

## Syntax<a name="aws-resource-redshift-clusterparametergroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-redshift-clusterparametergroup-syntax.json"></a>

```
{
  "Type" : "AWS::Redshift::ClusterParameterGroup",
  "Properties" : {
      "[Description](#cfn-redshift-clusterparametergroup-description)" : String,
      "[ParameterGroupFamily](#cfn-redshift-clusterparametergroup-parametergroupfamily)" : String,
      "[Parameters](#cfn-redshift-clusterparametergroup-parameters)" : [ Parameter, ... ],
      "[Tags](#cfn-redshift-clusterparametergroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-redshift-clusterparametergroup-syntax.yaml"></a>

```
Type: AWS::Redshift::ClusterParameterGroup
Properties: 
  [Description](#cfn-redshift-clusterparametergroup-description): String
  [ParameterGroupFamily](#cfn-redshift-clusterparametergroup-parametergroupfamily): String
  [Parameters](#cfn-redshift-clusterparametergroup-parameters): 
    - Parameter
  [Tags](#cfn-redshift-clusterparametergroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-redshift-clusterparametergroup-properties"></a>

`Description`  <a name="cfn-redshift-clusterparametergroup-description"></a>
The description of the parameter group\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ParameterGroupFamily`  <a name="cfn-redshift-clusterparametergroup-parametergroupfamily"></a>
The name of the cluster parameter group family that this cluster parameter group is compatible with\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Parameters`  <a name="cfn-redshift-clusterparametergroup-parameters"></a>
An array of parameters to be modified\. A maximum of 20 parameters can be modified in a single request\.  
For each parameter to be modified, you must supply at least the parameter name and parameter value; other name\-value pairs of the parameter are optional\.  
For the workload management \(WLM\) configuration, you must supply all the name\-value pairs in the wlm\_json\_configuration parameter\.  
*Required*: No  
*Type*: List of [Parameter](aws-property-redshift-clusterparametergroup-parameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-redshift-clusterparametergroup-tags"></a>
The list of tags for the cluster parameter group\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-redshift-clusterparametergroup-return-values"></a>

### Ref<a name="aws-resource-redshift-clusterparametergroup-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "myClusterParameterGroup" }` 

For the Amazon Redshift cluster parameter group `myClusterParameterGroup`, `Ref` returns the name of the cluster parameter group\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-redshift-clusterparametergroup--examples"></a>



### Single Parameter<a name="aws-resource-redshift-clusterparametergroup--examples--Single_Parameter"></a>

The following example describes a parameter group with one parameter that is specified:

#### JSON<a name="aws-resource-redshift-clusterparametergroup--examples--Single_Parameter--json"></a>

```
"myClusterParameterGroup" : {
  "Type" : "AWS::Redshift::ClusterParameterGroup",
  "Properties" : {
    "Description" : "My parameter group",
    "ParameterGroupFamily" : "redshift-1.0",
    "Parameters" : [ {
      "ParameterName" : "enable_user_activity_logging",
      "ParameterValue" : "true"
    }]
  }
}
```

#### YAML<a name="aws-resource-redshift-clusterparametergroup--examples--Single_Parameter--yaml"></a>

```
myClusterParameterGroup: 
  Type: "AWS::Redshift::ClusterParameterGroup"
  Properties: 
    Description: "My parameter group"
    ParameterGroupFamily: "redshift-1.0"
    Parameters: 
      - 
        ParameterName: "enable_user_activity_logging"
        ParameterValue: "true"
```

### Workload Management Configuration<a name="aws-resource-redshift-clusterparametergroup--examples--Workload_Management_Configuration"></a>

The following example modifies the workload management configuration using the `wlm_json_configuration` parameter\. The parameter value is a JSON object that must be passed as a string enclosed in quotation marks \("\)\.

#### JSON<a name="aws-resource-redshift-clusterparametergroup--examples--Workload_Management_Configuration--json"></a>

```
"RedshiftClusterParameterGroup": {
  "Type": "AWS::Redshift::ClusterParameterGroup",
  "Properties": {
    "Description": "Cluster parameter group",
    "ParameterGroupFamily": "redshift-1.0",
    "Parameters": [{
      "ParameterName": "wlm_json_configuration",
      "ParameterValue": "[{\"user_group\":[\"example_user_group1\"],\"query_group\":[\"example_query_group1\"],\"query_concurrency\":7},{\"query_concurrency\":5}]"
    }],
    "Tags": [
      {
        "Key": "foo",
        "Value": "bar"
      }
    ]
  }
}
```

#### YAML<a name="aws-resource-redshift-clusterparametergroup--examples--Workload_Management_Configuration--yaml"></a>

```
RedshiftClusterParameterGroup: 
  Type: "AWS::Redshift::ClusterParameterGroup"
  Properties: 
    Description: "Cluster parameter group"
    ParameterGroupFamily: "redshift-1.0"
    Parameters: 
      - 
        ParameterName: "wlm_json_configuration"
        ParameterValue: "[{\"user_group\":[\"example_user_group1\"],\"query_group\":[\"example_query_group1\"],\"query_concurrency\":7},{\"query_concurrency\":5}]"
    Tags:
      - Key: foo
        Value: bar
```