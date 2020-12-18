# `Ref`<a name="intrinsic-function-reference-ref"></a>

The intrinsic function `Ref` returns the value of the specified *parameter* or *resource*\.
+ When you specify a parameter's logical name, it returns the value of the parameter\.
+ When you specify a resource's logical name, it returns a value that you can typically use to refer to that resource, such as a [physical ID](resources-section-structure.md)\.

When you are declaring a resource in a template and you need to specify another template resource by name, you can use the `Ref` to refer to that other resource\. In general, `Ref` returns the name of the resource\. For example, a reference to an [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) returns the name of that Auto Scaling group resource\.

For some resources, an identifier is returned that has another significant meaning in the context of the resource\. An [AWS::EC2::EIP](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-eip.html) resource, for instance, returns the IP address, and an [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html) returns the instance ID\. 

**Tip**  
You can also use `Ref` to add values to Output messages\.

For more information about `Ref` return values for a particular resource or property, refer to the documentation for that resource or property in the [Resource and property reference](aws-template-resource-type-ref.md)\.

## Declaration<a name="ref-declaration"></a>

### JSON<a name="intrinsic-function-reference-ref-syntax.json"></a>

```
{ "Ref" : "logicalName" }
```

### YAML<a name="intrinsic-function-reference-ref-syntax.yaml"></a>

Syntax for the full function name:

```
Ref: logicalName
```

Syntax for the short form:

```
!Ref logicalName
```

## Parameters<a name="ref-parameters"></a>

logicalName  
The logical name of the resource or parameter you want to dereference\.

## Return value<a name="ref-return-value"></a>

The physical ID of the resource or the value of the parameter\.

## Example<a name="ref-example"></a>

The following resource declaration for an Elastic IP address needs the instance ID of an EC2 instance and uses the `Ref` function to specify the instance ID of the MyEC2Instance resource:

### JSON<a name="intrinsic-function-reference-ref-example.json"></a>

```
"MyEIP" : {
   "Type" : "AWS::EC2::EIP",
   "Properties" : {
      "InstanceId" : { "Ref" : "MyEC2Instance" }
   }
}
```

### YAML<a name="intrinsic-function-reference-ref-example.yaml"></a>

```
MyEIP:
  Type: "AWS::EC2::EIP"
  Properties:
    InstanceId: !Ref MyEC2Instance
```

## Supported functions<a name="ref-supported-functions"></a>

You cannot use any functions in the `Ref` function\. You must specify a string that is a resource logical ID\.