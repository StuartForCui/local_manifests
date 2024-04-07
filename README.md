![Evolution X](https://github.com/truly-irham/local_manifests/raw/14.0/EvoBanner.png)

Evolution X
===========

[![Download Evolution X](https://img.shields.io/sourceforge/dt/evolution-x.svg)](https://sourceforge.net/projects/evolution-x/files/latest/download)

### Syncing Evolution X Source Code ###

To initialize the uqpr2 manifest branch of Evolution X:

```bash
repo init -u https://github.com/Evolution-X/manifest -b uqpr2
```

### Syncing Xiaomi 12T Pro/RedmiK50Ultra "diting" dependencies for Evolution X uqpr2 ###

Please add this manifest to .repo/local_manifests before syncing:

```bash
# Execute this command inside your build directory

git clone https://github.com/truly-irham/local_manifests.git -b udc .repo/local_manifests
```

To sync all sources defined in the manifests, run:

```bash
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

NOTE: If you encounter sync error such as EOF, you would need to specify lower flags for syncing (i.e. -j4 or lower). Please also note that the sync process will take a long time depending on your internet connection.

### Changes required to build Evolution X for diting ###

There are some changes required to successfully build Evolution X for diting. To do that, simply put the `changes-evox-diting.sh` bash file inside the root of your build directory and run:

```bash
./changes-evox-diting.sh
```

### Build Evolution X for diting ###

Now, you are ready to build Evolution X for diting.

- Set up the build environment:

```bash
source build/envsetup.sh
```

- Choose a target:
```bash
lunch evolution_diting-userdebug
```

- To start compiling:
```bash
m evolution
```

# Credits:

| Project                           | GitHub Organization                        | Project                           | GitHub Organization                  |
|-----------------------------------|-------------------------------------------|-----------------------------------|---------------------------------------|
| LineageOS                         | [Link](https://github.com/LineageOS)      | crDroid                           | [Link](https://github.com/crdroidandroid) |
| ParanoidAndroid                   | [Link](https://github.com/AOSPA)          | Octavi-OS                         | [Link](https://github.com/Octavi-OS) |
| PixelDust                         | [Link](https://github.com/PixelDust-Twelve)   | hentaiOS                          | [Link](https://github.com/hentaiOS) |
| ProtonAOSP                        | [Link](https://github.com/ProtonAOSP)     | POSP                              | [Link](https://github.com/PotatoProject) |
| BlissROMs                         | [Link](https://github.com/BlissRoms)      | StatiXOS                          | [Link](https://github.com/StatiXOS) |
| Syberia Project                   | [Link](https://github.com/syberia-project)| ArrowOS                           | [Link](https://github.com/ArrowOS) |
| PixelExperience                   | [Link](https://github.com/PixelExperience)| AICP                              | [Link](https://github.com/AICP) |
| ShapeShiftOS                      | [Link](https://github.com/ShapeShiftOS)   | YAAP                              | [Link](https://github.com/yaap) |
| PixelExtended                     | [Link](https://github.com/PixelExtended)  | AospExtended                      | [Link](https://github.com/AospExtended) |
| Nitrogen OS                       | [Link](https://github.com/nitrogen-project)| PixysOS                           | [Link](https://github.com/PixysOS) |
| Havoc-OS                          | [Link](https://github.com/Havoc-OS)       | Xtended                           | [Link](https://github.com/Project-Xtended) |
| ColtOS                            | [Link](https://github.com/Colt-Enigma)    | exTHmUI                           | [Link](https://github.com/exTHmUI) |
| TheParasiteProject                | [Link](https://github.com/TheParasiteProject) |

* And tons of other ROMs not mentioned above

