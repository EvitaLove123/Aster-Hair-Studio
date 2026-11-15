# Aster Hair Studio

Android-first browser workspace for previewing VRM characters and fitting external hair assets.

## Current features
- Load and preview VRM models in the browser.
- Import external hair as GLB, glTF, or FBX.
- Select hair mesh nodes and adjust position, scale, and Y rotation.
- Attach the selected hair object to the character's raw Head bone.
- Export the complete loaded character as **VRM 0.x** or **VRM 1.0**.
- Export a selected hair object separately as GLB.

## VRM export workflow
1. Load a VRM character.
2. Import the hair asset.
3. Select the hair group or mesh in Hair Outliner.
4. Adjust its transform.
5. Press **Attach to Head**.
6. Choose **Download VRM 0.x** or **Download VRM 1.0**.

The VRM exporter is based on the MIT-licensed [Ringo3apples/vrm-exporter](https://github.com/Ringo3apples/vrm-exporter) module. It runs in the browser and uses the loaded VRM instance. Exported results still need validation in the target apps.

## Not implemented yet
- Automatic Hair Fitter (auto scalp alignment, clipping correction).
- Hair Spring Bone group authoring and collider editing.
- Guaranteed preservation of every custom VRM extension/material feature for every model.
- Automatic conversion/retargeting of arbitrary FBX hair rigs.

## GitHub Pages
In **Settings → Pages**, select **Deploy from a branch**, branch `main`, folder `/(root)`, then save.

Published URL: https://evitalove123.github.io/Aster-Hair-Studio/

## Notes
- Three.js, three-vrm, and the VRM exporter module load from CDNs; an internet connection is required.
- Model processing occurs locally in the browser; the app does not upload model files.
- Test exports on copies of your models first. Large models may exceed Android browser memory limits.
