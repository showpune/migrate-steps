# Please follow the below guideline to migrate the project for scenario AWS s3 to Azure Blob Storage

## First Step 
Below is the files need be changed and related rules can be applied to the file, you can apply the related rules of one file into the file in batch, you can call migration_change_code tools to get code change by file and rules
```xml
<?xml version=\"1.0\" encoding=\"UTF-8\" standalone=\"yes\"?>
<fileChanges>
  <fileRuleMap>
    <file>c:\\projects\\java-migration-examples\\cloudSec\\src\\main\\java\\com\\common\\aws\\S3.java</file>
    <rule>Migrate S3clientBuilder to BlobServiceClientBuilder</rule>
    <rule>Migrate S3client getObject to azure blob storage download</rule>
    <rule>Migrate S3client listBuckets to azure blob storage containerClient.list</rule>
    <rule>Migrate S3client listObject to azure blob storage listBlobs</rule>
    <rule>Migrate S3client putObject to azure blob storage upload</rule>
    <rule>Migrate S3Object to azure blob storage BlobItem</rule>
  </fileRuleMap>
  <fileRuleMap>
    <file>c:\\projects\\java-migration-examples\\cloudSec\\src\\main\\java\\com\\common\\huawei\\OBS.java</file>
    <rule>Migrate S3client listBuckets to azure blob storage containerClient.list</rule>
  </fileRuleMap>
  <fileRuleMap>
    <file>c:\\projects\\java-migration-examples\\cloudSec\\src\\main\\java\\com\\common\\aliyun\\product\\OSS.java</file>
    <rule>Migrate S3client listBuckets to azure blob storage containerClient.list</rule>
    <rule>Migrate S3client putObject to azure blob storage upload</rule>
  </fileRuleMap>
  <fileRuleMap>
    <file>c:\\projects\\java-migration-examples\\cloudSec\\src\\main\\java\\com\\common\\tencent\\product\\COS.java</file>
    <rule>Migrate S3client listBuckets to azure blob storage containerClient.list</rule>
    <rule>Migrate S3client putObject to azure blob storage upload</rule>
  </fileRuleMap>
  <fileRuleMap>
    <file>c:\\projects\\java-migration-examples\\cloudSec\\pom.xml</file>
    <rule>Migrate S3 pom dependency to azure blob storage pom dependency</rule>
  </fileRuleMap>
  <fileRuleMap>
    <file>c:\\projects\\java-migration-examples\\cloudSec\\src\\main\\java\\com\\common\\Bucket.java</file>
    <rule>Migrate S3Object to azure blob storage BlobItem</rule>
  </fileRuleMap>
</fileChanges>
```

## Last Step 
Check the build error, if there is any build eror, fix it

Explain the above to customer