## Walkthrough: Configuring WPA2 and TKIP on a Wireless Access Point

### Lab Objective:

Learn how to configure WPA2 and TKIP on a wireless access point.

### Lab Purpose:

WPA2 has replaced WPA as the preferred security protocol for wireless connections. WPA2 can work with other protocols to offer enhanced security. TKIP-RC4 stream cipher is used with a 128-bit per packet key, meaning each packet has a unique key.

### Lab Tool:

Packet Tracer

### Lab Topology:

- A laptop is connected to a wireless access point (AP) by a wireless connection.
- The access point is connected to a router using an Ethernet cable.

### Task 1: Connect Router to Access Point and Add Laptop

1.  **Add a Router, Access Point, and Laptop to the Workspace:**
    - Use a crossover cable to connect the router to the access point.
    - Insert a wireless card into the laptop’s side slot.
    - Label the wireless device as `AP-PT` in Packet Tracer.

### Task 2: Configure IP Address on the Router

1.  **Access the Router CLI:**
    
    - Click on the router, go to the CLI tab.
2.  **Enter Configuration Mode:**
    
    plaintext
    
    Copy code
    
    `Router>en Router#conf t`
    
3.  **Configure the Ethernet Interface:**
    
    plaintext
    
    Copy code
    
    `Router(config)#int f0/0 Router(config-if)#ip add 192.168.1.1 255.255.255.0 Router(config-if)#no shut`
    

### Task 3: Configure Security and Wireless Settings on the Access Point

1.  **Access the Access Point Config Tab:**
    
    - Click on the access point, go to the Config tab.
2.  **Set Wireless Settings:**
    
    - **SSID:** `calbright`
    - **Pass Phrase:** `123456789`
    - **Security:** `WPA2-PSK`
    - **Encryption:** `TKIP`

### Task 4: Configure Wireless Card Settings on the Laptop

1.  **Access the Laptop Config Tab:**
    
    - Click on the laptop, go to the Config tab.
2.  **Set Wireless Configuration:**
    
    - **SSID:** `calbright`
    - **Pass Phrase:** `123456789`
    - **Security:** `WPA2-PSK`
    - **Encryption:** `TKIP`
3.  **Set IPv4 Address:**
    
    - **IP Address:** `192.168.1.2`
    - **Subnet Mask:** `255.255.255.0`

### Task 5: Add Default Gateway on the Laptop

1.  **Access the Laptop Config Tab:**
    
    - Click on the laptop, go to the Config tab.
2.  **Set Default Gateway:**
    
    - **Default Gateway:** `192.168.1.1`

### Task 6: Verify Wireless Connection

1.  **Check the Canvas:**
    - Ensure the laptop is wirelessly connected to the access point.
    - Verify the access point is connected to the router.

### Task 7: Ping from Laptop to Router

1.  **Ping Command:**
    - Open the laptop’s Command Prompt.
        
    - Run the following command:
        
        plaintext
        
        Copy code
        
        `ping 192.168.1.1`
