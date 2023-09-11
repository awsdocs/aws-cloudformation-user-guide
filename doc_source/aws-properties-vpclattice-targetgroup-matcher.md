# AWS::VpcLattice::TargetGroup Matcher<a name="aws-properties-vpclattice-targetgroup-matcher"></a>

Describes the codes to use when checking for a successful response from a target for health checks\.

## Syntax<a name="aws-properties-vpclattice-targetgroup-matcher-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-vpclattice-targetgroup-matcher-syntax.json"></a>

```
{
  "[HttpCode](#cfn-vpclattice-targetgroup-matcher-httpcode)" : String
}
```

### YAML<a name="aws-properties-vpclattice-targetgroup-matcher-syntax.yaml"></a>

```
  [HttpCode](#cfn-vpclattice-targetgroup-matcher-httpcode): String
```

## Properties<a name="aws-properties-vpclattice-targetgroup-matcher-properties"></a>

`HttpCode`  <a name="cfn-vpclattice-targetgroup-matcher-httpcode"></a>
The HTTP code to use when checking for a successful response from a target\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)