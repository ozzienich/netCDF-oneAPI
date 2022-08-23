# intel oneAPI
```shell
module load icc/latest	
export NCDIR=/opt/netcdf/oneapi
export CPPFLAGS=-I${NCDIR}/include
export LDFLAGS=-L${NCDIR}/lib

export LIB_NETCDF=/opt/netcdf/oneapi/lib/
export LD_LIBRARY_PATH=$LIB_NETCDF:$LD_LIBRARY_PATH
```

## build/compile icc:
```shell
./configure --prefix=/opt/netcdf/oneapi  CC=icc --disable-hdf5
```

## build/compile ifort
```shell
./configure --prefix=/opt/netcdf   CC=icc   FC=ifort  F77=ifort   LDFLAGS=-L/opt/netcdf/lib:/opt/intel/oneapi/compiler/latest/linux/lib  LIBS=-l/opt/netcdf/lib:/opt/intel/oneapi/compiler/latest/linux/lib FCFLAGS="-g"  CPPFLAGS="-I/opt/netcdf/include -fpic"  CFLAGS="-I/opt/netcdf/include -fpic" 

./configure --prefix=/opt/netcdf    FC=ifort  F77=ifort   LDFLAGS=-L/opt/netcdf/lib:/opt/intel/oneapi/compiler/latest/linux/lib  LIBS=-l/opt/netcdf/lib:/opt/intel/oneapi/compiler/latest/linux/lib FCFLAGS="-g"    
```
