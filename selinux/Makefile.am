
include $(top_srcdir)/Common.am


my_files = openstackguestagent.te openstackguestagent.fc

dist_noinst_SCRIPTS = ${my_files}

if USE_SELINUX
all: openstackguestagent.pp

openstackguestagent.pp:
	$(MAKE) -f /usr/share/selinux/devel/Makefile openstackguestagent.pp
endif


if USE_SELINUX
install-exec-local:
	semodule -i $(abs_builddir)/selinux/openstackguestagent.pp
endif

