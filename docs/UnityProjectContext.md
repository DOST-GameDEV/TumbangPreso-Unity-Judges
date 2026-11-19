# Unity project context

This judging snapshot is based on development revision [`d0e45d2`](https://github.com/DOST-GameDEV/TumbangPreso-Unity/commit/d0e45d2f08992c46c81d0e868b17c4c96a467e2e). The snapshot includes the project assets, source code, and tests. The original production service linkage is cleared.

## Source map

| Question | Open here |
| --- | --- |
| What are the rules and defaults? | [Engine-free Core](../Packages/com.tumbangpreso.core/Runtime), especially `Balance`, `MatchRules`, `CustomGameRules`, and `Roster` |
| Where do round transitions and scoring happen? | [MatchDirector](../Assets/TumbangPreso/Runtime/MatchDirector.cs) and [MatchHost](../Assets/TumbangPreso/Runtime/MatchHost.cs) |
| How do hero kits plug into the game? | [Abilities](../Assets/TumbangPreso/Runtime/Abilities) |
| How are multiplayer actions synchronized? | [NetAuthority](../Assets/TumbangPreso/Runtime/NetAuthority.cs) and the [network layer](../Assets/TumbangPreso/Runtime/Net) |
| Where are the menus and camera systems? | [UI](../Assets/TumbangPreso/Runtime/UI) and [Camera](../Assets/TumbangPreso/Runtime/Camera) |
| Where are the courts and scene order? | [Map scenes](../Assets/TumbangPreso/Scenes/Maps) and [Build Settings](../ProjectSettings/EditorBuildSettings.asset) |

The project uses Unity **6000.5.8f1**, URP, uGUI, Input System, and Netcode for GameObjects with embedded Unity Transport. The same engine-free rules compile into an embedded Unity package and the .NET Core project. Unity components implement scene lifecycle, input, physics, and presentation. The host owns match outcomes, including scoring and accepted actions.

The entry point is [SplashScreen.unity](../Assets/TumbangPreso/Scenes/Ui/SplashScreen.unity). The current Home and Gamemode screens lead to practice and custom rooms. [Play from source](PLAY.md) covers the entry routes.

## Validation and tests

Unity 6000.5.8f1 compiled the gameplay and test assemblies on a fresh checkout. The asset importer reported an error on the inherited [duskline model](../Assets/TumbangPreso/Resources/Models/UltimateProps/duskline.glb).

The focused [throw-guide PlayMode test](../Assets/TumbangPreso/Tests/PlayMode/LandingCircleTests.cs) passed on this revision. It checks the guide near the held slipper, dash spacing, and the landing preview during a charge.

Run the engine-free suite with the .NET 9 SDK from the repository root.

```sh
dotnet test Core.Tests/TumbangPreso.Core.Tests.csproj --nologo
```

The engine-free check on this snapshot passed **843 of 849** cases. Six inherited assertions disagree with the current four-round defaults, distance normalization, or the Voodoo status label. The original gameplay and test expectations are carried forward.

Unity [EditMode and PlayMode tests](../Assets/TumbangPreso/Tests) cover scene and runtime behavior. Open **Window → General → Test Runner** to inspect or run a focused check. Real multiplayer behavior requires multiple instances on the same revision, and service deployments are outside the scope of this snapshot.
