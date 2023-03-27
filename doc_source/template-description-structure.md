# Description<a name="template-description-structure"></a>

The `Description` section \(optional\) enables you to include comments about your template\.

The value for the description declaration must be a literal string that is between 0 and 1024 bytes in length\. You cannot use a parameter or function to specify the description\. The following snippet is an example of a description declaration:

**Important**  
During a stack update, you cannot update the `Description` section by itself\. You can update it only when you include changes that add, modify, or delete resources\.

## JSON<a name="template-description-structure-example.json"></a>

```
"Description" : "Here are some details about the template."
```

## YAML<a name="template-description-structure-example.yaml"></a>

```
Description: >
  Here are some
  details about
  the template.
```