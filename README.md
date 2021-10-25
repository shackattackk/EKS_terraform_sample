# EKS Notes

## Run amazon docker image locally

```
# Run amazon CLI
docker run --rm -it -v $(pwd):/work -w /work --entrypoint /bin/sh amazon/aws-cli:latest

# install some tools
yum install -y jq gzip tar git unzip wget
```

## Configure aws-cli

```
aws configure
```

## Download Terraform

```
curl -o /tmp/terraform.zip -LO https://releases.hashicorp.com/terraform/0.13.0/terraform_0.13.0_linux_amd64.zip
unzip /tmp/terraform.zip
chmod +x terraform && mv terraform /usr/local/bin
```

## Deploy EKS

```
terraform init
terraform plan
terraform apply
```
