# happy-meraki-client-vpn
PowerShell scripts for setting up Meraki Client VPN on Windows 10

Windows 10 doesn't like to play nice with the Meraki client VPN, especially when following Meraki's own setup instructions.

These default 

These scripts attempt to:
  1. Pre-emptively fix issues with NAT-Traversal. Commonly pops up when clients use cellphone hotspots.
  2. Simplify creating a split tunnel connection.
  3. Prevent Windows from authenticating to network resources with the VPN credential.
  4. Create a rasphone desktop shortcut. It seems to behave better, and users find it easier to enter credentials into.
  5. Create the connection for all users. Especially useful for shared laptops or users prone to Windows user profile corruption.
  
  <b>AddMerakiVPN_Prompts.ps1:</b> Handy when you administer multiple Meraki client VPNs, such as at an MSP's help desk.    
    It will prompt for:
    1. VPN connection name.
        A new name will create a new connection. An existing name prompts for permission to delete and recreate.
    2. VPN concentrator address
    3. Pre-shared key
    4. Routes if you pick split tunnel.
  
  <b>AddMerakiVPN.ps1:</b> Edit the variables in the script yourself and then run. Good for large deployments. 
