# Cloudflare Workerd Wrapper

My own wrapper of Cloudflare's workerd. Only for macOS Catalina.

## Why?

* I run macOS Catalina.
* Building workerd from source is not desirable at the time.
* I have a pre-built workerd binary installed using npm, but it's not working due to older libc++.
* I have LLVM 15 (along with libc++) installed, but somehow it is not recognized by the pre-built workerd.

## What does it do?

* Set `DYLD_LIBRARY_PATH` to the LLVM libc++ path.
* Run workerd and pass all arguments to it.