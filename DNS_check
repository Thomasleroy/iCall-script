app-service none
    definition {
        set pn "/Common/my_pool"
           set total 0
           set usable 0
           foreach obj [tmsh::get_status /ltm pool $pn detail] {
           foreach member [tmsh::get_field_value $obj members] {
           incr total
           if { [tmsh::get_field_value $member status.availability-state] == "available" && \
                [tmsh::get_field_value $member status.enabled-state] == "enabled" } {
                incr usable
     }
   }                                                                                                                                                                                        }
           if { $usable==0} {
                 tmsh::modify /ltm virtual-address 10.10.10.10 route-advertisement disabled
                 tmsh::modify /ltm virtual-address 10.10.10.10 route-advertisement disabled
                        } else {
                 tmsh::modify /ltm virtual-address 10.10.10.10 route-advertisement enabled
                 tmsh::modify /ltm virtual-address 10.10.10.10 route-advertisement enabled
                  }
    }
    description none
    events none
}
