# grub-unlzma
GRUB utilities don't provide any way to unwrap a bootable image produced by the *grub-mkimage* tool, thus there is no easy way to extract a core image from a bootable image of GRUB. A core image is often compressed and written after a platform-specific code and a decompressor, so you have to figure out the correct offset of a core image within a bootable image of GRUB first.

## grub-guess
The *grub-guess* script tries to guess the offset of a core image within a bootable image of GRUB. On success, an uncompressed core image is written to stdout and the offset is written to stderr.
