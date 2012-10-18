
include $(top_srcdir)/Common.am


my_files = openstackguestagent.te openstackguestagent.fc

dist_noinst_SCRIPTS = ${my_files}

if USE_SELINUX
all:
	$(MAKE) -f /usr/share/selinux/devel/Makefile $(top_srcdir)/selinux/openstackguestagent.pp
endif


if USE_SELINUX
install-exec-local:
	semodule -i $(top_srcdir)/selinux/openstackguestagent.pp
endif

