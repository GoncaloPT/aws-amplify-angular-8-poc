# Aws amplify POC

This POC is to demonstrate the use of aws amplify with:
1. graphql
1. dynamoDB 
1. AppSync
1. Angular


## Steps executed 

Based in https://aws-amplify.github.io/docs/cli-toolchain/quickstart


### Configure amplify to a aws account

This just configures amplify - it doesn't create any resource
```
amplify configure
```

### Create angular app
1. make sure ng-cli is updated, to update use 

#### Have the right cli version
1. Currently only versions 6 to 8 are supported
```
npm install -g @angular/cli@8.3.25

```

#### Create the app
```
ng new <app-name>
```

#### Add amplify modules
```
npm i aws-amplify aws-amplify-angular --save
```

### Init amplify

```
amplify init 
```

used default options here along side with the profile created using amplify configure

NOTE: to be able to use this command i have to create the following env var
```
set NODE_TLS_REJECT_UNAUTHORIZED=0
```

### Adding API

amplify add api
> GraphQL
> amplifyPoc
> Amazon Cognito User Pool

### Generate code 
amplify codegen
