# Instructions

Following these steps will generate an AMI which has girder3 behind nginx.
It will have a local assetstore which is 100GB in size.
The admin user will have username: girder password: girder which needs to be changed.
Also there won't be any plugins installed.

### 1. Clone this repository
```
git clone git@github.com:dorukozturk/girder-ami.git
```

### 2. Enter your AWS credentials
```
cd girder-ami/packer
cp envs.example .envs
```

Modify the .envs file and enter your AWS credentials.
Source the .envs file.
```
source .envs
```

### 3. Install required Python packages
```
pip install python-gilt ansible==2.6.0
```

### 4. Install Packer
Follow [Packer's installation guide](https://www.packer.io/intro/getting-started/install.html) based on your operating system.

### 5. Run Packer to generate the AMI
```
packer build packer.json
```
