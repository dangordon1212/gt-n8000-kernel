#
# Makefile for Linux CIFS VFS client 
#
obj-$(CONFIG_CIFS) += cifs.o

CFLAGS_cifssmb.o += -Wno-error=array-bounds

cifs-y := cifsfs.o cifssmb.o cifs_debug.o connect.o dir.o file.o inode.o \
	  link.o misc.o netmisc.o smbencrypt.o transport.o asn1.o \
	  cifs_unicode.o nterr.o xattr.o cifsencrypt.o \
	  readdir.o ioctl.o sess.o export.o

cifs-$(CONFIG_CIFS_ACL) += cifsacl.o

cifs-$(CONFIG_CIFS_UPCALL) += cifs_spnego.o

cifs-$(CONFIG_CIFS_DFS_UPCALL) += dns_resolve.o cifs_dfs_ref.o

cifs-$(CONFIG_CIFS_FSCACHE) += fscache.o cache.o
