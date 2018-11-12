# OpenShift AWS Lab

## Configure AWS credentials
```shell
aws configure --profile <profile-name>
```

## Export RHSM credentials
```shell
export RHSM_USER="user"
export RHSM_PASSWORD="password"
export RHSM_POOL="pool-id"
```

## Pull down installation playbooks
```shell
git clone -b release-3.11 git@github.com:openshift/openshift-ansible.git /usr/share/ansible
```

## Fill out parameters in [defaults/main.yml](defaults/main.yml)

## Deploy Cluster
```shell
./deploy.yml -v -e '@vars/3.11-inventory.yml'
```