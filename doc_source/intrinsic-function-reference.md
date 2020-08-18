# Intrinsic function reference<a name="intrinsic-function-reference"></a>

AWS CloudFormation provides several built\-in functions that help you manage your stacks\. Use intrinsic functions in your templates to assign values to properties that are not available until runtime\.

**Note**  
You can use intrinsic functions only in specific parts of a template\. Currently, you can use intrinsic functions in resource properties, outputs, metadata attributes, and update policy attributes\. You can also use intrinsic functions to conditionally create stack resources\.

**Topics**
+ [`Fn::Base64`](intrinsic-function-reference-base64.md)
+ [`Fn::Cidr`](intrinsic-function-reference-cidr.md)
+ [Condition functions](intrinsic-function-reference-conditions.md)
+ [`Fn::FindInMap`](intrinsic-function-reference-findinmap.md)
+ [`Fn::GetAtt`](intrinsic-function-reference-getatt.md)
+ [`Fn::GetAZs`](intrinsic-function-reference-getavailabilityzones.md)
+ [`Fn::ImportValue`](intrinsic-function-reference-importvalue.md)
+ [`Fn::Join`](intrinsic-function-reference-join.md)
+ [`Fn::Select`](intrinsic-function-reference-select.md)
+ [`Fn::Split`](intrinsic-function-reference-split.md)
+ [`Fn::Sub`](intrinsic-function-reference-sub.md)
+ [`Fn::Transform`](intrinsic-function-reference-transform.md)
+ [`Ref`](intrinsic-function-reference-ref.md)