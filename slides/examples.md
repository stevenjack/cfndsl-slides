### Examples

#### AWS::SQS::Queue (DSL)

```ruby
Parameter "SQSRetentionPeriod" do
  String
  Descrption "The Retention period for the queues generated in this example"
end

queues = [
  'TestOne',
  'TestTwo'
]

queues.each do |name|

  Resource "#{name}Queue" do
    Type "AWS::SQS::Queue"
    Property "MessageRetentionPeriod", Ref("SQSRetentionPeriod")
  end

end
```


### Examples

#### AWS::AutoScaling::AutoScalingGroup (Output)

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
