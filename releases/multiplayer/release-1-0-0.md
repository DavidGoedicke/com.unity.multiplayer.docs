---
id: release-1.0.0
title: Netcode 1.0.0 - 21-10-2021
description: In-progress release notes for the next release of Unity Netcode for GameObjects (Netcode) including new features, updates, bug fixes, known issues, and information to help you upgrade.
---

The following in-progress content tracks features, updates, bug fixes, and refactoring for the next release of Unity Netcode. Specific release information including supported Unity versions, release date, and release version is to be announced. All content and development information is subject to change.

This release contains features, updates, bug fixes, and refactoring for the  Netcode for GameObjects v1.0.0 Pre-Release.

| Product | Version | Status | Release Date | Supported Unity Versions |
| -- | -- | -- | -- | -- |
| Netcode for GameObjects | 1.0.0| Pre-Release | October 21, 2021 | 2020.3 and later |

:::note
Netcode for GameObjects supports Windows, MacOS, Ubuntu 20.4 LTS and Ubuntu 18.04 LTS versions of Unity Editor and Player
:::
### Added

- Added `ClientNetworkTransform` sample to the SDK package [#1168](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1168?w=1)
- Added `Bootstrap` sample to the SDK package [#1140](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1140?w=1)
- Enhanced `NetworkSceneManager` implementation with additive scene loading capabilities [#1080](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1080?w=1), [#955](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/955?w=1), [#913](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/913?w=1)
  - `NetworkSceneManager.OnSceneEvent` provides improved scene event notificaitons  
- Enhanced `NetworkTransform` implementation with per axis/component based and threshold based state replication [#1042](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1042?w=1), [#1055](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1055?w=1), [#1061](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1061?w=1), [#1084](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1084?w=1), [#1101](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1101?w=1)
- Added a jitter-resistent `BufferedLinearInterpolator<T>` for `NetworkTransform` [#1060](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1060?w=1)
- Implemented `NetworkPrefabHandler` that provides support for object pooling and `NetworkPrefab` overrides [#1073](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1073?w=1), [#1004](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1004?w=1), [#977](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/977?w=1), [#905](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/905?w=1),[#749](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/749?w=1), [#727](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/727?w=1)
- Implemented auto `NetworkObject` transform parent synchronization at runtime over the network [#855](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/855?w=1)
- Adopted Unity C# Coding Standards in the codebase with `.editorconfig` ruleset [#666](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/666?w=1), [#670](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/670?w=1)
- When a client tries to spawn a `NetworkObject` an exception is thrown to indicate unsupported behavior. [#981](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/981?w=1)
- Added a `NetworkTime` and `NetworkTickSystem` which allows for improved control over time and ticks. [#845](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/845?w=1)
- Added a `OnNetworkDespawn` function to `NetworkObject` which gets called when a `NetworkObject` gets despawned and can be overriden. [#865](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/865?w=1)
- Added `SnapshotSystem` that would allow variables and spawn/despawn messages to be sent in blocks [#805](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/805?w=1), [#852](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/852?w=1), [#862](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/862?w=1), [#963](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/963?w=1), [#1012](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1012?w=1), [#1013](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1013?w=1), [#1021](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1021?w=1), [#1040](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1040?w=1), [#1062](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1062?w=1), [#1064](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1021?w=1), [#1083](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1083?w=1), [#1091](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1091?w=1), [#1111](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1111?w=1), [#1129](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1129?w=1), [#1166](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1166?w=1), [#1192](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1192?w=1)
  - Disabled by default for now, except spawn/despawn messages
  - Will leverage unreliable messages with eventual consistency
- `NetworkBehaviour` and `NetworkObject`'s `NetworkManager` instances can now be overriden [[#762](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/762?w=1)
- Added metrics reporting for the new network profiler if the Multiplayer Tools package is present [#1104](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1104?w=1), [#1089](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1089?w=1), [#1096](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1096?w=1), [#1086](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1086?w=1), [#1072](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1072?w=1), [#1058](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1058?w=1), [#960](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/960?w=1), [#897](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/897?w=1), [#891](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/891?w=1), [#878](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/878?w=1)
- `NetworkBehaviour.IsSpawned` a quick (and stable) way to determine if the associated NetworkObject is spawned [#1190](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1190?w=1)
- Added `NetworkRigidbody` and `NetworkRigidbody2D` components to support networking `Rigidbody` and `Rigidbody2D` components [#1202](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1202?w=1), [#1175](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1175?w=1)
- Added `NetworkObjectReference` and `NetworkBehaviourReference` structs which allow to sending `NetworkObject/Behaviours` over RPCs/`NetworkVariable`s [#1173](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1173?w=1)
- Added `NetworkAnimator` component to support networking `Animator` component [#1281](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1281?w=1), [#872](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/872?w=1)


### Changed

- Bumped minimum Unity version, renamed package as "Unity Netcode for GameObjects", replaced `MLAPI` namespace and its variants with `Unity.Netcode` namespace and per asm-def variants [#1007](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1007?w=1), [#1009](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1009?w=1), [#1015](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1015?w=1), [#1017](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1017?w=1), [#1019](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1019?w=1), [#1025](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1025?w=1), [#1026](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1026?w=1), [#1065](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1065?w=1)
  - Minimum Unity version:
    - 2019.4 → 2020.3+
  - Package rename:
    - Display name: `MLAPI Networking Library` → `Netcode for GameObjects`
    - Name: `com.unity.multiplayer.mlapi` → `com.unity.netcode.gameobjects`
    - Updated package description
  - All `MLAPI.x` namespaces are replaced with `Unity.Netcode`
    - `MLAPI.Messaging` → `Unity.Netcode`
    - `MLAPI.Connection` → `Unity.Netcode`
    - `MLAPI.Logging` → `Unity.Netcode`
    - `MLAPI.SceneManagement` → `Unity.Netcode`
    - and other `MLAPI.x` variants to `Unity.Netcode`
  - All assembly definitions are renamed with `Unity.Netcode.x` variants
    - `Unity.Multiplayer.MLAPI.Runtime` → `Unity.Netcode.Runtime`
    - `Unity.Multiplayer.MLAPI.Editor` → `Unity.Netcode.Editor`
    - and other `Unity.Multiplayer.MLAPI.x` variants to `Unity.Netcode.x` variants
- Renamed `Prototyping` namespace and assembly definition to `Components` [#1145](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1145?w=1)
- Changed `NetworkObject.Despawn(bool destroy)` API to default to `destroy = true` for better usability [#1217](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1217?w=1)
- Scene registration in `NetworkManager` is now replaced by Build Setttings → Scenes in Build List [#1080](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1080?w=1)
- `NetworkSceneManager.SwitchScene` has been replaced by `NetworkSceneManager.LoadScene` [#955](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/955?w=1)
- `NetworkManager, NetworkConfig, and NetworkSceneManager` scene registration replaced with scenes in build list [#1080](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1080?w=1)
- `GlobalObjectIdHash` replaced `PrefabHash` and `PrefabHashGenerator` for stability and consistency [#698](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/698?w=1)
- `NetworkStart` has been renamed to `OnNetworkSpawn`. [#865](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/865?w=1)
- Network variable cleanup - eliminated shared mode, variables are server-authoritative [#1059](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1059?w=1), [#1074](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1074?w=1)
- `NetworkManager` and other systems are no longer singletons/statics [#696](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/696?w=1), [#705](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/705?w=1), [#706](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/706?w=1), [#737](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/737?w=1), [#738](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/738?w=1), [#739](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/739?w=1), [#746](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/746?w=1), [#747](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/747?w=1), [#763](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/763?w=1), [#765](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/765?w=1), [#766](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1168?w=1), [#783](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1168?w=1), [#784](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1168?w=1), [#785](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/785?w=1), [#786](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/786?w=1), [#787](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/787?w=1), [#788](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/788?w=1)
- Changed `INetworkSerializable.NetworkSerialize` method signature to use `BufferSerializer<T>` instead of `NetworkSerializer` [#1187](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1187?w=1)
- Changed `CustomMessagingManager`'s methods to use `FastBufferWriter` and `FastBufferReader` instead of `Stream` [#1187](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1187?w=1)
- Reduced internal runtime allocations by removing LINQ calls and replacing managed lists/arrays with native collections [#1196](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1196?w=1)

### Removed

- Removed `NetworkNavMeshAgent` [#1150](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1150?w=1)
- Removed `NetworkDictionary`, `NetworkSet` [#1149](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1149?w=1)
- Removed `NetworkVariableSettings` [#1097](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1097?w=1)
- Removed predefined `NetworkVariable<T>` types [#1093](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1093?w=1)
    - Removed `NetworkVariableBool`, `NetworkVariableByte`, `NetworkVariableSByte`, `NetworkVariableUShort`, `NetworkVariableShort`, `NetworkVariableUInt`, `NetworkVariableInt`, `NetworkVariableULong`, `NetworkVariableLong`, `NetworkVariableFloat`, `NetworkVariableDouble`, `NetworkVariableVector2`, `NetworkVariableVector3`, `NetworkVariableVector4`, `NetworkVariableColor`, `NetworkVariableColor32`, `NetworkVariableRay`, `NetworkVariableQuaternion`
- Removed `NetworkChannel` and `MultiplexTransportAdapter` [#1133](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1133?w=1)
- Removed ILPP backend for 2019.4, minimum required version is 2020.3+ [#895](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/895?w=1)
- `NetworkManager.NetworkConfig` had the following properties removed: [#1080](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1080?w=1)
  - Scene Registrations no longer exists
  - Allow Runtime Scene Changes was no longer needed and was removed
- Removed the NetworkObject.Spawn payload parameter [#1005](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1005?w=1)
- Removed `ProfilerCounter`, the original MLAPI network profiler, and the built-in network profiler module (2020.3). A replacement can now be found in the Multiplayer Tools package. [#1048](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1048?w=1)
- Removed UNet RelayTransport and related relay functionality in UNetTransport [#1081](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1081?w=1)
- Removed `UpdateStage` parameter from `ServerRpcSendParams` and `ClientRpcSendParams` [#1187](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1187?w=1)
- Removed `NetworkBuffer`, `NetworkWriter`, `NetworkReader`, `NetworkSerializer`, `PooledNetworkBuffer`, `PooledNetworkWriter`, and `PooledNetworkReader` [#1187](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1187?w=1)
- Removed `EnableNetworkVariable` in `NetworkConfig`, it is always enabled now [#1179](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1179?w=1)
- Removed `NetworkTransform`'s FixedSendsPerSecond, AssumeSyncedSends, InterpolateServer, ExtrapolatePosition, MaxSendsToExtrapolate, Channel, EnableNonProvokedResendChecks, DistanceSendrate [#1060](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1060?w=1) [#826](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/826?w=1) ([#1042](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1042?w=1), [#1055](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1055?w=1), [#1061](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1061?w=1), [#1084](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1084?w=1), [#1101](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1101?w=1))
- Removed `NetworkManager`'s `StopServer()`, `StopClient()` and `StopHost()` methods and replaced with single `NetworkManager.Shutdown()` method for all [#1108](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1108?w=1)

### Fixed

- Fixed ServerRpc ownership check to `Debug.LogError` instead of `Debug.LogWarning` [#1126](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1126?w=1)
- Fixed `NetworkObject.OwnerClientId` property changing before `NetworkBehaviour.OnGainedOwnership()` callback [#1092](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1092?w=1)
- Fixed `NetworkBehaviourILPP` to iterate over all types in an assembly [#803](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/803?w=1)
- Fixed cross-asmdef RPC ILPP by importing types into external assemblies [#678](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/678?w=1)
- Fixed `NetworkManager` shutdown when quitting the application or switching scenes [#1011](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1011?w=1)
  - Now `NetworkManager` shutdowns correctly and despawns existing `NetworkObject`s
- Fixed Only one `PlayerPrefab` can be selected on `NetworkManager` inspector UI in the editor [#676](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/676?w=1)
- Fixed connection approval not being triggered for host [#675](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/675?w=1)
- Fixed various situations where messages could be processed in an invalid order, resulting in errors [#948](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/948?w=1), [#1187](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1187?w=1), [#1218](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1218?w=1)
- Fixed `NetworkVariable`s being default-initialized on the client instead of being initialized with the desired value [#1266](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1266?w=1)
- Improved runtime performance and reduced GC pressure [#1187](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1187?w=1)
- Fixed #915 - clients are receiving data from objects not visible to them [#1099](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/1099?w=1)
- Fixed `NetworkTransform`'s "late join" issues, `NetworkTransform` now uses `NetworkVariable`s instead of RPCs [#826](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/826?w=1)
- Throw an exception for silent failure when a client tries to get another player's `PlayerObject`, it is now only allowed on the server-side [#844](https://github.com/Unity-Technologies/com.unity.netcode.gameobjects/pull/844?w=1)

### Known Issues

- `NetworkVariable` does not serialize `INetworkSerializable` types through their `NetworkSerialize` implementation
- `NetworkObjects` marked as `DontDestroyOnLoad` are disabled during some network scene transitions
- `NetworkTransform` interpolates from the origin when switching Local Space synchronization
- Exceptions thrown in `OnNetworkSpawn` user code for an object will prevent the callback in other objects
- Cannot send an array of `INetworkSerializable` in RPCs
- ILPP generation fails with special characters in project path