# Eiffel Rocket New Wave

AI-assisted 3D animation test for a French music history documentary: the
Eiffel Tower becomes the rocket.

The project is a creative fork in spirit from a Blender rocket-launch tutorial
recreation. The technical goal is now different: use the working smoke, flame,
and launch rig as a base for a short, polished, historically anchored animation
with a retro 1950s French New Wave feel.

## Creative Goal

Create a short documentary insert about French music history, using a surreal
Eiffel Tower launch as the image. The target look is not generic vintage Paris;
it should feel connected to postwar Left Bank culture, chanson, jazz cellars,
Saint-Germain-des-Pres, and French New Wave film language.

Current visual direction:

- Eiffel Tower launches like a rocket.
- Existing smoke and flame simulation remains the physical base.
- Final shot direction should move toward black-and-white 4:3 framing, film
  grain, jump-cut energy, and a Paris/Left Bank miniature set.

## Credits and Sources

- Original Blender rocket launch tutorial: Blender Made Easy,
  <https://www.youtube.com/watch?v=xjzhd62ZAKg>
- Technical base repo:
  <https://github.com/d-b-w-gain/blender-rocket-launch-demo>
- Rocket model source and license notes:
  `assets/rocket/SOURCE.md`
- HDRI/backplate source and license notes:
  `assets/hdri/SOURCE.md`
- Eiffel Tower asset notes:
  `assets/eifel_tower/SOURCE.md`

The Eiffel Tower asset source/license is not yet fully documented. Treat that
as a release blocker for any public/final packaged render or reusable asset
distribution beyond this working repository.

## Run

Generate the Blender scene:

```powershell
& "C:\Program Files (x86)\Steam\steamapps\common\Blender\blender.exe" --python scripts\rocket_launch_demo.py
```

Run validation bakes/renders:

```powershell
& "C:\Program Files (x86)\Steam\steamapps\common\Blender\blender.exe" --background --python scripts\validate_bakes.py
```

Generated files go under `renders/` and are ignored by Git except for
`renders/.gitkeep`.

## Project Map

```text
assets/     Required model and lighting assets plus source notes.
docs/       Creative sequence, shot planning, and documentary context.
reference/  Original tutorial transcript/keyframes used for the launch rig.
scripts/    Blender scene generation and validation scripts.
renders/    Local generated renders, caches, and Blender output.
```
