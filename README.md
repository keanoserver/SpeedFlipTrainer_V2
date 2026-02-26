# SpeedFlipTrainer (BakkesMod Plugin)

This is a C++ BakkesMod plugin (`.dll`) for practicing and measuring speed flips.

## Build in Visual Studio (recommended)

1. Install **Visual Studio 2019 or 2022** with the **Desktop development with C++** workload.
2. Open `SpeedFlipTrainer.sln`.
3. In the top toolbar, set:
   - **Configuration:** `Release`
   - **Platform:** `x64`
4. Build the plugin:
   - **Build > Build Solution** (or press `Ctrl+Shift+B`).
5. If build succeeds, the DLL is output to:
   - `plugins\SpeedFlipTrainer.dll` (at repo root)

> The project is configured as a **DynamicLibrary** and outputs to `$(SolutionDir)plugins\`.

## If build fails with BakkesMod SDK/include/lib errors

This project imports `SpeedFlipTrainer/BakkesMod.props`, so your BakkesMod SDK paths must be set there (or in your local user props) before it can compile.

## Install into BakkesMod

1. Copy `plugins\SpeedFlipTrainer.dll`.
2. Paste into your BakkesMod plugin folder:
   - `%AppData%\bakkesmod\bakkesmod\plugins\`
3. Restart Rocket League (or reload plugins via BakkesMod console).

## Use in Rocket League

1. Launch Rocket League with BakkesMod running.
2. Open **F2 -> Plugins -> SpeedFlipTrainer**.
3. Enable/disable meters and configure thresholds from the plugin settings.

### Reset to defaults with a keybind

- In plugin settings, set **Reset key** (default `F7`) and click **Apply reset keybind**.
- Press that key in game to reset SpeedFlipTrainer settings/state back to defaults.
- You can also click **Reset now** in the same settings section.

## Build from command line (optional)

From a **Developer Command Prompt for VS** in the repo root:

```bat
msbuild SpeedFlipTrainer.sln /p:Configuration=Release /p:Platform=x64 /m
```

The DLL will still be written to `plugins\SpeedFlipTrainer.dll`.
