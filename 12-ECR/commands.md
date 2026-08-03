# Login to ECR
aws ecr get-login-password --region <region> \
| docker login --username AWS --password-stdin <account-id>.dkr.ecr.<region>.amazonaws.com

# Create Repository
aws ecr create-repository --repository-name my-app

# Tag Image
docker tag my-app:latest <account-id>.dkr.ecr.<region>.amazonaws.com/my-app:latest

# Push Image
docker push <account-id>.dkr.ecr.<region>.amazonaws.com/my-app:latest