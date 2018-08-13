# AWS::Redshift::ClusterParameterGroup<a name="aws-resource-redshift-clusterparametergroup"></a>

Creates an Amazon Redshift parameter group that you can associate with an Amazon Redshift cluster\. The parameters in the group apply to all the databases that you create in the cluster\.

**Topics**
+ [Syntax](#aws-resource-redshift-clusterparametergroup-syntax)
+ [Properties](#w3ab2c21c10d995b9)
+ [Return Values](#w3ab2c21c10d995c11)
+ [Examples](#w3ab2c21c10d995c13)

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
    "[Tags](#cfn-redshift-clusterparametergroup-tags)" : [ Resource Tag, ... ]
  }
}
```

### YAML<a name="aws-resource-redshift-clusterparametergroup-syntax.yaml"></a>

```
Type: "AWS::Redshift::ClusterParameterGroup"
Properties: 
  [Description](#cfn-redshift-clusterparametergroup-description): String
  [ParameterGroupFamily](#cfn-redshift-clusterparametergroup-parametergroupfamily): String
  [Parameters](#cfn-redshift-clusterparametergroup-parameters):
    - Parameter
  [Tags](#cfn-redshift-clusterparametergroup-tags):
    - Resource Tag
```

## Properties<a name="w3ab2c21c10d995b9"></a>

`Description`  <a name="cfn-redshift-clusterparametergroup-description"></a>
A description of the parameter group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ParameterGroupFamily`  <a name="cfn-redshift-clusterparametergroup-parametergroupfamily"></a>
The Amazon Redshift engine version that applies to this cluster parameter group\. The cluster engine version determines the set of parameters that you can specify in the `Parameters` property\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Parameters`  <a name="cfn-redshift-clusterparametergroup-parameters"></a>
A list of parameter names and values that are allowed by the Amazon Redshift engine version that you specified in the `ParameterGroupFamily` property\. For more information, see [Amazon Redshift Parameter Groups](http://docs.aws.amazon.com/redshift/latest/mgmt/working-with-parameter-groups.html) in the *Amazon Redshift Cluster Management Guide*\.  
*Required*: No  
*Type*: [Amazon Redshift Parameter Type](aws-property-redshift-clusterparametergroup-parameter.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Tags`  <a name="cfn-redshift-clusterparametergroup-tags"></a>
Specifies an arbitrary set of tags \(key–value pairs\) to associate with this parameter group\. Use tags to manage your resources\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10d995c11"></a>

### Ref<a name="w3ab2c21c10d995c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "myClusterParameterGroup" }
```

For the Amazon Redshift cluster parameter group `myClusterParameterGroup`, `Ref` returns the name of the cluster parameter group\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="w3ab2c21c10d995c13"></a>

### Single Parameter<a name="w3ab2c21c10d995c13b2"></a>

The following example describes a parameter group with one parameter that is specified:

#### JSON<a name="aws-resource-redshift-clusterparametergroup-example1.json"></a>

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

#### YAML<a name="aws-resource-redshift-clusterparametergroup-example1.yaml"></a>

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

### Workload Management Configuration<a name="w3ab2c21c10d995c13b4"></a>

The following example modifies the workload management configuration using the `wlm_json_configuration` parameter\. The parameter value is a JSON object that must be passed as a string enclosed in quotation marks \(`"`\)\.

#### JSON<a name="aws-resource-redshift-clusterparametergroup-example2.json"></a>

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

#### YAML<a name="aws-resource-redshift-clusterparametergroup-example2.yaml"></a>

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