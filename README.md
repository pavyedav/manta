# manta
MANTA - Microsimulation Analysis for Network Traffic Assignment
## Dependencies

 - Boost 1.59
 - OpenCV (used versions: 3.2.0 in Ubuntu)
 - CUDA (used versions: 9.0 in Ubuntu)
 - g++ (used versions: 6.4.0 in Ubuntu)
 - Qt5 (used versions: 5.9.5 in Ubuntu)
 - qmake (used verions: 3.1 in Ubuntu)

## Installation & Compilation

Once the necessaries dependencies are installed you can use the following lines to make sure the
correct verions of each one are used:
```bash
export PATH=PATH=/usr/local/cuda-9.0/bin:$PATH
export LIBRARY_PATH=/usr/local/cuda-9.0/lib64:$LIBRARY_PATH 
export LD_LIBRARY_PATH=/usr/local/cuda-9.0/lib64:$LD_LIBRARY_PATH 
```

In Linux you can also add those `export`statements lines at the end of your user's `~/.bashrc` to
avoid re-entering them on each session.

Clone in your home directory with:
```bash
git clone git@github.com:udst/manta.git ~/manta && cd ~/manta
```

If necessary checkout a different branch than master (`maintenance` for instance):
```bash
git checkout edge_speeds_over_time
```

Create `Makefile` and compile with:
```bash
sudo qmake LivingCity/LivingCity.pro && sudo make -j
```

## Running

If you wish to edit configuration, modify `command_line_options.ini`.

Run with:
```bash
cd LivingCity
./LivingCity
```
