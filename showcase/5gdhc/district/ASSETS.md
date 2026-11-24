# District scene assets (U12)

> 이 소개 페이지 배포본에서는 `textures/*.jpg` 6개를 같은 해상도로 JPG 품질 85로 다시 저장했습니다. 아래 표의 크기와 해시는 내려받은 원본 기준입니다.


Third-party files used by `district.html`. All are CC0 1.0 (public domain dedication, no attribution required).
Files are byte-identical to the download, except the six JPGs re-encoded for this page (note above). Fetched 2026-11-20. Total 7,856,016 bytes.

| File | Kind | Source | Author | Licence | Bytes | sha256 |
|---|---|---|---|---|---|---|
| `hdri/kloofendal_48d_partly_cloudy_puresky_1k.hdr` | HDRI, day (partly cloudy, sky only), 1k RGBE | https://polyhaven.com/a/kloofendal_48d_partly_cloudy_puresky (file: https://dl.polyhaven.org/file/ph-assets/HDRIs/hdr/1k/kloofendal_48d_partly_cloudy_puresky_1k.hdr) | Greg Zaal (original), Jarod Guest (sky edits), Poly Haven | CC0 1.0 (https://polyhaven.com/license) | 1435119 | `fd94c84997b8a3c353b62c2125a9b44e19509956986a126e472684432a02d798` |
| `hdri/qwantani_dusk_2_puresky_1k.hdr` | HDRI, dusk (sky only), 1k RGBE | https://polyhaven.com/a/qwantani_dusk_2_puresky (file: https://dl.polyhaven.org/file/ph-assets/HDRIs/hdr/1k/qwantani_dusk_2_puresky_1k.hdr) | Greg Zaal (photography), Jarod Guest (processing), Poly Haven | CC0 1.0 (https://polyhaven.com/license) | 1166018 | `56dc9cb681f2641c08377e20e83fa5e4865fd900bcce26a15a1883580139b5e2` |
| `textures/Asphalt010_1K-JPG_Color.jpg` | PBR asphalt, base colour, 1024² | https://ambientcg.com/view?id=Asphalt010 (zip: https://ambientcg.com/get?file=Asphalt010_1K-JPG.zip) | ambientCG (page names no individual author) | CC0 1.0 (https://ambientcg.com/license) | 1093417 | `412598f9cfa046ff222a76ecd66fde576e42f5141938ffe3be2e2c0e9082e5c8` |
| `textures/Asphalt010_1K-JPG_NormalGL.jpg` | PBR asphalt, normal (OpenGL, +Y), 1024² | same zip | ambientCG (page names no individual author) | CC0 1.0 | 2105657 | `2dce239d12302f29d57ad92fe92377ca0533a17628a535a5d07677c10884617e` |
| `textures/Asphalt010_1K-JPG_Roughness.jpg` | PBR asphalt, roughness, 1024² grey | same zip | ambientCG (page names no individual author) | CC0 1.0 | 746915 | `5f0f9ee453565de9fdf838140a425f59b215ca3c87a3c269e39247d6f688c13f` |
| `textures/Concrete034_1K-JPG_Color.jpg` | PBR concrete, base colour, 1024×512 | https://ambientcg.com/view?id=Concrete034 (zip: https://ambientcg.com/get?file=Concrete034_1K-JPG.zip) | ambientCG (page names no individual author) | CC0 1.0 (https://ambientcg.com/license) | 269501 | `8ceb9186d990b31fce785e06fdc6974c160f1d27c43f6160266f164deba713aa` |
| `textures/Concrete034_1K-JPG_NormalGL.jpg` | PBR concrete, normal (OpenGL, +Y), 1024×512 | same zip | ambientCG (page names no individual author) | CC0 1.0 | 821681 | `e509eb9dfa978e780fbebfd2acacc2ce158b5b7ced722ddc0759039dd51e18ca` |
| `textures/Concrete034_1K-JPG_Roughness.jpg` | PBR concrete, roughness, 1024×512 grey | same zip | ambientCG (page names no individual author) | CC0 1.0 | 217708 | `a4a9e39857a19afd23a778e5abf44fcdf6bd7f93918f1cf6878b41933e553511` |

Notes
- HDRIs load with `three/addons/loaders/HDRLoader.js` (RGBELoader is deprecated since r180) and go through `PMREMGenerator.fromEquirectangular` for `scene.environment`. Both are "pure sky" variants (no ground objects), so they do not put a foreign landscape into reflections.
- ambientCG normals are the GL variant: use as-is with three (`normalScale` positive). Colour maps need `colorSpace = SRGBColorSpace`; normal and roughness stay linear.
- Unused files can be deleted with their row; nothing else references them.

Not staged
- Trees: Kenney Nature Kit (CC0) models are 5-31 KB but toy-like block shapes, not more realistic than the procedural trees. Poly Haven tree models are 66-958 MB per glTF set. Trees stay procedural.
- Terrain DEM: not downloaded. Copernicus GLO-30 (tile N37 E127 is public) needs the attribution "© DLR e.V. 2010-2014 and © Airbus Defence and Space GmbH 2014-2018 provided under COPERNICUS by the European Union and ESA; all rights reserved" next to the OSM credit if ever used.
