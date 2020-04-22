check the LD_LIBRARY_PATH path value. If this is not having the path of location where the .so files are located then add it using export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:<new path>

use ldd command to check what all files it is linked to.