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

### [list-entities](https://docs.aws.amazon.com/cli/latest/reference/iottwinmaker/list-entities.html)

```java
$ aws iottwinmaker list-entities --workspace-id MyWorkspace --region us-east-1
{
    "entitySummaries": [
        {
            "arn": "arn:aws:iottwinmaker:us-east-1:677146750822:workspace/MyWorkspace/entity/a2cb48b1-e30b-4564-9f4e-5310abd2be27",
            "creationDateTime": "2022-07-05T14:52:17.676000+09:00",
            "description": "",
            "entityId": "a2cb48b1-e30b-4564-9f4e-5310abd2be27",
            "entityName": "Cabinet1",
            "hasChildEntities": false,
            "parentEntityId": "$ROOT",
            "status": {
                "error": {},
                "state": "ACTIVE"
            },
            "updateDateTime": "2022-07-09T09:52:47.302000+09:00"
        },
        {
            "arn": "arn:aws:iottwinmaker:us-east-1:677146750822:workspace/MyWorkspace/entity/ecac81ef-5ffe-4ea4-89f0-3b63d58a0804",
            "creationDateTime": "2022-07-05T14:51:03.480000+09:00",
            "description": "",
            "entityId": "ecac81ef-5ffe-4ea4-89f0-3b63d58a0804",
            "entityName": "Cabinets",
            "hasChildEntities": false,
            "parentEntityId": "$ROOT",
            "status": {
                "error": {},
                "state": "ACTIVE"
            },
            "updateDateTime": "2022-07-09T09:52:39.745000+09:00"
        },
        {
            "arn": "arn:aws:iottwinmaker:us-east-1:677146750822:workspace/MyWorkspace/entity/32847fed-27fb-4ff3-af6f-c540e7bed317",
            "creationDateTime": "2022-07-05T12:34:53.894000+09:00",
            "description": "",
            "entityId": "32847fed-27fb-4ff3-af6f-c540e7bed317",
            "entityName": "Mixers",
            "hasChildEntities": false,
            "parentEntityId": "$ROOT",
            "status": {
                "error": {},
                "state": "ACTIVE"
            },
            "updateDateTime": "2022-07-05T12:37:22.688000+09:00"
        },
        {
            "arn": "arn:aws:iottwinmaker:us-east-1:677146750822:workspace/MyWorkspace/entity/e8daadc5-35fe-4dcb-932a-1bb160638a3d",
            "creationDateTime": "2022-07-05T14:16:23.467000+09:00",
            "description": "",
            "entityId": "e8daadc5-35fe-4dcb-932a-1bb160638a3d",
            "entityName": "Factory",
            "hasChildEntities": false,
            "parentEntityId": "$ROOT",
            "status": {
                "error": {},
                "state": "ACTIVE"
            },
            "updateDateTime": "2022-07-05T14:16:23.467000+09:00"
        },
        {
            "arn": "arn:aws:iottwinmaker:us-east-1:677146750822:workspace/MyWorkspace/entity/491495d6-4709-496b-ad8a-e2af99ac0e55",
            "creationDateTime": "2022-07-05T14:17:31.858000+09:00",
            "description": "",
            "entityId": "491495d6-4709-496b-ad8a-e2af99ac0e55",
            "entityName": "Conveyor1",
            "hasChildEntities": false,
            "parentEntityId": "$ROOT",
            "status": {
                "error": {},
                "state": "ACTIVE"
            },
            "updateDateTime": "2022-07-09T09:52:24.171000+09:00"
        },
        {
            "arn": "arn:aws:iottwinmaker:us-east-1:677146750822:workspace/MyWorkspace/entity/2e24a3f2-05de-40a7-85e0-ae27e54a55a4",
            "creationDateTime": "2022-07-05T14:16:50.865000+09:00",
            "description": "",
            "entityId": "2e24a3f2-05de-40a7-85e0-ae27e54a55a4",
            "entityName": "Conveyors",
            "hasChildEntities": false,
            "parentEntityId": "$ROOT",
            "status": {
                "error": {},
                "state": "ACTIVE"
            },
            "updateDateTime": "2022-07-05T14:16:50.865000+09:00"
        }
    ]
}
```

#### [entity 삭제](https://docs.aws.amazon.com/cli/latest/reference/iottwinmaker/delete-entity.html)

```java
$ aws iottwinmaker delete-entity --entity-id a2cb48b1-e30b-4564-9f4e-5310abd2be27 --workspace-id MyWorkspace --region us-east-1
```


## Reference

[AWS IoT TwinMaker 정식 출시 – 디지털 트윈 서비스](https://aws.amazon.com/ko/blogs/korea/aws-iot-twinmaker-is-now-generally-available/)

[AWS IoT TwinMaker Getting Started](https://github.com/aws-samples/aws-iot-twinmaker-samples)
