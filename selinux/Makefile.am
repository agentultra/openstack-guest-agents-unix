
include $(top_srcdir)/Common.am

openstackguestagent.pp:
	@if [ -n "${SELINUX_ENABLED}" ]; then $(MAKE) -f /usr/share/selinux/devel/Makefile \
	$(top_srcdir)/selinux/openstackguestagent.pp; fi

install-exec-local:
	@if [ -f $(top_srcdir)/selinux/openstackguestagent.pp ]; then semodule -i $(top_srcdir)/selinux/openstackguestagent.pp; fi

