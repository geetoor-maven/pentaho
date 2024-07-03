# SETUP OPERATING SYSTEM

Before we really use the pentaho from virtual machine engine to host windows, We have to setup a few things both at the host windows and in the virtual meachine.

1. Setup network virtual machine to bridged adapter

    open your virtual machine and click setting -> in the left sidebar, go to network and setting adapter 1 to Bridged Adapter.
![STP-1](img/setup/stp1.png)


### SETUP ON THE HOST MACHINE

1. Allow SQL Server through windows firewall
- Open ` Windows Firawall with Advanced Security `
![STP-2](img/setup/stp2.png)
- Create a new inbound rule to allow TCP port 1433 ( default SQL Server port )
![STP-3](img/setup/stp3.png)

2. Enable TCP/IP 
- Open SQL Server Configuration Manger
- Go to SQL Server Network Configuration -> Protocols for [YourInstance]
- Enable TCP/IP
![STP-4](img/setup/stp4.png)

3. Verify SQL Server Configuration Using SMSS
- Open SQL Server Management Studio (SSMS)
- Ensure that the server is configured to allow remote connections
    - Rigth-Click on the server in Object Explorer and Select Properties
    - Go to the Connections page and ensure Allow Remote connections to this server is Checked

![STP-5](img/setup/stp5.png)

### SETUP ON THE UBUNTU VIRTUAL MACHINE

1. Check UFW Status 
- Check the status of UFW
![STP-6](img/setup/stp6.png)

- if UFW is active, allow outgoing traffic to the SQL server port 1433
![STP-7](img/setup/stp7.png)

- if you need to allow incoming trafic from specific IP ranges, you can use :
```sh
sudo ufw allow from <your_windows_host_ip> to any port 1433
```

### Additional Network Check

1. Check your ip address ubuntu vm
![STP-8](img/setup/stp8.png)

2. Check your ip address host windows
![STP-9](img/setup/stp9.png)

3. Ping ip address host windows on ubuntu vm with command :
```sh
ping <your_windows_host_ip>
```

4. Ping ip address ubuntu vm on host windows with command :
```sh
ping <your_ubuntu_vm_ip>
```

5. Telnet to SQL Server Port, Check if you can connect to the SQL Server Port :
```sh
telnet <your_windows_host_ip> 1433
```
![STP-10](img/setup/stp10.png)

6. if Telnet is not installed, you can install it using :
```sh
sudo apt-get install telnet
```

Now you should have communicated each other 2 machine ( host windows and ubuntu virtual machine ) and can be used for the SQL server database connection to windows host


#### <a href='https://github.com/geetoor-maven/pentaho/blob/master/8_RUNNING_SH_FILE.md'>Next Step</a>