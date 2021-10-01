# Packer AWS AMI 
Create an AWS AMI artifact 

### Added Provisioner
- ansible
- docker
- docker-compose
- python3-pip
- git

### Prerequisites on your machine
* Docker

### Usage
First set up a few variables for your environment in file "variables.tf".

### Usage
First set up a few variables for your environment in file "app.json.pkr.hcl".

| Name | Description | Type | Default |
|------|-------------|:----:|:-----:|
| ami\_name | Ami name. | string | `"DEVOP_TEST"` |
| region | The name AWS availability zone. | string | `"us-west-1"` |
| instance\_type | Type instace ec2. | string | `"t3a.small"` |
| default\_tags | Default tags name. | map | `"Key: value"` |

### Run container packer
```docker run -it -v $PWD:/app -w /app --entrypoint "" hashicorp/packer:light sh```

### Environments AWS
- export AWS_ACCESS_KEY_ID=
- export AWS_SECRET_ACCESS_KEY=
- export AWS_DEFAULT_REGION=

### Install Ansible container
```apk -U add ansible```

### Running project
```packer build app.json.pkr.hcl```

### Add variables
- variable "ami_name"
- variable "region"
- variable "type"
- variable "instance_typ"

### Debugging Packer Builds
- ```packer build -debug```
- ```PACKER_LOG=1 packer build```
- Debug mode informs the builders that they should output debugging information.
- Packer has detailed logs which can be enabled
