---  
id: Unity.Netcode.SceneEventType  
title: Unity.Netcode.SceneEventType  
---

<div class="markdown level0 summary">

The different types of scene events communicated between a server and
client. Used by NetworkSceneManager for Unity.Netcode.SceneEventMessage
messages Note: This is only when EnableSceneManagement is enabled See
also: SceneEvent

</div>

<div class="markdown level0 conceptual">

</div>

##### **Namespace**: System.Dynamic.ExpandoObject

##### **Assembly**: MLAPI.dll

##### Syntax

``` lang-csharp
public enum SceneEventType : byte
```

## 

| Name                 | Description                                                                                                                                                                                                                                                                                                                                               |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Load                 | Load a scene Invocation: Server Side Message Flow: Server to client Event Notification: Both server and client are notified a load scene event started                                                                                                                                                                                                    |
| LoadComplete         | A client has finished loading a scene Invocation: Client Side Message Flow: Client to Server Event Notification: Both server and client receive a local notification                                                                                                                                                                                      |
| LoadEventCompleted   | All clients have finished loading a scene Invocation: Server Side Message Flow: Server to Client Event Notification: Both server and client receive a local notification containing the clients that finished as well as the clients that timed out (if any).                                                                                             |
| ReSynchronize        | Game session re-synchronization of NetworkObjects that were destroyed during a Synchronize event Invocation: Server Side Message Flow: Server to client Event Notification: Both server and client receive a local notification Note: This will be removed once snapshot and buffered messages are finalized as it will no longer be needed at that point |
| Synchronize          | Synchronize current game session state for approved clients Invocation: Server Side Message Flow: Server to client Event Notification: Server and Client receives a local notification (server receives the ClientId being synchronized)                                                                                                                  |
| SynchronizeComplete  | A client has finished synchronizing from a Synchronize event Invocation: Client Side Message Flow: Client to Server Event Notification: Both server and client receive a local notification                                                                                                                                                               |
| Unload               | Unload a scene Invocation: Server Side Message Flow: Server to client Event Notification: Both server and client are notified an unload scene event started                                                                                                                                                                                               |
| UnloadComplete       | A client has finished unloading a scene Invocation: Client Side Message Flow: Client to Server Event Notification: Both server and client receive a local notification                                                                                                                                                                                    |
| UnloadEventCompleted | All clients have unloaded a scene Invocation: Server Side Message Flow: Server to Client Event Notification: Both server and client receive a local notification containing the clients that finished as well as the clients that timed out (if any).                                                                                                     |
