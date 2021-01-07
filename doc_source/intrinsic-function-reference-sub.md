# `Fn::Sub`<a name="intrinsic-function-reference-sub"></a>

The intrinsic function `Fn::Sub` substitutes variables in an input string with values that you specify\. In your templates, you can use this function to construct commands or outputs that include values that aren't available until you create or update a stack\.

## Declaration<a name="w7739ab1c33c28c59b5"></a>

The following sections show the function's syntax\.

### JSON<a name="intrinsic-function-reference-sub-syntax.json"></a>

```
{ "Fn::Sub" : [ String, { Var1Name: Var1Value, Var2Name: Var2Value } ] }
```

If you're substituting only template parameters, resource logical IDs, or resource attributes in the `String` parameter, don't specify a variable map\.

```
{ "Fn::Sub" : String }
```

### YAML<a name="intrinsic-function-reference-sub-syntax.yaml"></a>

Syntax for the full function name:

```
Fn::Sub:
  - String
  - Var1Name: Var1Value
    Var2Name: Var2Value
```

Syntax for the short form:

```
!Sub
  - String
  - Var1Name: Var1Value
    Var2Name: Var2Value
```

If you're substituting only template parameters, resource logical IDs, or resource attributes in the `String` parameter, don't specify a variable map\.

Syntax for the full function name:

```
Fn::Sub: String
```

Syntax for the short form:

```
!Sub String
```

## Parameters<a name="w7739ab1c33c28c59b7"></a>

`String`  
A string with variables that AWS CloudFormation substitutes with their associated values at runtime\. Write variables as `${MyVarName}`\. Variables can be template parameter names, resource logical IDs, resource attributes, or a variable in a key\-value map\. If you specify only template parameter names, resource logical IDs, and resource attributes, don't specify a key\-value map\.  
If you specify template parameter names or resource logical IDs, such as `${InstanceTypeParameter}`, AWS CloudFormation returns the same values as if you used the `Ref` intrinsic function\. If you specify resource attributes, such as `${MyInstance.PublicIp}`, AWS CloudFormation returns the same values as if you used the `Fn::GetAtt` intrinsic function\.  
To write a dollar sign and curly braces \(`${}`\) literally, add an exclamation point \(`!`\) after the open curly brace, such as `${!Literal}`\. AWS CloudFormation resolves this text as `${Literal}`\.

`VarName`  
The name of a variable that you included in the `String` parameter\.

`VarValue`  
The value that AWS CloudFormation substitutes for the associated variable name at runtime\.

## Return value<a name="w7739ab1c33c28c59b9"></a>

AWS CloudFormation returns the original string, substituting the values for all of the variables\.

## Examples<a name="w7739ab1c33c28c59c11"></a>

The following examples demonstrate how to use the `Fn::Sub` function\.

### Fn::Sub with a mapping<a name="w7739ab1c33c28c59c11b4"></a>

The following example uses a mapping to substitute the `${Domain}` variable with the resulting value from the `Ref` function\.

#### JSON<a name="intrinsic-function-reference-sub-example-2.json"></a>

```
{ "Fn::Sub": [ "www.${Domain}", { "Domain": {"Ref" : "RootDomainName" }} ]}
```

#### YAML<a name="intrinsic-function-reference-sub-example-2.yaml"></a>

```
Name: !Sub
  - www.${Domain}
  - { Domain: !Ref RootDomainName }
```

 

### Fn::Sub without a mapping<a name="w7739ab1c33c28c59c11b6"></a>

The following example uses Fn::Sub with the `AWS::Region` and `AWS::AccountId` pseudo parameters and the `vpc` resource logical ID to create an Amazon Resource Name \(ARN\) for a VPC\.

#### JSON<a name="intrinsic-function-reference-sub-example-3.json"></a>

```
{ "Fn::Sub": "arn:aws:ec2:${AWS::Region}:${AWS::AccountId}:vpc/${vpc}" }
```

#### YAML<a name="intrinsic-function-reference-sub-example-3.yaml"></a>

```
!Sub 'arn:aws:ec2:${AWS::Region}:${AWS::AccountId}:vpc/${vpc}'
```

 

### UserData commands<a name="w7739ab1c33c28c59c11b8"></a>

The following example uses `Fn::Sub` to substitute the `AWS::StackName` and `AWS::Region` pseudo parameters for the actual stack name and region at runtime\.

#### JSON<a name="intrinsic-function-reference-sub-example.json"></a>

For readability, the JSON example uses the `Fn::Join` function to separate each command, instead of specifying the entire user data script in a single string value\.

```
"UserData": { "Fn::Base64": { "Fn::Join": ["\n", [
  "#!/bin/bash -xe",
  "yum update -y aws-cfn-bootstrap",
  { "Fn::Sub": "/opt/aws/bin/cfn-init -v --stack ${AWS::StackName} --resource LaunchConfig --configsets wordpress_install --region ${AWS::Region}" },
  { "Fn::Sub": "/opt/aws/bin/cfn-signal -e $? --stack ${AWS::StackName} --resource WebServerGroup --region ${AWS::Region}" }]]
}}
```

#### YAML<a name="intrinsic-function-reference-sub-example.yaml"></a>

The YAML example uses a literal block to specify the user data script\.

```
UserData:
  Fn::Base64:
    !Sub |
      #!/bin/bash -xe
      yum update -y aws-cfn-bootstrap
      /opt/aws/bin/cfn-init -v --stack ${AWS::StackName} --resource LaunchConfig --configsets wordpress_install --region ${AWS::Region}
      /opt/aws/bin/cfn-signal -e $? --stack ${AWS::StackName} --resource WebServerGroup --region ${AWS::Region}
```

## Supported functions<a name="w7739ab1c33c28c59c13"></a>

For the `String` parameter, you cannot use any functions\. You must specify a string value\.

For the `VarName` and `VarValue` parameters, you can use the following functions:
+ `Fn::Base64`
+ `Fn::FindInMap`
+ `Fn::GetAtt`
+ `Fn::GetAZs`
+ `Fn::If`
+ `Fn::ImportValue`
+ `Fn::Join`
+ `Fn::Select`
+ `Ref`