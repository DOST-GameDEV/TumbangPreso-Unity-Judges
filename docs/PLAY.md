# Play from source

## Open the project

1. Install [Unity 6000.5.8f1](https://unity.com/releases/editor/whats-new/6000.5.8f1) in Unity Hub.
2. Clone the repository. Allow several gigabytes for the checkout and additional space for Unity's import cache.

   ```sh
   git clone https://github.com/DOST-GameDEV/TumbangPreso-Unity-Judges.git
   ```

3. In Unity Hub, choose **Add → Add project from disk** and select the folder containing `Assets`, `Packages`, and `ProjectSettings`. Let the first import finish. Unity downloads the dependencies listed in the package manifest.
4. In the Project window, open `Assets/TumbangPreso/Scenes/Ui/SplashScreen.unity`. Press **Play**, focus the **Game** view, and continue as **Guest** when prompted.

## Solo review

| Route from Home | What to try |
| --- | --- |
| **Gamemode → Practice → Tutorial** | Learn how to charge and curve throws, retrieve your slipper, use skills, and defend the can. Follow the current on-screen bindings. |
| **Gamemode → Practice → Training** | Play against active bots. Use **Rules** in the Practice menu to inspect match settings and bot difficulty. |
| **Gamemode → Custom → Host → LAN** | Set up a full match with other reviewers. Read the room's rules and choose a mode before starting. |

### A quick round

- **Attacker.** Aim at the lata from behind the chalk line. Hold and release **left mouse** to throw, then run in and use **right mouse** to retrieve your slipper. Head back across the line before the taya tags you.
- **Taya.** Guard the lata. Follow the contextual grab prompt to put a knocked can upright. Use the lunge control when a vulnerable attacker enters range.
- **Hero Strike.** Press **E** or **Q** for the two skills and **X** for the ultimate when it is ready. Open the ability information with **F1**.

The default desktop bindings include **WASD** to move, **mouse** to look, **Shift** to sprint, **Space** to jump, **middle mouse** to lunge or shove, and the **mouse wheel** to add throw curve. The in-game prompts reflect any rebinding and the current control scheme.

## LAN review

Use the same revision on each computer and connect them to the same local network. On the host, go to **Gamemode → Custom → Host → LAN**. On the other computers, choose **Gamemode → Custom → Join** and select the host's room. If LAN discovery is unavailable, use the join field with the host's local address. Fill four player seats with people or bots, ready the players, and start from the host. Where the room offers **Spectate**, an observer can watch without taking a player seat.

If a room is missing, confirm the computers are on the same network and that the OS firewall permits the game traffic on that network. A school or guest network may isolate devices. Use offline Practice as the fallback.

The snapshot is unlinked from BH Studios' Unity Gaming Services. Practice and LAN are the evaluation routes. Internet matchmaking, online room codes, sign-in, and cloud saves require a separately configured service deployment.
