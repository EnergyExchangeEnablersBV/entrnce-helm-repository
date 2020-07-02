# aws-ecr-credential

This Chart seemlessly integrate Kubernetes with AWS ECR

Simply deploy this chart to your kubernetes cluster and you will be able to pull and run images from your AWS ECR (Elastic Container Registry) in your cluster.

Before you run this chart. Insert the secrets below in your kubernetes namespace.
```yaml
apiVersion: v1
kind: Secret
metadata:
  name: aws-ecr-credential
  namespace: < namespace >
type: Opaque
data:
  AWS_ACCESS_KEY_ID: < accessKeyId >
  AWS_SECRET_ACCESS_KEY: < secretAccessKey >
```
