# Tools

## qemu

### configure
- `./configure --disable-kvm --disable-werror --target-list="i386-softmmu x86_64-softmmu" --python=python2`
    - Need to specify the path for **python2**

### make
- `commands-posix.c:633: undefined reference to 'major'` `commands-posix.c:634: undefined reference to 'minor'`
    - Add `<sys/sysmacros.h>` to commands-posix.c
    - http://patchwork.ozlabs.org/patch/709415/
- `virtio-9p.c:796: undefined reference to 'minor'` `virtio-9p.c:796: undefined reference to 'major'` `virtio-9p.c:2803: undefined reference to 'makedev'` `virtio-9p.c:2124: undefined reference to 'makedev'`
    - Add `<sys/sysmacros.h>` to virtio-9p.c