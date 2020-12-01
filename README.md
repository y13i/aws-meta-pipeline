# aws-meta-pipeline

## Usage

1. Fork this repo.
2. Create a [CloudFormation service role](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-iam-servicerole.html).
3. Deploy stack.

```
aws cloudformation deploy \
  --region "us-east-1" \
  --stack-name "aws-meta-pipeline" \
  --template "template.cfn.json" \
  --capabilities "CAPABILITY_IAM" \
  --role-arn "${yourCfnRoleArn}" \
  --parameter-overrides "FullRepositoryId=${yourGithubUsername}/aws-meta-pipeline,CfnRole=${yourCfnRoleArn}"
```

4. Open [Connections](https://console.aws.amazon.com/codesuite/settings/connections) and make the connection `AVAILABLE`.
5. Modify `template.cfn.json`, commit and push it. Then the pipeline applies the change.
