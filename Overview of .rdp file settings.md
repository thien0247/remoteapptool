[[![DONKZ.NL \| Remote Desktop Plus

[[Remote DesktopPlus]
# Overview of .rdp file settings 
On this page you will find an overview of most of the available .rdp
file settings which can be used with the */o* command line switch.

All settings must be specified using the .rdp file style syntax:

*option:type:value*

Examples:\
*alternate shell:s:notepad.exe*\
*keyboardhook:i:2*

Note: The information in this overview is largely compiled from [this
article at the Microsoft TechNet site](http://technet.microsoft.com/en-us/library/ff393699(WS.10).aspx){target="_blank"
rel="noopener"}.

Use the search box on the left to search and filter keywords.

# 

# Overview of available settings 
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Setting                             Type   Default value     Description and possible values Settable   RDP+ equivalent    5.1   5.2   6.0   6.1   7.0   7.1   8.0   8.1   10.0
                                                                                               from RDC                                                                      
                                                                                               GUI?                                                                          
  ----------------------------------- ------ ----------------- ------------------------------- ---------- ------------------ ----- ----- ----- ----- ----- ----- ----- ----- ------
  administrative session              i      0                 Connect to the administrative   Command    /console, /admin                     X     X     X     X     X     X
                                                               session of the remote           line                                                                          
                                                               computer.\                                                                                                    
                                                               \                                                                                                             
                                                               0 - Do not use the                                                                                            
                                                               administrative session.\                                                                                      
                                                               1 - Connect to the                                                                                            
                                                               administrative session.                                                                                       

  allow desktop composition           i      0                 Determines whether desktop      Yes                                 X     X     X     X     X     X     X     X
                                                               composition (needed for Aero)                                                                                 
                                                               is permitted when you log on to                                                                               
                                                               the remote computer.\                                                                                         
                                                               \                                                                                                             
                                                               0 - Disable desktop composition                                                                               
                                                               in the remote session.\                                                                                       
                                                               1 - Desktop composition is                                                                                    
                                                               permitted.                                                                                                    

  allow font smoothing                i      0                 Determines whether font         Yes                                 X     X     X     X     X     X     X     X
                                                               smoothing may be used in the                                                                                  
                                                               remote session.\                                                                                              
                                                               \                                                                                                             
                                                               0 - Disable font smoothing in                                                                                 
                                                               the remote session.\                                                                                          
                                                               1 - Font smoothing is                                                                                         
                                                               permitted.                                                                                                    

  alternate full address              s                        Specifies an alternate name or  No                                                    X     X     X     X     X
                                                               IP address of the remote                                                                                      
                                                               computer that you want to                                                                                     
                                                               connect to.\                                                                                                  
                                                               \                                                                                                             
                                                               Will be overruled by RDP+.                                                                                    

  alternate shell                     s                        Specifies a program to be       Yes        /start             X     X     X     X     X     X     X     X     X
                                                               started automatically when you                                                                                
                                                               connect to a remote computer.                                                                                 
                                                               The value should be a valid                                                                                   
                                                               path to an executable file.\                                                                                  
                                                               This setting only works when                                                                                  
                                                               connecting to servers.                                                                                        

  audiocapturemode                    i      0                 Determines how sounds captured  Yes                                                   X     X     X     X     X
                                                               (recorded) on the local                                                                                       
                                                               computer are handled when you                                                                                 
                                                               are connected to the remote                                                                                   
                                                               computer.\                                                                                                    
                                                               \                                                                                                             
                                                               0 - Do not capture audio from                                                                                 
                                                               the local computer.\                                                                                          
                                                               1 - Capture audio from the                                                                                    
                                                               local computer and send to the                                                                                
                                                               remote computer.                                                                                              

  audiomode                           i      0                 Determines how sounds on a      Yes        /\[no\]sound       X     X     X     X     X     X     X     X     X
                                                               remote computer are handled                                                                                   
                                                               when you are connected to the                                                                                 
                                                               remote computer.\                                                                                             
                                                               \                                                                                                             
                                                               0 - Play sounds on the local                                                                                  
                                                               computer.\                                                                                                    
                                                               1 - Play sounds on the remote                                                                                 
                                                               computer.\                                                                                                    
                                                               2 - Do not play sounds.                                                                                       

  audioqualitymode                    i      0                 Determines the quality of the   No                                                    X     X     X     X     X
                                                               audio played in the remote                                                                                    
                                                               session.\                                                                                                     
                                                               \                                                                                                             
                                                               0 - Dynamically adjust audio                                                                                  
                                                               quality based on available                                                                                    
                                                               bandwidth.\                                                                                                   
                                                               1 - Always use medium audio                                                                                   
                                                               quality.\                                                                                                     
                                                               2 - Always use uncompressed                                                                                   
                                                               audio quality.                                                                                                

  authentication level                i      2                 Determines what should happen   Yes                                 X     X     X     X     X     X     X     X
                                                               when server authentication                                                                                    
                                                               fails.\                                                                                                       
                                                               \                                                                                                             
                                                               0 - If server authentication                                                                                  
                                                               fails, connect without giving a                                                                               
                                                               warning.\                                                                                                     
                                                               1 - If server authentication                                                                                  
                                                               fails, do not connect.\                                                                                       
                                                               2 - If server authentication                                                                                  
                                                               fails, show a warning and allow                                                                               
                                                               the user to connect or not.\                                                                                  
                                                               3 - Server authentication is                                                                                  
                                                               not required.\                                                                                                
                                                               \                                                                                                             
                                                               This setting will be overruled                                                                                
                                                               by RDP+.                                                                                                      

  autoreconnect max retries           i      20                Determines the maximum number   No                            X     X     X     X     X     X     X     X     X
                                                               of times the client computer                                                                                  
                                                               will try to reconnect to the                                                                                  
                                                               remote computer if the                                                                                        
                                                               connection is dropped.\                                                                                       
                                                               Note: The maximum value Remote                                                                                
                                                               Desktop can handle is 200.                                                                                    

  autoreconnection enabled            i      1                 Determines whether the client   Yes                           X     X     X     X     X     X     X     X     X
                                                               computer will automatically try                                                                               
                                                               to reconnect to the remote                                                                                    
                                                               computer if the connection is                                                                                 
                                                               dropped.\                                                                                                     
                                                               \                                                                                                             
                                                               0 - Do not attempt to                                                                                         
                                                               reconnect.\                                                                                                   
                                                               1 - Attempt to reconnect.                                                                                     

  bandwidthautodetect                 i      1                 Enables the option for          Yes                                                               X     X     X
                                                               automatic detection of the                                                                                    
                                                               network type. Used in                                                                                         
                                                               conjunction with                                                                                              
                                                               **networkautodetect**. Also see                                                                               
                                                               **connection type**.\                                                                                         
                                                               \                                                                                                             
                                                               0 - Do not enable the option                                                                                  
                                                               for automatic network                                                                                         
                                                               detection.\                                                                                                   
                                                               1 - Enable the option for                                                                                     
                                                               automatic network detection.                                                                                  

  bitmapcachepersistenable            i      1                 Determines whether bitmaps are  Yes                                 X     X     X     X     X     X     X     X
                                                               cached on the local computer                                                                                  
                                                               (disk-based cache). Bitmap                                                                                    
                                                               caching can improve the                                                                                       
                                                               performance of your remote                                                                                    
                                                               session.\                                                                                                     
                                                               \                                                                                                             
                                                               0 - Do not cache bitmaps.\                                                                                    
                                                               1 - Cache bitmaps.                                                                                            

  bitmapcachesize                     i      1500              Specifies the size in kilobytes No                            X     X     X     X     X     X     X     X     X
                                                               of the memory-based bitmap                                                                                    
                                                               cache. The maximum value is                                                                                   
                                                               32000.                                                                                                        

  compression                         i      1                 Determines whether the          No                            X     X     X     X     X     X     X     X     X
                                                               connection should use bulk                                                                                    
                                                               compression.\                                                                                                 
                                                               \                                                                                                             
                                                               0 - Do not use bulk                                                                                           
                                                               compression.\                                                                                                 
                                                               1 - Use bulk compression.                                                                                     

  connect to console                  i      0                 Connect to the console session  Command    /console, /admin   X     X     X                                   
                                                               of the remote computer.\        line                                                                          
                                                               \                                                                                                             
                                                               0 - Connect to a normal                                                                                       
                                                               session.\                                                                                                     
                                                               1 - Connect to the console                                                                                    
                                                               screen.                                                                                                       

  connection type                     i      2                 Specifies pre-defined           Yes                                                   X     X     X     X     X
                                                               performance settings for the                                                                                  
                                                               Remote Desktop session.\                                                                                      
                                                               \                                                                                                             
                                                               1 - Modem (56 Kbps).\                                                                                         
                                                               2 - Low-speed broadband (256                                                                                  
                                                               Kbps - 2 Mbps).\                                                                                              
                                                               3 - Satellite (2 Mbps - 16 Mbps                                                                               
                                                               with high latency).\                                                                                          
                                                               4 - High-speed broadband (2                                                                                   
                                                               Mbps - 10 Mbps).\                                                                                             
                                                               5 - WAN (10 Mbps or higher with                                                                               
                                                               high latency).\                                                                                               
                                                               6 - LAN (10 Mbps or higher).\                                                                                 
                                                               7 - Automatic bandwidth                                                                                       
                                                               detection. Requires                                                                                           
                                                               **bandwidthautodetect**.****\                                                                                 
                                                               \                                                                                                             
                                                               By itself, this setting does                                                                                  
                                                               nothing. When selected in the                                                                                 
                                                               RDC GUI, this option changes                                                                                  
                                                               several performance related                                                                                   
                                                               settings (themes, animation,                                                                                  
                                                               font smoothing, etcetera).                                                                                    
                                                               These separate settings always                                                                                
                                                               overrule the connection type                                                                                  
                                                               setting.                                                                                                      

  desktopheight                       i      600               The height (in pixels) of the   Limited    /h                 X     X     X     X     X     X     X     X     X
                                                               remote session desktop.                                                                                       

  desktop size id                     i      0                 Specifies pre-defined           Yes                           X     X     X     X     X     X     X     X     X
                                                               dimensions of the remote                                                                                      
                                                               session desktop.\                                                                                             
                                                               \                                                                                                             
                                                               0 - 640x480.\                                                                                                 
                                                               1 - 800x600.\                                                                                                 
                                                               2 - 1024x768.\                                                                                                
                                                               3 - 1280x1024.\                                                                                               
                                                               4 - 1600x1200.\                                                                                               
                                                               \                                                                                                             
                                                               This setting is ignored when                                                                                  
                                                               either /w and /h, or                                                                                          
                                                               **desktopwidth** and                                                                                          
                                                               **desktopheight** are already                                                                                 
                                                               specified.                                                                                                    

  desktopwidth                        i      800               The width (in pixels) of the    Limited    /w                 X     X     X     X     X     X     X     X     X
                                                               remote session desktop.                                                                                       

  devicestoredirect                   s                        Determines which supported Plug Yes        /\[no\]drives                  X     X     X     X     X     X     X
                                                               and Play devices on the client                                                                                
                                                               computer will be redirected and                                                                               
                                                               available in the remote                                                                                       
                                                               session.\                                                                                                     
                                                               \                                                                                                             
                                                               No value specified - Do not                                                                                   
                                                               redirect any supported Plug and                                                                               
                                                               Play devices.\                                                                                                
                                                               \* - Redirect all supported                                                                                   
                                                               Plug and Play devices,                                                                                        
                                                               including ones that are                                                                                       
                                                               connected later.\                                                                                             
                                                               DynamicDevices - Redirect any                                                                                 
                                                               supported Plug and Play devices                                                                               
                                                               that are connected later.\                                                                                    
                                                               The hardware ID for one or more                                                                               
                                                               Plug and Play devices -                                                                                       
                                                               Redirect the specified                                                                                        
                                                               supported Plug and Play                                                                                       
                                                               device(s).                                                                                                    

  disable ctrl+alt+del                i      1                 Determines whether you have to  No                            X     X     X     X     X     X     X     X     X
                                                               press CTRL+ALT+DELETE before                                                                                  
                                                               entering credentials after you                                                                                
                                                               are connected to the remote                                                                                   
                                                               computer.\                                                                                                    
                                                               \                                                                                                             
                                                               0 - CTRL+ALT+DELETE is required                                                                               
                                                               before logging in.\                                                                                           
                                                               1 - CTRL+ALT+DELETE is not                                                                                    
                                                               required. You can logon                                                                                       
                                                               immediately.\                                                                                                 
                                                               \                                                                                                             
                                                               Note: When disabled, this                                                                                     
                                                               setting will also delay the                                                                                   
                                                               autologin until the user has                                                                                  
                                                               pressed CTRL+ALT+DELETE.                                                                                      

  disable full window drag            i      1                 Determines whether window       Yes                           X     X     X     X     X     X     X     X     X
                                                               content is displayed when you                                                                                 
                                                               drag the window to a new                                                                                      
                                                               location.\                                                                                                    
                                                               \                                                                                                             
                                                               0 - Show the contents of the                                                                                  
                                                               window while dragging.\                                                                                       
                                                               1 - Show an outline of the                                                                                    
                                                               window while dragging.                                                                                        

  disable menu anims                  i      1                 Determines whether menus and    Yes                           X     X     X     X     X     X     X     X     X
                                                               windows can be displayed with                                                                                 
                                                               animation effects in the remote                                                                               
                                                               session.\                                                                                                     
                                                               \                                                                                                             
                                                               0 - Menu and window animation                                                                                 
                                                               is permitted.\                                                                                                
                                                               1 - No menu and window                                                                                        
                                                               animation.                                                                                                    

  disable themes                      i      0                 Determines whether themes are   Yes                           X     X     X     X     X     X     X     X     X
                                                               permitted when you log on to                                                                                  
                                                               the remote computer.\                                                                                         
                                                               \                                                                                                             
                                                               0 - Themes are permitted.\                                                                                    
                                                               1 - Disable theme in the remote                                                                               
                                                               session.                                                                                                      

  disable wallpaper                   i      1                 Determines whether the desktop  Yes        /\[no\]wallpaper   X     X     X     X     X     X     X     X     X
                                                               background is displayed in the                                                                                
                                                               remote session.\                                                                                              
                                                               \                                                                                                             
                                                               0 - Display the wallpaper.\                                                                                   
                                                               1 - Do not show any wallpaper.                                                                                

  disableconnectionsharing            i      0                 Determines whether a new        No                                        X     X     X     X     X     X     X
                                                               Terminal Server session is                                                                                    
                                                               started with every launch of a                                                                                
                                                               RemoteApp to the same computer                                                                                
                                                               and with the same credentials.\                                                                               
                                                               \                                                                                                             
                                                               0 - No new session is started.                                                                                
                                                               The currently active session of                                                                               
                                                               the user is shared.\                                                                                          
                                                               1 - A new login session is                                                                                    
                                                               started for the RemoteApp.                                                                                    

  disableremoteappcapscheck           i      0                 Specifies whether the Remote    No                                                    X     X     X     X     X
                                                               Desktop client should check the                                                                               
                                                               remote computer for RemoteApp                                                                                 
                                                               capabilities.\                                                                                                
                                                               0 - Check the remote computer                                                                                 
                                                               for RemoteApp capabilities                                                                                    
                                                               before logging in.\                                                                                           
                                                               1 - Do not check the remote                                                                                   
                                                               computer for RemoteApp                                                                                        
                                                               capabilities.Note: This setting                                                                               
                                                               must be set to 1 when                                                                                         
                                                               connecting to Windows XP SP3,                                                                                 
                                                               Vista or 7 computers with                                                                                     
                                                               RemoteApps configured on them.                                                                                
                                                               This is the default behavior of                                                                               
                                                               RDP+.                                                                                                         

  displayconnectionbar                i      1                 Determines whether the          Yes                           X     X     X     X     X     X     X     X     X
                                                               connection bar appears when you                                                                               
                                                               are in full screen mode.\                                                                                     
                                                               \                                                                                                             
                                                               0 - Do not show the connection                                                                                
                                                               bar.\                                                                                                         
                                                               1 - Show the connection bar.\                                                                                 
                                                               \                                                                                                             
                                                               Will be overruled by RDP+ when                                                                                
                                                               using the parameter /noclose.                                                                                 

  domain                              s                        Specifies the name of the       Yes        /u, /domain        X     X     X     X     X     X     X     X     X
                                                               domain of the user.\                                                                                          
                                                               \                                                                                                             
                                                               Will be ignored/overruled by                                                                                  
                                                               RDP+.                                                                                                         

  drivestoredirect                    s                        Determines which local disk     Yes        /\[no\]drives                  X     X     X     X     X     X     X
                                                               drives on the client computer                                                                                 
                                                               will be redirected and                                                                                        
                                                               available in the remote                                                                                       
                                                               session.\                                                                                                     
                                                               \                                                                                                             
                                                               No value specified - Do not                                                                                   
                                                               redirect any drives.\                                                                                         
                                                               \* - Redirect all disk drives,                                                                                
                                                               including drives that are                                                                                     
                                                               connected later.\                                                                                             
                                                               DynamicDrives - Redirect any                                                                                  
                                                               drives that are connected                                                                                     
                                                               later.\                                                                                                       
                                                               The drive and labels for one or                                                                               
                                                               more drives - Redirect the                                                                                    
                                                               specified drive(s).                                                                                           

  enablecredsspsupport                i      1                 Determines whether Remote       No                                        X     X     X     X     X     X     X
                                                               Desktop will use CredSSP for                                                                                  
                                                               authentication if it\'s                                                                                       
                                                               available.\                                                                                                   
                                                               \                                                                                                             
                                                               0 - Do not use CredSSP, even if                                                                               
                                                               the operating system supports                                                                                 
                                                               it.\                                                                                                          
                                                               1 - Use CredSSP, if the                                                                                       
                                                               operating system supports it.                                                                                 

  enablesuperpan                      i      0                 Determines whether SuperPan is  No                                                    X     X     X     X     X
                                                               enabled or disabled. SuperPan                                                                                 
                                                               allows the user to navigate a                                                                                 
                                                               remote desktop in full-screen                                                                                 
                                                               mode without scroll bars, when                                                                                
                                                               the dimensions of the remote                                                                                  
                                                               desktop are larger than the                                                                                   
                                                               dimensions of the current                                                                                     
                                                               client window. The user can                                                                                   
                                                               point to the window border, and                                                                               
                                                               the desktop view will scroll                                                                                  
                                                               automatically in that                                                                                         
                                                               direction.\                                                                                                   
                                                               \                                                                                                             
                                                               0 - Do not use SuperPan. The                                                                                  
                                                               remote session window is sized                                                                                
                                                               to the client window size.\                                                                                   
                                                               1 - Enable SuperPan. The remote                                                                               
                                                               session window is sized to the                                                                                
                                                               dimensions specified through /w                                                                               
                                                               and /h, or through                                                                                            
                                                               **desktopwidth** and                                                                                          
                                                               **desktopheight**.                                                                                            

  full address                        s                        Specifies the name or IP        Yes        /v                 X     X     X     X     X     X     X     X     X
                                                               address (and optional port) of                                                                                
                                                               the remote computer that you                                                                                  
                                                               want to connect to.\                                                                                          
                                                               \                                                                                                             
                                                               Will be ignored by RDP+.                                                                                      

  gatewaycredentialssource            i      4                 Specifies the credentials that  Yes                                       X     X     X     X     X     X     X
                                                               should be used to validate the                                                                                
                                                               connection with the RD                                                                                        
                                                               Gateway.\                                                                                                     
                                                               \                                                                                                             
                                                               0 - Ask for password (NTLM).\                                                                                 
                                                               1 - Use smart card.\                                                                                          
                                                               4 - Allow user to select later.                                                                               

  gatewayhostname                     s                        Specifies the hostname of the   Yes         /rdgateway                    X     X     X     X     X     X     X
                                                               RD Gateway.                                                                                                   

  gatewayprofileusagemethod           i      0                 Determines the RD Gateway       Yes                                       X     X     X     X     X     X     X
                                                               authentication method to be                                                                                   
                                                               used.\                                                                                                        
                                                               \                                                                                                             
                                                               0 - Use the default profile                                                                                   
                                                               mode, as specified by the                                                                                     
                                                               administrator.\                                                                                               
                                                               1 - Use explicit settings.                                                                                    

  gatewayusagemethod                  i      4                 Specifies if and how to use a   Yes                                       X     X     X     X     X     X     X
                                                               Remote Desktop Gateway (RD                                                                                    
                                                               Gateway) server.\                                                                                             
                                                               \                                                                                                             
                                                               0 - Do not use an RD Gateway                                                                                  
                                                               server.\                                                                                                      
                                                               1 - Always use an RD Gateway,                                                                                 
                                                               even for local connections.\                                                                                  
                                                               2 - Use the RD Gateway if a                                                                                   
                                                               direct connection cannot be                                                                                   
                                                               made to the remote computer                                                                                   
                                                               (i.e. bypass for local                                                                                        
                                                               addresses).\                                                                                                  
                                                               3 - Use the default RD Gateway                                                                                
                                                               settings.\                                                                                                    
                                                               4 - Do not use an RD Gateway                                                                                  
                                                               server.\                                                                                                      
                                                               \                                                                                                             
                                                               0 and 4 have the same effect,                                                                                 
                                                               but setting the method to 4                                                                                   
                                                               also sets the option for                                                                                      
                                                               bypassing local addresses in                                                                                  
                                                               the Remote Desktop user                                                                                       
                                                               interface.                                                                                                    

  keyboardhook                        i      2                 Determines how Windows key      Yes                           X     X     X     X     X     X     X     X     X
                                                               combinations are applied when                                                                                 
                                                               you are connected to a remote                                                                                 
                                                               computer.\                                                                                                    
                                                               \                                                                                                             
                                                               0 - Windows key combinations                                                                                  
                                                               are applied on the local                                                                                      
                                                               computer.\                                                                                                    
                                                               1 - Windows key combinations                                                                                  
                                                               are applied on the remote                                                                                     
                                                               computer.\                                                                                                    
                                                               2 - Windows key combinations                                                                                  
                                                               are applied in full-screen mode                                                                               
                                                               only.                                                                                                         

  negotiate security layer            i      1                 Determines whether the level of No                                        X     X     X     X     X     X     X
                                                               security is negotiated or not.\                                                                               
                                                               \                                                                                                             
                                                               0 - Security layer negotiation                                                                                
                                                               is not enabled and the session                                                                                
                                                               is started by using Secure                                                                                    
                                                               Sockets Layer (SSL).\                                                                                         
                                                               1 - Security layer negotiation                                                                                
                                                               is enabled and the session is                                                                                 
                                                               started by using x.224                                                                                        
                                                               encryption.                                                                                                   

  networkautodetect                   i      1                 Determines whether to use       Yes                                                               X     X     X
                                                               auomatic network bandwidth                                                                                    
                                                               detection or not. Requires the                                                                                
                                                               option **bandwidthautodetect**                                                                                
                                                               to be set and correlates with                                                                                 
                                                               **connection type** 7.\                                                                                       
                                                               \                                                                                                             
                                                               0 - Use automatic network                                                                                     
                                                               bandwitdh detection.\                                                                                         
                                                               1 - Do not use automatic                                                                                      
                                                               network bandwitdh detection.                                                                                  

  password 51                         b                        The user password in a binary   Yes        /p, /pe, /i        X     X     X     X     X     X     X     X     X
                                                               hash value. Will be overruled                                                                                 
                                                               by RDP+.                                                                                                      

  pinconnectionbar                    i      1                 Determines whether or not the   No                            X     X     X     X     X     X     X     X     X
                                                               connection bar should be pinned                                                                               
                                                               to the top of the remote                                                                                      
                                                               session upon connection when in                                                                               
                                                               full screen mode.\                                                                                            
                                                               \                                                                                                             
                                                               0 - The connection bar should                                                                                 
                                                               not be pinned to the top of the                                                                               
                                                               remote session.\                                                                                              
                                                               1 - The connection bar should                                                                                 
                                                               be pinned to the top of the                                                                                   
                                                               remote session.                                                                                               

  prompt for credentials              i      0                 Determines whether Remote       Yes                                       X     X     X     X     X     X     X
                                                               Desktop Connection will prompt                                                                                
                                                               for credentials when connecting                                                                               
                                                               to a remote computer for which                                                                                
                                                               the credentials have been                                                                                     
                                                               previously saved.\                                                                                            
                                                               \                                                                                                             
                                                               0 - Remote Desktop will use the                                                                               
                                                               saved credentials and will not                                                                                
                                                               prompt for credentials.\                                                                                      
                                                               1 - Remote Desktop will prompt                                                                                
                                                               for credentials.\                                                                                             
                                                               \                                                                                                             
                                                               This setting is ignored by                                                                                    
                                                               RDP+.                                                                                                         

  prompt for credentials on client    i      0                 Determines whether Remote       No                                              X     X     X     X     X     X
                                                               Desktop Connection will prompt                                                                                
                                                               for credentials when connecting                                                                               
                                                               to a server that does not                                                                                     
                                                               support server authentication.\                                                                               
                                                               \                                                                                                             
                                                               0 - Remote Desktop will not                                                                                   
                                                               prompt for credentials.\                                                                                      
                                                               1 - Remote Desktop will prompt                                                                                
                                                               for credentials.\                                                                                             
                                                               \                                                                                                             
                                                               This setting is ignored by                                                                                    
                                                               RDP+.                                                                                                         

  promptcredentialonce                i      1                 When connecting through an RD   Yes                                             X     X     X     X     X     X
                                                               Gateway, determines whether RDC                                                                               
                                                               should use the same credentials                                                                               
                                                               for both the RD Gateway and the                                                                               
                                                               remote computer.\                                                                                             
                                                               \                                                                                                             
                                                               0 - Remote Desktop will not use                                                                               
                                                               the same credentials .\                                                                                       
                                                               1 - Remote Desktop will use the                                                                               
                                                               same credentials for both the                                                                                 
                                                               RD gateway and the remote                                                                                     
                                                               computer.                                                                                                     

  public mode                         i      0                 Determines whether Remote       Command                                               X     X     X     X     X
                                                               Desktop Connection will be      line                                                                          
                                                               started in public mode.\                                                                                      
                                                               \                                                                                                             
                                                               0 - Remote Desktop will not                                                                                   
                                                               start in public mode .\                                                                                       
                                                               1 - Remote Desktop will start                                                                                 
                                                               in public mode and will not                                                                                   
                                                               save any user data                                                                                            
                                                               (credentials, bitmap cache,                                                                                   
                                                               MRU) on the local machine.\                                                                                   
                                                               \                                                                                                             
                                                               This setting is incompatible                                                                                  
                                                               with autologin and some other                                                                                 
                                                               features and therefore ignored                                                                                
                                                               by RDP+.                                                                                                      

  redirectclipboard                   i      1                 Determines whether the          Yes                                       X     X     X     X     X     X     X
                                                               clipboard on the client                                                                                       
                                                               computer will be redirected and                                                                               
                                                               available in the remote session                                                                               
                                                               and vice versa.\                                                                                              
                                                               \                                                                                                             
                                                               0 - Do not redirect the                                                                                       
                                                               clipboard.\                                                                                                   
                                                               1 - Redirect the clipboard.                                                                                   

  redirectcomports                    i      0                 Determines whether the COM      Yes                           X     X     X     X     X     X     X     X     X
                                                               (serial) ports on the client                                                                                  
                                                               computer will be redirected and                                                                               
                                                               available in the remote                                                                                       
                                                               session.\                                                                                                     
                                                               \                                                                                                             
                                                               0 - The COM ports on the local                                                                                
                                                               computer are not available in                                                                                 
                                                               the remote session.\                                                                                          
                                                               1 - The COM ports on the local                                                                                
                                                               computer are available in the                                                                                 
                                                               remote session.                                                                                               

  redirectdirectx                     i      1                 Determines whether DirectX will No                                                    X     X     X     X     X
                                                               be enabled for the remote                                                                                     
                                                               session.\                                                                                                     
                                                               \                                                                                                             
                                                               0 - Do not enable DirectX                                                                                     
                                                               rendering.\                                                                                                   
                                                               1 - Enable DirectX rendering in                                                                               
                                                               the remote session.                                                                                           

  redirectdrives                      i      0                 Determines whether local disk   Yes        /\[no\]drives      X     X                                         
                                                               drives on the client computer                                                                                 
                                                               will be redirected and                                                                                        
                                                               available in the remote                                                                                       
                                                               session.\                                                                                                     
                                                               \                                                                                                             
                                                               0 - The drives on the local                                                                                   
                                                               computer are not available in                                                                                 
                                                               the remote session.\                                                                                          
                                                               1 - The drives on the local                                                                                   
                                                               computer are available in the                                                                                 
                                                               remote session.\                                                                                              
                                                               \                                                                                                             
                                                               Note: This setting is replaced                                                                                
                                                               by **drivestoredirect** from                                                                                  
                                                               RDC 6.0 onward.                                                                                               

  redirectposdevices                  i      0                 Determines whether Microsoft    No                                        X     X     X     X     X     X     X
                                                               Point of Service (POS) for .NET                                                                               
                                                               devices connected to the client                                                                               
                                                               computer will be redirected and                                                                               
                                                               available in the remote                                                                                       
                                                               session.\                                                                                                     
                                                               \                                                                                                             
                                                               0 - The POS devices from the                                                                                  
                                                               local computer are not                                                                                        
                                                               available in the remote                                                                                       
                                                               session.\                                                                                                     
                                                               1 - The POS devices from the                                                                                  
                                                               local computer are available in                                                                               
                                                               the remote session.                                                                                           

  redirectprinters                    i      1                 Determines whether printers     Yes        /\[no\]printers    X     X     X     X     X     X     X     X     X
                                                               configured on the client                                                                                      
                                                               computer will be redirected and                                                                               
                                                               available in the remote                                                                                       
                                                               session.\                                                                                                     
                                                               \                                                                                                             
                                                               0 - The printers on the local                                                                                 
                                                               computer are not available in                                                                                 
                                                               the remote session.\                                                                                          
                                                               1 - The printers on the local                                                                                 
                                                               computer are available in the                                                                                 
                                                               remote session.                                                                                               

  redirectsmartcards                  i      1                 Determines whether smart card   Yes                           X     X     X     X     X     X     X     X     X
                                                               devices on the client computer                                                                                
                                                               will be redirected and                                                                                        
                                                               available in the remote                                                                                       
                                                               session.\                                                                                                     
                                                               \                                                                                                             
                                                               0 - The smart card device on                                                                                  
                                                               the local computer is not                                                                                     
                                                               available in the remote                                                                                       
                                                               session.\                                                                                                     
                                                               1 - The smart card device on                                                                                  
                                                               the local computer is available                                                                               
                                                               in the remote session.                                                                                        

  remoteapplicationcmdline            s                        Optional command line           No                                        X     X     X     X     X     X     X
                                                               parameters for the RemoteApp.                                                                                 

  remoteapplicationfile               s                        Specifies a file to be opened   No         /remotefile                    X     X     X     X     X     X     X
                                                               on the remote computer by the                                                                                 
                                                               RemoteApp.\                                                                                                   
                                                               \                                                                                                             
                                                               Note: For local files to be                                                                                   
                                                               opened, you must also enable                                                                                  
                                                               drive redirection for (at                                                                                     
                                                               least) the source drive.                                                                                      

  remoteapplicationexpandcmdline      i      1                 Determines whether environment  No                                        X     X     X     X     X     X     X
                                                               variables contained in the                                                                                    
                                                               RemoteApp command line                                                                                        
                                                               parameter should be expanded                                                                                  
                                                               locally or remotely.\                                                                                         
                                                               \                                                                                                             
                                                               0 - Environment variables                                                                                     
                                                               should be expanded to the                                                                                     
                                                               values of the local computer.\                                                                                
                                                               1 - Environment variables                                                                                     
                                                               should be expanded on the                                                                                     
                                                               remote computer to the values                                                                                 
                                                               of the remote computer.                                                                                       

  remoteapplicationexpandworkingdir   i      0                 Determines whether environment  No                                        X     X     X     X     X     X     X
                                                               variables contained in the                                                                                    
                                                               RemoteApp working directory                                                                                   
                                                               parameter should be expanded                                                                                  
                                                               locally or remotely.\                                                                                         
                                                               \                                                                                                             
                                                               0 - Environment variables                                                                                     
                                                               should be expanded to the                                                                                     
                                                               values of the local computer.\                                                                                
                                                               1 - Environment variables                                                                                     
                                                               should be expanded on the                                                                                     
                                                               remote computer to the values                                                                                 
                                                               of the remote computer.\                                                                                      
                                                               \                                                                                                             
                                                               Note: The RemoteApp working                                                                                   
                                                               directory is specified through                                                                                
                                                               the **shell working directory**                                                                               
                                                               parameter.                                                                                                    

  remoteapplicationicon               s                        Specifies the file name of an   No                                        X     X     X     X     X     X     X
                                                               icon file to be displayed in                                                                                  
                                                               the Remote Desktop interface                                                                                  
                                                               while starting the RemoteApp.                                                                                 
                                                               By default RDC will show the                                                                                  
                                                               standard Remote Desktop icon.\                                                                                
                                                               \                                                                                                             
                                                               Note: Only .ico files are                                                                                     
                                                               supported.                                                                                                    

  remoteapplicationmode               i      0                 Determines whether a RemoteApp  No         /remoteapp                     X     X     X     X     X     X     X
                                                               shoud be launched when                                                                                        
                                                               connecting to the remote                                                                                      
                                                               computer.\                                                                                                    
                                                               \                                                                                                             
                                                               0 - Use a normal session and do                                                                               
                                                               not start a RemoteApp.\                                                                                       
                                                               1 - Connect and launch a                                                                                      
                                                               RemoteApp.                                                                                                    

  remoteapplicationname               s                        Specifies the name of the       No                                        X     X     X     X     X     X     X
                                                               RemoteApp in the Remote Desktop                                                                               
                                                               interface while starting the                                                                                  
                                                               RemoteApp.                                                                                                    

  remoteapplicationprogram            s                        Specifies the alias or          No         /remoteapp                           X     X     X     X     X     X
                                                               executable name of the                                                                                        
                                                               RemoteApp.                                                                                                    

  screen mode id                      i      2                 Determines whether the remote   Yes        /f\[ullscreen\],   X     X     X     X     X     X     X     X     X
                                                               session window appears full                /fit,\                                                             
                                                               screen when you connect to the             /max, /w, /h                                                       
                                                               remote computer.\                                                                                             
                                                               \                                                                                                             
                                                               1 - The remote session will                                                                                   
                                                               appear in a window.\                                                                                          
                                                               2 - The remote session will                                                                                   
                                                               appear full screen.                                                                                           

  server port                         i      3389              Defines an alternate default    Command    /v                 X     X     X     X     X     X     X     X     X
                                                               port for the Remote Desktop     line                                                                          
                                                               connection.\                                                                                                  
                                                               \                                                                                                             
                                                               Will be overruled by any port                                                                                 
                                                               number appended to the server                                                                                 
                                                               name.                                                                                                         

  session bpp                         i      32                Determines the color depth (in  Yes                           X     X     X     X     X     X     X     X     X
                                                               bits) on the remote computer                                                                                  
                                                               when you connect.\                                                                                            
                                                               \                                                                                                             
                                                               8 - 256 colors (8 bit).\                                                                                      
                                                               15 - High color (15 bit).\                                                                                    
                                                               16 - High color (16 bit).\                                                                                    
                                                               24 - True color (24 bit).\                                                                                    
                                                               32 - Highest quality (32 bit).                                                                                

  shell working directory             s                        The working directory on the    Yes                           X     X     X     X     X     X     X     X     X
                                                               remote computer to be used if                                                                                 
                                                               an alternate shell is                                                                                         
                                                               specified.                                                                                                    

  smart sizing                        i      0                 Determines whether the client   No                            X     X     X     X     X     X     X     X     X
                                                               computer should scale the                                                                                     
                                                               content on the remote computer                                                                                
                                                               to fit the window size of the                                                                                 
                                                               client computer when the window                                                                               
                                                               is resized.\                                                                                                  
                                                               \                                                                                                             
                                                               0 - The client window display                                                                                 
                                                               will not be scaled when                                                                                       
                                                               resized.\                                                                                                     
                                                               1 - The client window display                                                                                 
                                                               will be scaled when resized.                                                                                  

  span monitors                       i      0                 Determines whether the remote   Yes        /span                          X     X     X     X     X     X     X
                                                               session window will be spanned                                                                                
                                                               across multiple monitors when                                                                                 
                                                               you connect to the remote                                                                                     
                                                               computer.\                                                                                                    
                                                               \                                                                                                             
                                                               0 - Monitor spanning is not                                                                                   
                                                               enabled.\                                                                                                     
                                                               1 - Monitor spanning is                                                                                       
                                                               enabled.\                                                                                                     
                                                               \                                                                                                             
                                                               Note: When using Remote Desktop                                                                               
                                                               Connection 7 (Windows 7/2008),                                                                                
                                                               the **use multimon** setting is                                                                               
                                                               recommended.                                                                                                  

  superpanaccelerationfactor          i      1                 Specifies the number of pixels  No                                                    X     X     X     X     X
                                                               that the screen view scrolls in                                                                               
                                                               a given direction for every                                                                                   
                                                               pixel of mouse movement by the                                                                                
                                                               client when in SuperPan mode                                                                                  

  usbdevicestoredirect                s                        Determines which supported      Yes                                                         X     X     X     X
                                                               RemoteFX USB devices on the                                                                                   
                                                               client computer will be                                                                                       
                                                               redirected and available in the                                                                               
                                                               remote session when you connect                                                                               
                                                               to a remote session that                                                                                      
                                                               supports RemoteFX USB                                                                                         
                                                               redirection.\                                                                                                 
                                                               \                                                                                                             
                                                               No value specified - Do not                                                                                   
                                                               redirect any supported RemoteFX                                                                               
                                                               USB devices.\                                                                                                 
                                                               \* - Redirect all supported                                                                                   
                                                               RemoteFX USB devices for                                                                                      
                                                               redirection that are not                                                                                      
                                                               redirected by high-level                                                                                      
                                                               redirection mechanisms.\                                                                                      
                                                               {Device Setup Class GUID} -                                                                                   
                                                               Redirect all supported RemoteFX                                                                               
                                                               USB devices that are members of                                                                               
                                                               the specified device setup                                                                                    
                                                               class.\                                                                                                       
                                                               USB\\InstanceID - Redirect the                                                                                
                                                               supported RemoteFX USB device                                                                                 
                                                               specified by the given instance                                                                               
                                                               ID.\                                                                                                          
                                                               -USB\\InstanceID - Do not                                                                                     
                                                               redirect the supported RemoteFX                                                                               
                                                               USB device specified by the                                                                                   
                                                               given instance ID, even if the                                                                                
                                                               device is in a device setup                                                                                   
                                                               class that is redirected..                                                                                    

  use multimon                        i      0                 Determines whether the session  Yes        /multimon                                  X     X     X     X     X
                                                               should use true multiple                                                                                      
                                                               monitor support when connecting                                                                               
                                                               to the remote computer.\                                                                                      
                                                               \                                                                                                             
                                                               0 - Do not enable multiple                                                                                    
                                                               monitor support.\                                                                                             
                                                               1 - Enable multiple monitor                                                                                   
                                                               support.                                                                                                      

  username                            s                        Specifies the name of the user  Yes        /u                 X     X     X     X     X     X     X     X     X
                                                               account that will be used to                                                                                  
                                                               log on to the remote computer.\                                                                               
                                                               \                                                                                                             
                                                               Will be ignored by RDP+.                                                                                      

  videoplaybackmode                   i      1                 Determines whether RDC will use No                                                    X     X     X     X     X
                                                               RDP efficient multimedia                                                                                      
                                                               streaming for video playback.\                                                                                
                                                               \                                                                                                             
                                                               0 - Do not use RDP efficient                                                                                  
                                                               multimedia streaming for video                                                                                
                                                               playback.\                                                                                                    
                                                               1 - Use RDP efficient                                                                                         
                                                               multimedia streaming for video                                                                                
                                                               playback when possible.                                                                                       

  winposstr                           s      0,3,0,0,800,600   Specifies the position and      No         /f\[ullscreen\],   X     X     X     X     X     X     X     X     X
                                                               dimensions of the session                  /fit,\                                                             
                                                               window on the client computer.\            /max, /w, /h, /pos                                                 
                                                               \                                                                                                             
                                                               Will be overruled by RDP+.                                                                                    
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:::
:::
:::

## RDC versions 
:::
5.1 : Included with Windows XP.\
5.2 : Included with Windows 2003.\
6.0 : Included with Windows Vista. Available for Windows XP SP2 and
Windows 2003 SP1/SP2.\
6.1 : Included with Windows 2008, Windows Vista SP1 and Windows XP SP3.
Available for Windows XP SP2.\
7.0 : Included with Windows 2008 R2 and Windows 7. Available for Windows
XP SP3 and Windows Vista SP1/SP2.7.1 : Included with Windows 7 SP1 and
Windows 2008 R2 SP1.\
8.0 : Included with Windows 8 and Windows 2012. Available for Windows 7
SP1 and Windows 2008 R2 SP1.\
8.1 : Included with Windows 8.1 and Windows 2012 R2. Available for Windows 7 SP1 and Windows 2008 R2 SP1.\
10.0: Included with Windows 10.
