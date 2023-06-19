## Etherchannel: 

- Etherchannel là một kỹ thuật nhóm hai hay nhiều  đường kết nối để truyền tải dữ liệu vật lý thành một đường ảo duy nhất ( Logic ) nhằm mục đích
tăng tốc độ chuyền tải dữ liệu  và khả năng dự phòng  cho hệ thống ( Reduncancy ).

- Công nghệ Etherchannel có thể gộp từ 2 đến 8 link vật lý thành một link logical.

- Các Port kết nối Etherchannel giữa 2 Switch phải tương đồng với nhau về :
  - Cấu hình ( Configuration )
  - Tốc độ ( Speed )
  - Băng thông ( Bendwidth )
  - Duplex ( Full Duplex )
  - Native Vlan và các Vlans
  - Switchport Mode ( Trunking or Access )

## Configuration:

Demo-NguyenNN(config)#int port-channel 1

Demo-NguyenNN(config-if-range)#int ran g0/1-2

Demo-NguyenNN(config-if-range)#channel-group 1 mode active

Demo-NguyenNN(config-if-range)#do show int eth
----
GigabitEthernet0/1:
Port state    = Down Not-in-Bndl
Channel group = 1           Mode = Active          Gcchange = -
Port-channel  = null        GC   =   -             Pseudo port-channel = Po1
Port index    = 0           Load = 0x00            Protocol =   LACP

Flags:  S - Device is sending Slow LACPDUs   F - Device is sending fast LACPDUs.
        A - Device is in active mode.        P - Device is in passive mode.

Local information:
                            LACP port     Admin     Oper    Port        Port
Port      Flags   State     Priority      Key       Key     Number      State
Gi0/1     SA      down      32768         0x1       0x0     0x11A       0x45

Age of the port in the current state: 0d:00h:01m:57s

----
GigabitEthernet0/2:
Port state    = Down Not-in-Bndl
Channel group = 1           Mode = Active          Gcchange = -
Port-channel  = null        GC   =   -             Pseudo port-channel = Po1
Port index    = 0           Load = 0x00            Protocol =   LACP

Flags:  S - Device is sending Slow LACPDUs   F - Device is sending fast LACPDUs.
        A - Device is in active mode.        P - Device is in passive mode.

Local information:
                            LACP port     Admin     Oper    Port        Port
Port      Flags   State     Priority      Key       Key     Number      State
Gi0/2     SA      down      32768         0x1       0x0     0x11B       0x45

Age of the port in the current state: 0d:00h:00m:41s

----
Port-channel1:Port-channel1   (Primary aggregator)

Age of the Port-channel   = 0d:00h:03m:24s
Logical slot/port   = 2/1          Number of ports = 0
HotStandBy port = null
Port state          = Port-channel Ag-Not-Inuse
Protocol            =   LACP
Port security       = Disabled



