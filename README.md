# aws-meta-pipeline

## Usage

1. Fork this repo.

2. Deploy stack.

```
aws cloudformation deploy \
  --region "us-east-1" \
  --stack-name "aws-meta-pipeline" \
  --template "template.cfn.json" \
  --capabilities "CAPABILITY_IAM" \
  --parameter-overrides "FullRepositoryId=${yourGithubUsername}/aws-meta-pipeline"
```

3. Then open [Connections](https://console.aws.amazon.com/codesuite/settings/connections) and make the connection `AVAILABLE`.
