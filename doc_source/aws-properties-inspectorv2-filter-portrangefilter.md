# AWS::InspectorV2::Filter PortRangeFilter<a name="aws-properties-inspectorv2-filter-portrangefilter"></a>

An object that describes the details of a port range filter\.

## Syntax<a name="aws-properties-inspectorv2-filter-portrangefilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-inspectorv2-filter-portrangefilter-syntax.json"></a>

```
{
  "[BeginInclusive](#cfn-inspectorv2-filter-portrangefilter-begininclusive)" : Integer,
  "[EndInclusive](#cfn-inspectorv2-filter-portrangefilter-endinclusive)" : Integer
}
```

### YAML<a name="aws-properties-inspectorv2-filter-portrangefilter-syntax.yaml"></a>

```
  [BeginInclusive](#cfn-inspectorv2-filter-portrangefilter-begininclusive): Integer
  [EndInclusive](#cfn-inspectorv2-filter-portrangefilter-endinclusive): Integer
```

## Properties<a name="aws-properties-inspectorv2-filter-portrangefilter-properties"></a>

`BeginInclusive`  <a name="cfn-inspectorv2-filter-portrangefilter-begininclusive"></a>
The port number the port range begins at\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndInclusive`  <a name="cfn-inspectorv2-filter-portrangefilter-endinclusive"></a>
The port number the port range ends at\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)