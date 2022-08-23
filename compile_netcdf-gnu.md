export NCDIR=/opt/netcdf/gnu
export CPPFLAGS=-I${NCDIR}/include
export LDFLAGS=-L${NCDIR}/lib

export LIB_NETCDF=/opt/netcdf/gnu/lib/
export LD_LIBRARY_PATH=$LIB_NETCDF:$LD_LIBRARY_PATH


#build/compile C:
./configure --prefix=/opt/netcdf/gnu  CC=gcc --disable-hdf5


#build/compile gfortran
./configure LDFLAGS=-L/opt/netcdf/gnu/lib --prefix=/opt/netcdf/gnu
