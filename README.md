# CMake Template

Template I use for starting out with C++ projects.

## Usage

Create `build` directory:

```bash
mkdir build
cd build
```

Use cmake to create build files:

```bash
cmake -G Ninja -DCMAKE_BUILD_TYPE=DEBUG ../
```

Create symlink to indexes for clangd.

```bash
cd .. # Move to base of project
ln -s build/compile_commands.json
```

Compile:

```bash
cd build
ninja
```
