To obtain in-game models and textures:

1). Open "UModel" and set "Path to game files:" to "C:\Program Files (x86)\Steam\steamapps\common\Borderlands" Note: NOT Borderlands GOTY enhanced :(

2). Make sure all boxes in "View / export object types" are checked

3). Press "OK"

4). Under "Package name" select "W_STARTUP_[any 3 letter localization code]" and select "open"

5). Use "Page Up" and "Page Down" to navigate the assets in the game!

6). When you want to export click "Tools", "Export current object", I typically set "Use uncooked UE3 package names" so that my directory structure matches that of the in-game assets

7). Make sure to use TGA uncompressed for the texture format

8). If exporting 3d models, you need to import the models again using the provided script under ActionXImporter, make sure to set the texture directory to the root directory of your UModelExports folder!

9). Do not forget to delete the "bones" in the 3d model before exporting again, these are the small white pyramid structures. These are used by the game for animations I think but we do not need them. The coordinate space of the parts is correct (when importing exported .obj files, relative space to other parts is fine, see OnShape document)

10). To see the detailed textures change the "k_d" line in the .mtl files from "..._color.tga" to "..._light.tga" but using the normals might be cleaner