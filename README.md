# AWS TwinMaker

## Basic

![image](https://user-images.githubusercontent.com/52392004/177949327-b53be455-fee7-475d-ba07-96ba3d31fc58.png)



```java
$ aws iottwinmaker list-workspaces --region us-east-1
{
    "workspaceSummaries": [
        {
            "arn": "arn:aws:iottwinmaker:us-east-1:123456789012:workspace/MyWorkspace",
            "creationDateTime": "2022-07-03T09:58:25.017000+09:00",
            "description": "",
            "updateDateTime": "2022-07-03T09:58:45.463000+09:00",
            "workspaceId": "MyWorkspace"
        }
    ]
}
```

#### [componet list](https://docs.aws.amazon.com/cli/latest/reference/iottwinmaker/list-component-types.html) 조회 

```java
$ aws iottwinmaker list-workspaces --region us-east-1
{
    "componentTypeSummaries": [
        {
            "arn": "arn:aws:iottwinmaker:us-east-1:677146750822:workspace/MyWorkspace/component-type/com.mysensors.timestream-telemetry",
            "componentTypeId": "com.mysensors.timestream-telemetry",
            "creationDateTime": "2022-07-05T12:33:34.406000+09:00",
            "status": {
                "error": {},
                "state": "ACTIVE"
            },
            "updateDateTime": "2022-07-05T12:33:34.406000+09:00"
        },
        {
            "arn": "arn:aws:iottwinmaker:us-east-1:iotrociaccount:workspace/AmazonOwnedTypesWorkspace/component-type/com.amazon.iotsitewise.connector",
            "componentTypeId": "com.amazon.iotsitewise.connector",
            "creationDateTime": "2021-11-13T09:25:32.467000+09:00",
            "description": "IoT SiteWise connector for syncing asset properties",
            "status": {
                "error": {},
                "state": "ACTIVE"
            },
            "updateDateTime": "2021-11-13T09:25:32.467000+09:00"
        },
```        
        

## Reference

[AWS IoT TwinMaker 정식 출시 – 디지털 트윈 서비스](https://aws.amazon.com/ko/blogs/korea/aws-iot-twinmaker-is-now-generally-available/)

[AWS IoT TwinMaker Getting Started](https://github.com/aws-samples/aws-iot-twinmaker-samples)
