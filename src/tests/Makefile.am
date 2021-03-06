if ENABLE_TESTS

LDADD = ../lxc/liblxc.la

lxc_test_api_reboot_SOURCES = api_reboot.c
lxc_test_apparmor_SOURCES = aa.c
lxc_test_attach_SOURCES = attach.c
lxc_test_basic_SOURCES = basic.c
lxc_test_cgpath_SOURCES = cgpath.c
lxc_test_clonetest_SOURCES = clonetest.c
lxc_test_concurrent_SOURCES = concurrent.c
lxc_test_config_jump_table_SOURCES = config_jump_table.c lxctest.h
lxc_test_console_SOURCES = console.c
lxc_test_console_log_SOURCES = console_log.c lxctest.h
lxc_test_containertests_SOURCES = containertests.c
lxc_test_createtest_SOURCES = createtest.c
lxc_test_criu_check_feature_SOURCES = criu_check_feature.c lxctest.h
lxc_test_cve_2019_5736_SOURCES =  cve-2019-5736.c lxctest.h
lxc_test_destroytest_SOURCES = destroytest.c
lxc_test_device_add_remove_SOURCES = device_add_remove.c
lxc_test_getkeys_SOURCES = getkeys.c
lxc_test_get_item_SOURCES = get_item.c
lxc_test_list_SOURCES = list.c
lxc_test_locktests_SOURCES = locktests.c
lxc_test_lxcpath_SOURCES = lxcpath.c
lxc_test_may_control_SOURCES = may_control.c
lxc_test_mount_injection_SOURCES = mount_injection.c lxctest.h
lxc_test_parse_config_file_SOURCES = parse_config_file.c \
				     lxctest.h
lxc_test_raw_clone_SOURCES = lxc_raw_clone.c \
			     lxctest.h \
			     ../lxc/namespace.c ../lxc/namespace.h \
			     ../lxc/raw_syscalls.c ../lxc/raw_syscalls.h
			     ../lxc/utils.c ../lxc/utils.h
lxc_test_reboot_SOURCES = reboot.c
lxc_test_saveconfig_SOURCES = saveconfig.c
lxc_test_share_ns_SOURCES = share_ns.c lxctest.h
lxc_test_shortlived_SOURCES = shortlived.c
lxc_test_shutdowntest_SOURCES = shutdowntest.c
lxc_test_snapshot_SOURCES = snapshot.c
lxc_test_startone_SOURCES = startone.c
lxc_test_state_server_SOURCES = state_server.c lxctest.h
lxc_test_utils_SOURCES = lxc-test-utils.c lxctest.h

AM_CFLAGS=-DLXCROOTFSMOUNT=\"$(LXCROOTFSMOUNT)\" \
	  -DLXCPATH=\"$(LXCPATH)\" \
	  -DLXC_GLOBAL_CONF=\"$(LXC_GLOBAL_CONF)\" \
	  -DLXCINITDIR=\"$(LXCINITDIR)\" \
	  -DLXC_DEFAULT_CONFIG=\"$(LXC_DEFAULT_CONFIG)\" \
	  -DRUNTIME_PATH=\"$(RUNTIME_PATH)\" \
	  -I $(top_srcdir)/src \
	  -I $(top_srcdir)/src/lxc \
	  -I $(top_srcdir)/src/lxc/cgroups \
	  -I $(top_srcdir)/src/lxc/tools \
	  -pthread

if ENABLE_APPARMOR
AM_CFLAGS += -DHAVE_APPARMOR
endif

if ENABLE_SECCOMP
AM_CFLAGS += -DHAVE_SECCOMP \
	     $(SECCOMP_CFLAGS)
endif

if ENABLE_SELINUX
AM_CFLAGS += -DHAVE_SELINUX
endif

bin_PROGRAMS = lxc-test-api-reboot \
	       lxc-test-apparmor \
	       lxc-test-attach \
	       lxc-test-basic \
	       lxc-test-cgpath \
	       lxc-test-clonetest \
	       lxc-test-concurrent \
	       lxc-test-config-jump-table \
	       lxc-test-console \
	       lxc-test-console-log \
	       lxc-test-containertests \
	       lxc-test-createtest \
	       lxc-test-criu-check-feature \
	       lxc-test-cve-2019-5736 \
	       lxc-test-destroytest \
	       lxc-test-device-add-remove \
	       lxc-test-getkeys \
	       lxc-test-get_item \
	       lxc-test-list \
	       lxc-test-locktests \
	       lxc-test-lxcpath \
	       lxc-test-may-control \
	       lxc-test-mount-injection \
	       lxc-test-parse-config-file \
	       lxc-test-raw-clone \
	       lxc-test-reboot \
	       lxc-test-saveconfig \
	       lxc-test-share-ns \
	       lxc-test-shortlived \
	       lxc-test-shutdowntest \
	       lxc-test-snapshot \
	       lxc-test-startone \
	       lxc-test-state-server \
	       lxc-test-utils

bin_SCRIPTS =
if ENABLE_TOOLS
bin_SCRIPTS += lxc-test-automount \
	       lxc-test-autostart \
	       lxc-test-cloneconfig \
	       lxc-test-createconfig \
	       lxc-test-no-new-privs \
	       lxc-test-rootfs

if DISTRO_UBUNTU
bin_SCRIPTS += lxc-test-lxc-attach \
	       lxc-test-apparmor-mount \
	       lxc-test-apparmor-generated \
	       lxc-test-checkpoint-restore \
	       lxc-test-snapdeps \
	       lxc-test-symlink \
	       lxc-test-unpriv \
	       lxc-test-usernic
endif
endif

endif

EXTRA_DIST = basic.c \
	     cgpath.c \
	     clonetest.c \
	     concurrent.c \
	     config_jump_table.c \
	     console.c \
	     console_log.c \
	     containertests.c \
	     createtest.c \
	     criu_check_feature.c \
	     cve-2019-5736.c \
	     destroytest.c \
	     device_add_remove.c \
	     get_item.c \
	     getkeys.c \
	     list.c \
	     locktests.c \
	     lxcpath.c \
	     lxc_raw_clone.c \
	     lxc-test-lxc-attach \
	     lxc-test-automount \
	     lxc-test-rootfs \
	     lxc-test-autostart \
	     lxc-test-apparmor-mount \
	     lxc-test-apparmor-generated \
	     lxc-test-checkpoint-restore \
	     lxc-test-cloneconfig \
	     lxc-test-createconfig \
	     lxc-test-no-new-privs \
	     lxc-test-snapdeps \
	     lxc-test-symlink \
	     lxc-test-unpriv \
	     lxc-test-utils.c \
	     may_control.c \
	     mount_injection.c \
	     parse_config_file.c \
	     saveconfig.c \
	     shortlived.c \
	     shutdowntest.c \
	     snapshot.c \
	     startone.c \
	     state_server.c \
	     share_ns.c

clean-local:
	rm -f lxc-test-utils-*
	rm -f lxc-parse-config-file-*
