# ansible-role-repo

Enable, disable, create or amend repositories for yum compatible systems.

    repositories:
    - name: example
    description: example description
    baseurl: "https://example.com/rhel7"
    #baseurl: "file:///mnt/iso"
    gpgcheck: no
    enabled: yes
    state: present

Note the `baseurl` example for `file://`. This allows you to mount an ISO to a directory and use this as a yum repo. Useful for disconnected installs. Only one `baseurl` should be specified per repo.
