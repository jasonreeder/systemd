test_data_files = '''
        a.service
        basic.target
        b.service
        c.service
        daughter.service
        d.service
        end.service
        e.service
        f.service
        grandchild.service
        g.service
        hello-after-sleep.target
        hello.service
        h.service
        parent-deep.slice
        parent.slice
        sched_idle_bad.service
        sched_idle_ok.service
        sched_rr_bad.service
        sched_rr_change.service
        sched_rr_ok.service
        shutdown.target
        sleep.service
        sockets.target
        son.service
        sysinit.target
        testsuite.target
        timers.target
        unstoppable.service
        test-path/paths.target
        test-path/basic.target
        test-path/sysinit.target
        test-path/path-changed.service
        test-path/path-directorynotempty.service
        test-path/path-existsglob.service
        test-path/path-exists.service
        test-path/path-makedirectory.service
        test-path/path-modified.service
        test-path/path-mycustomunit.service
        test-path/path-service.service
        test-path/path-changed.path
        test-path/path-directorynotempty.path
        test-path/path-existsglob.path
        test-path/path-exists.path
        test-path/path-makedirectory.path
        test-path/path-modified.path
        test-path/path-unit.path
        test-execute/exec-environment-empty.service
        test-execute/exec-environment-multiple.service
        test-execute/exec-environment.service
        test-execute/exec-passenvironment-absent.service
        test-execute/exec-passenvironment-empty.service
        test-execute/exec-passenvironment-repeated.service
        test-execute/exec-passenvironment.service
        test-execute/exec-group.service
        test-execute/exec-group-nfsnobody.service
        test-execute/exec-supplementarygroups.service
        test-execute/exec-supplementarygroups-single-group.service
        test-execute/exec-supplementarygroups-single-group-user.service
        test-execute/exec-supplementarygroups-multiple-groups-default-group-user.service
        test-execute/exec-supplementarygroups-multiple-groups-withgid.service
        test-execute/exec-supplementarygroups-multiple-groups-withuid.service
        test-execute/exec-dynamicuser-fixeduser.service
        test-execute/exec-dynamicuser-fixeduser-one-supplementarygroup.service
        test-execute/exec-dynamicuser-supplementarygroups.service
        test-execute/exec-ignoresigpipe-no.service
        test-execute/exec-ignoresigpipe-yes.service
        test-execute/exec-personality-x86-64.service
        test-execute/exec-personality-x86.service
        test-execute/exec-personality-s390.service
        test-execute/exec-personality-ppc64.service
        test-execute/exec-personality-ppc64le.service
        test-execute/exec-personality-aarch64.service
        test-execute/exec-privatedevices-no.service
        test-execute/exec-privatedevices-yes.service
        test-execute/exec-privatedevices-no-capability-mknod.service
        test-execute/exec-privatedevices-yes-capability-mknod.service
        test-execute/exec-protectkernelmodules-no-capabilities.service
        test-execute/exec-protectkernelmodules-yes-capabilities.service
        test-execute/exec-protectkernelmodules-yes-mount-propagation.service
        test-execute/exec-privatetmp-no.service
        test-execute/exec-privatetmp-yes.service
        test-execute/exec-readonlypaths.service
        test-execute/exec-readonlypaths-mount-propagation.service
        test-execute/exec-readwritepaths-mount-propagation.service
        test-execute/exec-inaccessiblepaths-mount-propagation.service
        test-execute/exec-spec-interpolation.service
        test-execute/exec-systemcallerrornumber.service
        test-execute/exec-systemcallfilter-failing2.service
        test-execute/exec-systemcallfilter-failing.service
        test-execute/exec-systemcallfilter-not-failing2.service
        test-execute/exec-systemcallfilter-not-failing.service
        test-execute/exec-systemcallfilter-system-user.service
        test-execute/exec-systemcallfilter-system-user-nfsnobody.service
        test-execute/exec-user.service
        test-execute/exec-user-nfsnobody.service
        test-execute/exec-workingdirectory.service
        test-execute/exec-umask-0177.service
        test-execute/exec-umask-default.service
        test-execute/exec-privatenetwork-yes.service
        test-execute/exec-environmentfile.service
        test-execute/exec-oomscoreadjust-positive.service
        test-execute/exec-oomscoreadjust-negative.service
        test-execute/exec-ioschedulingclass-best-effort.service
        test-execute/exec-ioschedulingclass-idle.service
        test-execute/exec-ioschedulingclass-none.service
        test-execute/exec-ioschedulingclass-realtime.service
        test-execute/exec-capabilityboundingset-invert.service
        test-execute/exec-capabilityboundingset-merge.service
        test-execute/exec-capabilityboundingset-reset.service
        test-execute/exec-capabilityboundingset-simple.service
        test-execute/exec-capabilityambientset.service
        test-execute/exec-capabilityambientset-nfsnobody.service
        test-execute/exec-capabilityambientset-merge.service
        test-execute/exec-capabilityambientset-merge-nfsnobody.service
        test-execute/exec-runtimedirectory.service
        test-execute/exec-runtimedirectory-mode.service
        test-execute/exec-runtimedirectory-owner.service
        test-execute/exec-runtimedirectory-owner-nfsnobody.service
        test-execute/exec-restrict-namespaces-no.service
        test-execute/exec-restrict-namespaces-yes.service
        test-execute/exec-restrict-namespaces-mnt.service
        test-execute/exec-restrict-namespaces-mnt-blacklist.service
        test-execute/exec-read-only-path-succeed.service
        test-execute/exec-privatedevices-yes-capability-sys-rawio.service
        test-execute/exec-privatedevices-no-capability-sys-rawio.service
        bus-policy/hello.conf
        bus-policy/methods.conf
        bus-policy/ownerships.conf
        bus-policy/signals.conf
        bus-policy/check-own-rules.conf
        bus-policy/many-rules.conf
        bus-policy/test.conf
        hwdb/10-bad.hwdb
        journal-data/journal-1.txt
        journal-data/journal-2.txt
'''.split()

if conf.get('ENABLE_RESOLVED', false)
        test_data_files += '''
                test-resolve/_openpgpkey.fedoraproject.org.pkts
                test-resolve/fedoraproject.org.pkts
                test-resolve/gandi.net.pkts
                test-resolve/google.com.pkts
                test-resolve/root.pkts
                test-resolve/sw1a1aa-sw1a2aa-sw1a2ab-sw1a2ac.find.me.uk.pkts
                test-resolve/teamits.com.pkts
                test-resolve/zbyszek@fedoraproject.org.pkts
                test-resolve/_443._tcp.fedoraproject.org.pkts
                test-resolve/kyhwana.org.pkts
                test-resolve/fake-caa.pkts
        '''.split()
endif

if install_tests
        foreach file : test_data_files
                subdir = file.split('/')[0]
                if subdir == file
                        subdir = ''
                endif

                install_data(file,
                             install_dir : testsdir + '/testdata/' + subdir)
        endforeach
endif
