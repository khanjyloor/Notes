## Nagios core adding a host definition

 conf.d -> Configuration directory

 As root, create a new configuration file "name.cfg".

 ```
  define host {
    host_name store.tup.local
    alias store
    address 192.168.0.8
    max_check_attemps 3
    check_period 24x7
    check_command check-host-alive
    contacts root
    notification_interval 60
    notification_period 24x7
  }
 ```

 To check the configuration file in verbose mode:
    ```
      nagios3 -v /etc/nagios3/nagios.cfg
    ```
 Restart the nagios service as root:
    ```
      service nagios3 restart
    ```
