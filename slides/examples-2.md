### Examples

#### AWS::SQS::Queue (Output)

```ruby
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Parameters": {
        "SQSRetentionPeriod": {
            "Default": 300,
            "Description": "The Retention period for the queues generated in this example",
            "Type": "String"
        }
    },
    "Resources": {
        "TestOneQueue": {
            "Properties": {
                "MessageRetentionPeriod": {
                    "Ref": "SQSRetentionPeriod"
                }
            },
            "Type": "AWS::SQS::Queue"
        },
        "TestTwoQueue": {
            "Properties": {
                "MessageRetentionPeriod": {
                    "Ref": "SQSRetentionPeriod"
                }
            },
            "Type": "AWS::SQS::Queue"
        }
    }
}
end
```
