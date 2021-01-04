# Custom resource request types<a name="crpg-ref-requesttypes"></a>

The request type is sent in the `RequestType` field in the [vendor request object](crpg-ref-requests.md) sent by AWS CloudFormation when the template developer creates, updates, or deletes a stack that contains a custom resource\.

Each request type has a particular set of fields that are sent with the request, including an S3 URL for the response by the custom resource provider\. The provider must respond to the S3 bucket with either a `SUCCESS` or `FAILED` result within one hour\. After one hour, the request times out\. Each result also has a particular set of fields expected by AWS CloudFormation\.

This section provides information about the request and response fields, with examples, for each request type\.

## In this section<a name="w7739ab1c27c24c17c19b9"></a>
+ [Create](crpg-ref-requesttypes-create.md)
+ [Delete](crpg-ref-requesttypes-delete.md)
+ [Update](crpg-ref-requesttypes-update.md)