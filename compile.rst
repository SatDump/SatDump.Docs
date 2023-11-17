Compiling SatDump
=================

You might want to compile SatDump yourself. This is recommended to get the latest features on Linux, but can also be used to debug or even make your own modifications such as new pipelines or composites.

Linux
------

Install dependencies on Debian-based systems:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::
sudo apt install git build-essential cmake g++ pkgconf libfftw3-dev libvolk2-dev libpng-dev libluajit-5.1-dev # Core dependencies. If libvolk2-dev is not available, use libvolk1-dev



sudo apt install libnng-dev                                                                                   # If this package is not found, follow build instructions below for NNG

sudo apt install librtlsdr-dev libhackrf-dev libairspy-dev libairspyhf-dev                                    # All libraries required for live processing (optional)
sudo apt install libglfw3-dev                                                                                 # Only if you want to build the GUI Version (optional)
sudo apt install libzstd-dev                                                                                  # Only if you want to build with ZIQ Recording compression 
(optional)
sudo apt install libomp-dev                                                                                   # Shouldn't be required in general, but in case you have errors with OMP
sudo apt install ocl-icd-opencl-dev                                                                           # Optional, but recommended as it drastically increases speed of some operations. Installs OpenCL.
sudo apt install intel-opencl-icd                                                                             # Optional, enables OpenCL for Intel Integrated Graphics

# Install dependencies on Red-Hat-based systems:
sudo dnf install git cmake g++ fftw-devel volk-devel libpng-devel luajit-devel
sudo dnf install nng-devel
sudo dnf install rtl-sdr-devel hackrf-devel airspyone_host-devel
sudo dnf install glfw-devel
sudo dnf install libzstd-devel
(optional)
sudo dnf install libomp-devel
sudo dnf install ocl-icd                                                                                      # Optional, but recommended as it drastically increases speed of some operations. Installs OpenCL.
sudo dnf install intel-opencl                                                                                 # Optional, enables OpenCL for Intel Integrated Graphics

# If libnng-dev is not available, you will have to build it from source
git clone https://github.com/nanomsg/nng.git
cd nng
mkdir build && cd build
cmake -DCMAKE_BUILD_TYPE=Release -DBUILD_SHARED_LIBS=ON -DCMAKE_INSTALL_PREFIX=/usr ..
make -j4
sudo make install
cd ../..
rm -rf nng

# Finally, SatDump
git clone https://github.com/altillimity/satdump.git
cd satdump
mkdir build && cd build
# If you do not want to build the GUI Version, add -DBUILD_GUI=OFF to the command
# If you want to disable some SDRs, you can add -DPLUGIN_HACKRF_SDR_SUPPORT=OFF or similar
cmake -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=/usr ..
make -j`nproc`

# To run without installing
ln -s ../pipelines .        # Symlink pipelines so it can run
ln -s ../resources .        # Symlink resources so it can run
ln -s ../satdump_cfg.json . # Symlink settings so it can run

# To install system-wide
sudo make install

# Run (if you want!)
./satdump-ui
