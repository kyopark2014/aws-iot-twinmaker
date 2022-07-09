# AWS TwinMaker

## Basic

![image](https://user-images.githubusercontent.com/52392004/177949327-b53be455-fee7-475d-ba07-96ba3d31fc58.png)



```c
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

## Reference

[AWS IoT TwinMaker 정식 출시 – 디지털 트윈 서비스](https://aws.amazon.com/ko/blogs/korea/aws-iot-twinmaker-is-now-generally-available/)

[AWS IoT TwinMaker Getting Started](https://github.com/aws-samples/aws-iot-twinmaker-samples)
