# uppm-formula-repository-linux-x86_64
the offical formula repository for [uppm](https://github.com/leleliu008/uppm)

## what's formula
formula is a YAML format file which is used to config a [uppm](https://github.com/leleliu008/uppm) package infomation and describe how to install it.

|KEY|required?|overview|
|-|-|-|
|`summary`|required|the summary of this package.|
|`webpage`|required|the home webpage of this package.|
|`version`|required|the version of this package.|
|`license`|optional|the license of this package.|
|`bin-url`|required|the prebuild binary archive file download url of this package.<br>must end with one of `.zip` `.tar.xz` `.tar.gz` `.tar.lz` `.tar.bz2` `.tgz` `.txz`|
|`bin-sha`|required|the `sha256sum` of the prebuild binary archive file.|
|`dep-pkg`|optional|space-separated packages that will be used when installing or runtime.|
|`install`|optional|bash shell code to be run when installing.|

## the variable can be used in prepare and install block
|variable|overview|
|-|-|
|`NATIVE_OS_TYPE`|current machine os type.|
|`NATIVE_OS_NAME`|current machine os name.|
|`NATIVE_OS_VERS`|current machine os version.|
|`NATIVE_OS_ARCH`|current machine os arch.|
|||
|`UPPM_VERSION`|the version of `uppm`.|
|`UPPM_HOME`|the home directory of `uppm`.|
|||
|`UPPM_PKG_INSTALL_DIR`|the directory where the current package will be installed to.|
