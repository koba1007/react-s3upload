### Upload to S3 using pre-signed urls and React Uploady

### Step1 Deploy Back-end
#### Move folder lambda/upload
<code>
cd react-s3upload/lambda/upload
</code>

#### Deploy Back-end
<code>
sam deploy --guided
</code>

#### Sample log
<code>
Configuring SAM deploy
======================

        Looking for config file [samconfig.toml] :  Not found

        Setting default arguments for 'sam deploy'
        =========================================
        Stack Name [sam-app]: 
        AWS Region [ap-northeast-1]: 
        #Shows you resources changes to be deployed and require a 'Y' to initiate deploy
        Confirm changes before deploy [y/N]: y
        #SAM needs permission to be able to create roles to connect to the resources in your template
        Allow SAM CLI IAM role creation [Y/n]: y
        #Preserves the state of previously provisioned resources when an operation fails
        Disable rollback [y/N]:  
        S3SignedUploadUrlFunction may not have authorization defined, Is this okay? [y/N]: y
        Save arguments to configuration file [Y/n]: y
        SAM configuration file [samconfig.toml]: 
        SAM configuration environment [default]: 
 </code>

### Step2 Modify Front-end
#### Modify Upload.js line30
<code>
    let gateway = 'https://XXXXXX.execute-api.ap-northeast-1.amazonaws.com/Prod/';
</code>

### Step3 Build
#### Install yarn
<code>
npm install -g yarn
</code>

#### Backage Install
<code>
yarn
</code>

#### Start View
<code>
yarn start
</code>
