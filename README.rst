ressiboot Simple UEFI boot manager
----------------------------------

ressiboot is a fork of goofiboot - which is now dead upstream.

This fork is now being used for RESS Linux (and anyone else if they're interested)
because we need the full features of gummiboot, outside of the context of
systemd.

It's been stated on several occassions that systemd-boot is "not a direct
successor", and "systemd-boot does not support some of the features gummiboot
supported". As such, this fork becomes a separate and independent bootloader.

License
=======

ressiboot is available under the same license as goofiboot, the GNU
Lesser General Public License 2.1 (LGPL-2.1)

About
=====

ressiboot executes EFI images. The default entry is selected by a configured
pattern (glob) or an on-screen menu.

ressiboot operates on the EFI System Partition (ESP) only. Configuration
file fragments, kernels, initrds, other EFI images need to reside on the
ESP. Linux kernels must be built with CONFIG_EFI_STUB to be able to be
directly executed as an EFI image.

ressiboot reads simple and entirely generic configuration files; one file
per boot entry to select from.

Pressing Space (or most other) keys during bootup will show an on-screen
menu with all configured entries to select from. Pressing enter on the
selected entry loads and starts the EFI image.

If no timeout is configured and no key pressed during bootup, the default
entry is booted right away.
