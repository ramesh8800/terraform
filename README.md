
#  **<span style="color:green">Mithun Technologies, Marathahalli ,Bengaluru.</span>**
### **<span style="color:green">Contacts: +91-9980923226, +91-8296242028<br> WebSite : <http://mithuntechnologies.co.in/></span>**
### **Email: devopstrainingblr@gmail.com, devopstrainingblr@outlook.com**



## Terraform Installation And Setup In AWS EC2 Redhat Instnace.
##### Prerequisite
+ AWS Acccount.
+ Create Redhat EC2 Instnace.
+ Create IAM Role With Required Polocies.
   + VPCFullAccess
   + EC2FullAcces
   + S3FullAccess  ..etc
+ Attach IAM Role to EC2 Instance.

### Install Terraform

``` sh
$ sudo yum install wget unzip -y
$ wget https://releases.hashicorp.com/terraform/0.12.26/terraform_0.12.26_linux_amd64.zip
$ sudo unzip terraform_0.12.26_linux_amd64.zip -d /usr/local/bin/
# Export terraform binary path temporally
$ export PATH=$PATH:/usr/local/bin
# Add path permanently for current user.By Exporting path in .bashrc file at end of file.
$ vi .bashrc
   export PATH="$PATH:/usr/local/bin"
# Source .bashrc to reflect for current session
$ source ~/.bashrc   
```
#### Clone terraform scripts
``` sh
$ git clone https://github.com/MithunTechnologiesDevOps/Terraform_Scripts.git
$ cd Terraform_Scripts
```
#### <span style="color:orange">Update Your Key Name in variables.tf file before executing terraform script.</span>
## Infrastructure As A Code
#### Create Infrastructure(VPC,Subnets,Route Tables,EC2 Instnaces ..etc) As A Code Using Terraform Scripts
``` sh
# Initialise to install plugins
$ terraform init VPC/
# Validate teffaform scripts
$ terraform validate VPC/
# Plan terraform scripts which will list resources which is going  be created.
$ terraform plan VPC/
# Apply to create resources
$ terraform apply --auto-approve VPC/
```

##  Destroy Infrastructure  
```sh
$ terraform destroy --auto-approve VPC/
```



root@ip-172-31-7-10:~# history
    1  cd
    2  ls
    3  cd
    4  sudo apt install wget unzip -y
    5  wget https://releases.hashicorp.com/terraform/0.12.26/terraform_0.12.26_linux_amd64.zip
    6  sudo unzip terraform_0.12.26_linux_amd64.zip -d /usr/local/bin/
    7  export PATH=$PATH:/usr/local/bin
    8  vi .bashrc
    9  source ~/.bashrc
   10  terraform --version
   11  git --version
   12  git clone https://github.com/MithunTechnologiesDevOps/Terraform_Scripts.git
   13  ls
   14  cd Terraform_Scripts
   15  ls
   16  cd VPC/
   17  ls
   18  vi variables.tf
   19  ls
   20  cd
   21  ls
   22  cd Terraform_Scripts
   23  ls
   24  cd vpc
   25  cd VPC/
   26  ls
   27  vi vpc.tf
   28  cd
   29  ls
   30  cd Terraform_Scripts
   31  cd
   32  cd Terraform_Scripts
   33  ls
   34  cd VPC/
   35  ls
   36  cd vpc.tf
   37  vi vpc.tf
   38  vi variables.tf
   39  cd
   40  ls
   41  cd Terraform_Scripts
   42  ls
   43  cd VPC/
   44  ls
   45  vi variables.tf
   46  vi security-groups.tf
   47  vi instances.tf
   48  terraform init VPC/
   49  ls
   50  cd ..
   51  ls
   52  terraform init VPC/
   53  terraform validate VPC/
   54  cd VPC/
   55  ls
   56  vi vpc.tf
   57  cat variables.tf
   58  vi instances.tf
   59  cd ..
   60  terraform validate VPC/
   61  terraform plan VPC/
   62  cd
   63  cd Terraform_Scripts/
   64  ls
   65  cd VPC/
   66  ls
   67  cd ..
   68  terraform apply --auto-approve VPC/
   69  cd VPC/
   70  ls
   71  vi vpc.tf
   72  vi instances.tf
   73  cd ..
   74  terraform destroy --auto-approve VPC/
   75  cd
   76  cd Terraform_Scripts/
   77  ls
   78  vi terraform.tfstate
   79  cd
   80  ls
   81  terraform --version
   82  history
   83  cd
   84  ls
   85  cd Terraform_Scripts/
   86  ls
   87  cd VPC/
   88  ls
   89  cd
   90  ls
   91  cd Terraform_Scripts
   92  ls
   93  cd VPC/
   94  ls
   95  cat vpc.tf
   96  cat variables.tf
   97  cd
   98  ls
   99  cd Terraform_Scripts/
  100  ls
  101  cd EKS/
  102  ls
  103  vi workstation-external-ip.tf
  104  cat vpc.tf
  105  ls
  106  vi variables.tf
  107  cat providers.tf
  108  cat outputs.tf
  109  cd
  110  cd Terraform_Scripts/EKS/
  111  ls
  112  vi clusterautoscaler.yml
  113  vi eks-cluster.tf
  114  cd
  115  cd Terraform_Scripts/EKS/
  116  ls
  117  vi eks-cluster.tf
  118  cd
  119  cd Terraform_Scripts/EKS/
  120  ls
  121  vi eks-cluster.tf
  122  vi eks-worker-nodes.tf
  123  ls
  124  cd
  125  cd Terraform_Scripts/EKS/
  126  ls
  127  cd
  128  cd Terraform_Scripts/EKS/
  129  ls
  130  vi eks-worker-nodes.tf
  131  vi providers.tf
  132  cd
  133  cd Terraform_Scripts/EKS/
  134  ls
  135  vi providers.tf
  136  vi test.yml
  137  vi variables.tf
  138  vi vpc.tf
  139  vi workstation-external-ip.tf
  140  vi clusterautoscaler.yml
  141  vi eks-cluster.tf
  142  vi eks-worker-nodes.tf
  143  vi outputs.tf
  144  cd ..
  145  ls
  146  terraform init EKS/
  147  terraform validate EKS/
  148  terraform plan EKS/
  149  terraform apply EKS/
  150  cd
  151  cd Terraform_Scripts/
  152  ls
  153  cd EKS/
  154  ls
  155  vi eks-cluster.tf
  156  cd
  157  cd Terraform_Scripts/EKS/
  158  ls
  159  cd
  160  cd Terraform_Scripts/EKS/
  161  ls
  162  cd
  163  curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
  164  unzip awscliv2.zip
  165  sudo ./aws/install
  166  aws --version
  167  aws configure
  168  aws s3 ls
  169  aws --version
  170  cd Terraform_Scripts/
  171  ls
  172  terraform plan EKS/
  173  terraform apply EKS/
  174  vi .kube
  175  vi configmap
  176  ls
  177  ls -ll
  178  ls -la
  179  terraform destroy EKS/
  180  cd
  181  cd Terraform_Scripts/
  182  ls
  183  cd
  184  git --version
  185  git clone https://github.com/ramesh8800/terraform.git
  186  ls
  187  pwd
  188  cp /root/Terraform_Scripts/ /root/terrform
  189  cp -r /root/Terraform_Scripts/ /root/terrform
  190  ls
  191  rm -r terrform
  192  ls
  193  cd aws
  194  ls
  195  cd ..
  196  ls
  197  cp -r /root/Terraform_Scripts/ /root/terraform/
  198  ls
  199  cd terraform
  200  ls
  201  git add .
  202  cd Terraform_Scripts/
  203  ls
  204  git add .
  205  git status
  206  git commit -m"terraform"
  207  git config --global --edit
  208  git commit -m "first commit"
  209  git remote add origin https://github.com/ramesh8800/terraform.git
  210  git push https://github.com/ramesh8800/terraform.git
  211  cd
  212  

