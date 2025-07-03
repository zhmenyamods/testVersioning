---
title: subpage2
deprecated: false
hidden: false
metadata:
  robots: index
---
Risk labels are used to detect and mark the abnormal risk environment of devices. They are generally used in combination with device IDs and can prevent fraud risks. Device fingerprinting can detect many malicious risk environments, including but not limited to ROOT, Jailbreak, emulator, multi-opening, tamper detection, VPN usage, etc. Please fully understand and utilize the risk labels according to the actual business situation.

Some risk labels are applicable to all terminal devices, while some are only applicable to browsers, mini-programs, or mobile devices.

# **Current Device Time Abnormal**

<span style={{backgroundColor: '#53B160', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Android</span> <span style={{backgroundColor: '#9E9E9E', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>iOS</span> <span style={{backgroundColor: '#FF7F00', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Web</span> <span style={{backgroundColor: '#00BCD4', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Mini-programs</span>

**Label Description**: There is a significant deviation between the current device time and the requested server time, for example, more than 24 hours.

**Scenario**: Users manually modifying the device system time will cause a large time difference.

```
{
"device_risk_score":6,
"device_risk_label": [
"abnormal_time"
]
}
```

# **Device Is a Simulator**

<span style={{backgroundColor: '#53B160', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Android</span> <span style={{backgroundColor: '#9E9E9E', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>iOS</span> <span style={{backgroundColor: '#1E90FF', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Harmony</span> <span style={{backgroundColor: '#FF7F00', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Web</span> <span style={{backgroundColor: '#00BCD4', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Mini-programs</span>

**Label Description**: The scenario of an application running in an emulator. It refers to using software on a personal computer (PC) to simulate the operating environment similar to other devices or operating systems, rather than running in an environment of a real device.

**Scenario**: Mobile game enthusiasts use emulators to keep games running in the background, nurture accounts, and seek improper benefits. Keeping games running in the background aims to obtain in-game resources, experience, or rewards. Nurturing accounts means obtaining more benefits by running multiple secondary accounts. Seeking improper benefits refers to taking advantage of the loopholes in the rules of games or applications to gain improper profits. These behaviors undermine the fairness of games and the normal operation order of applications.

```
{
"device_risk_score":9,
"device_risk_label": [
"emulator"
]
}
```

# **Incognito Mode**

<span style={{backgroundColor: '#FF7F00', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Web</span>

**Label Description**: The incognito mode of the browser, also known as the private browsing mode, is a privacy - protection feature built into the browser. In this mode, the browser does not locally store user browsing history, cookies, and other information. It is an independent session window. When the window is closed, the relevant data will be automatically cleared, achieving the purpose of protecting user privacy.

**Scenario**: This label is more commonly marked in scenarios where users claim coupons during promotional activities. In this mode, users may try to create new identities, log in with multiple accounts to claim coupons, and take advantage of merchants in this way.

```
{
"device_risk_score":4,
"device_risk_label": [
"incognito_mode"
]
}
```

# **Virtual Browser**

<span style={{backgroundColor: '#FF7F00', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Web</span> <span style={{backgroundColor: '#00BCD4', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Mini-programs</span>

**Label Description**: A headless browser is a browser without a Graphical User Interface (GUI). It runs in the background and is operated and controlled through command lines or programming interfaces. For example, the Selenium library in Python can be used to easily operate a headless browser, sending commands such as opening web pages, clicking buttons, and filling out forms to achieve automated web page operations.

**Scenario**: Automated operations are used in automated testing, web page scraping, and data collection and analysis. It is an automated tool rather than something used by ordinary users.

```
{
"device_risk_score":6,
"device_risk_label": [
"headless_mode"
]
}
```

# **Useragent Abnormal**

<span style={{backgroundColor: '#FF7F00', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Web</span> <span style={{backgroundColor: '#00BCD4', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Mini-programs</span>

**Label Description**: The User Agent identification does not meet the specifications. The User Agent has been manually modified, or there is a problem with the browser itself, resulting in the UA string being tampered with or generated incorrectly.

**Scenario**: During network transmission, the UA is hijacked and tampered with, stealing and forging data information. Malicious attacks pose risks such as account theft or property fraud. Commonly, there are also cases where users try to forge a new identity by modifying the UA through plugins.

```
{
"device_risk_score":6,
"device_risk_label": [
"abnormal_useragent"
]
}
```

# **Debugger Is Detected**

<span style={{backgroundColor: '#53B160', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Android</span> <span style={{backgroundColor: '#9E9E9E', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>iOS</span> <span style={{backgroundColor: '#FF7F00', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Web</span> <span style={{backgroundColor: '#00BCD4', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Mini-programs（WeChat）</span>

**Label Description**: This label determines whether an application is in a debugged state by detecting API functions related to process management and debugging.

**Scenario**: Developers use the debuggers of development tools to identify errors in programs during the development process. In a normal user environment, debugging rarely occurs, except when the application itself is fortified and occupies the debugging port. Besides this, only malicious attackers use debuggers to analyze software, crack encryption algorithms, and tamper with the program's operation logic to achieve cheating.

```
{
"device_risk_score":12,
"device_risk_label": [
"debugger_detected"
]
}
```

# **Hook Tool Detected**

<span style={{backgroundColor: '#53B160', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Android</span> <span style={{backgroundColor: '#9E9E9E', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>iOS</span> <span style={{backgroundColor: '#FF7F00', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Web</span>

**Label Description**: Detect whether system functions have been hook. Hook mainly involves replacing, injecting into, or monitoring the functions of the target process. When running, the original function is not executed.

**Scenario**: Malicious actors use Hook technology to tamper with device information, undermining the integrity and accuracy of device data and generating new identities for devices.

```
{
"device_risk_score":9,
"device_risk_label": [
"hook_tool_detected"
]
}
```

# **Tampering With Device Parameters**

<span style={{backgroundColor: '#53B160', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Android</span> <span style={{backgroundColor: '#9E9E9E', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>iOS</span> <span style={{backgroundColor: '#FF7F00', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Web</span> <span style={{backgroundColor: '#00BCD4', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Mini-programs</span>

**Label Description**: Detect the tampering of device information through software or technical means. Commonly targeted information includes the device brand, model, system version, MAC address, etc.

**Scenario**: Use tools or software that can tamper with device parameters to disguise as other device information and generate new identities based on the modified device information.

```
{
"device_risk_score":9,
"device_risk_label": [
"device_info_tampered"
]
}
```

# **Group Control**

<span style={{backgroundColor: '#53B160', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Android</span> <span style={{backgroundColor: '#9E9E9E', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>iOS</span>

**Label Description**: Detect the function of sending commands to multiple devices simultaneously through specific software and hardware systems, enabling the batch control of one or more devices.

**Scenario**: In marketing and promotion activities, this is used to release product information on multiple media platforms simultaneously, conduct batch likes, comments, and reposts to achieve profitability. It can also be used for batch account nurturing and taking advantage of promotional offers (such as "wool - pulling" activities) and other improper behaviors.

```
{
"device_risk_score":12,
"device_risk_label": [
"group_control"
]
}
```

# **Without SIM Card Inserted**

<span style={{backgroundColor: '#53B160', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Android</span> <span style={{backgroundColor: '#9E9E9E', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>iOS</span> <span style={{backgroundColor: '#1E90FF', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Harmony</span>

**Label Description**: The device does not have a SIM card inserted, so it does not support voice calls, sending text messages, and cannot use the mobile data network.

**Scenario**: In the environment of group control operation, a large number of devices without SIM cards that perform the same behavior operations simultaneously will be detected as abnormal behaviors.

```
{
"device_risk_score":4,
"device_risk_label": [
"no_sim"
]
}
```

# **Device Parameter Abnormal**

<span style={{backgroundColor: '#9E9E9E', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>iOS</span> <span style={{backgroundColor: '#FF7F00', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Web</span> <span style={{backgroundColor: '#00BCD4', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Mini-programs</span>

**Label Description**: Hijack the collected data, intercept the request message packets, forge the collected data, and fabricate false message information to make it seem as if it comes from a legitimate data source.

**Scenario**: In the flash sale scenario, by capturing packets of the interface, bypassing the rendering of the activity page, and implementing interface-based requests, the purpose of quickly and effectively grabbing tickets can be achieved.

```
{
"device_risk_score":12,
"device_risk_label": [
"abnormal_device_attr"
]
}
```

# **Script Tampering**

<span style={{backgroundColor: '#FF7F00', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Web</span>

**Label Description**: The SDK source file has been maliciously modified.

**Scenario**: Fraudsters try to bypass device risk detection by modifying the script code to weaken the fingerprinting ability.

```
{
"device_risk_score":12,
"device_risk_label": [
"script_tempered"
]
}
```

# **Device as a Virtual Machine**

<span style={{backgroundColor: '#FF7F00', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Web</span>

**Label Description**: Check whether the browser is running on a virtual machine.

**Scenario**: Risk fraudsters can create a large number of virtual environments through virtual machines, achieve environmental isolation, disguise as real devices, increase the difficulty of risk detection, and thus carry out risk fraud.

```
{
"device_risk_score":12,
"device_risk_label": [
"virtual_machine"
]
}
```

# **Local Debugging**

<span style={{backgroundColor: '#FF7F00', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Web</span>

**Label Description**: Detect that the currently browsed page is a service launched locally rather than accessed from an online service.

**Scenario**: During the development and testing phase, developers will access the developer page in the form of a file without the need to deploy the service. Fraudsters will use technical means to capture the activity web page, conduct local page debugging, and look for vulnerabilities by analyzing the code logic to attack the activity page.

```
{
"device_risk_score":6,
"device_risk_label": [
"local_debug"
]
}
```

# **Android Debug Bridge**

<span style={{backgroundColor: '#53B160', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Android</span>

**Label Description**: Detect whether the Android device is in the ADB debugging state under the developer mode.

**Scenario**: In the developer environment, the device is debugged. Applications can be installed and uninstalled, and device information can be viewed through commands. One manifestation mode of group control is wired control. Through ADB connection, batch operation of device behaviors can be realized, which is a type of fraud risk.

```
{
"device_risk_score":4,
"device_risk_label": [
"adb_link"
]
}
```

# **Secondary Packaging**

<span style={{backgroundColor: '#53B160', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Android</span> <span style={{backgroundColor: '#9E9E9E', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>iOS</span>

**Label Description**: Detect the process of repackaging an existing APK file.

**Scenario**: Developers decompile the APK to obtain the application's resource files and code content, and then add some new functions or modify certain features on this basis. Fraudsters will replace functional modules, steal user privacy, cause traffic loss, and earn illegal advertising revenue, etc.

```
{
"device_risk_score":9,
"device_risk_label": [
"repackaged"
]
}
```

# **Using a Proxy**

<span style={{backgroundColor: '#53B160', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Android</span> <span style={{backgroundColor: '#9E9E9E', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>iOS</span> <span style={{backgroundColor: '#00BCD4', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Mini-programs(WeChat)</span>

**Label Description**: Detect whether the current device is using a proxy.

**Scenario**: Through network proxy tools, HTTP protocol requests can be intercepted and analyzed, and there will be risks of data information leakage and tampering. Common proxy tools include Charles, Fiddler, etc.

```
{
"device_risk_score":8,
"device_risk_label": [
"proxy_detected"
]
}
```

# **ROOT**

<span style={{backgroundColor: '#53B160', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Android</span>

**Label Description**: Detect the ROOT status of the device to determine whether the application is secure.

**Scenario**: Obtain the highest device privileges, install malicious software and dangerous frameworks, tamper with device information, forge new device identities, and achieve the purpose of risk fraud.

```
{
"device_risk_score":9,
"device_risk_label": [
"root"
]
}
```

# **Jailbreak Devices**

**Terminal Types**: iOS

**Label Description**: Detect the jailbreak status of the device to determine whether the application is secure.

**Scenario**: Jailbreak devices have a low security coefficient. Fraudsters can tamper with device information through jailbreak devices, control the device to trade in a risky environment, and induce users to suffer financial losses.

```
{
"device_risk_score":9,
"device_risk_label": [
"jail_break"
]
}
```

# **Using a VPN**

<span style={{backgroundColor: '#53B160', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Android</span> <span style={{backgroundColor: '#9E9E9E', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>iOS</span> <span style={{backgroundColor: '#FF7F00', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Web</span>

**Label Description**: Detect whether the device is using a VPN service.

**Scenario**: It can break through geographical restrictions to obtain external information and can also hide the user's real IP address at the same time. Some marketing activities have geographical restrictions, and business risk control can be carried out based on this risk.

```
{
"device_risk_score":4,
"device_risk_label": [
"vpn_detected"
]
}
```

# **Replay Attack**

<span style={{backgroundColor: '#53B160', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Android</span> <span style={{backgroundColor: '#9E9E9E', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>iOS</span> <span style={{backgroundColor: '#FF7F00', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Web</span> <span style={{backgroundColor: '#00BCD4', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Mini-programs</span>(Scores may vary for different terminals, the examples are for reference only)

**Label Description**: Detect that the same piece of collected data is reported repeatedly more than twice.

**Scenario**: Fraudsters use network technology to monitor and hijack network transmission packets, resend the packets repeatedly, and try to share the same device information to bypass the detection of the risk control system.

```
{
"device_risk_score":9,
"device_risk_label": [
"replay_attacks"
]
}
```

# **Cookie** **Tampering**

<span style={{backgroundColor: '#53B160', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Android</span> <span style={{backgroundColor: '#9E9E9E', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>iOS</span> <span style={{backgroundColor: '#1E90FF', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Harmony</span> <span style={{backgroundColor: '#FF7F00', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Web</span> <span style={{backgroundColor: '#00BCD4', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Mini-programs</span> (Scores may vary for different terminals, the examples are for reference only)

**Label Description**: Detect that the fingerprint cookie has been tampered with.

**Scenario**: After hijacking through system value storage functions, the cookie is modified and forged, affecting the stability of the device identity. Fraudsters try to generate a new identity to bypass risk detection, and engage in activities such as inflating traffic and points.

```
{
"device_risk_score":9,
"device_risk_label": [
"cookie_tempered"
]
}
```

# **Web** **Crawler**

<span style={{backgroundColor: '#FF7F00', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Web</span>

**Label Description**: Detect programs or scripts that automatically and massively capture web page information.

**Scenario**: Automated behavior is not that of a normal real user. This type of attack usually occurs in scenarios such as inflating traffic, grabbing tickets, and flash sales, and there is a risk of fraud.

```
{
"device_risk_score":8,
"device_risk_label": [
"crawler"
]
}
```

# **Malicious Extension Plugins**

<span style={{backgroundColor: '#FF7F00', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Web</span>

**Label Description**: Detect the installation of malicious extension programs in the browser.

**Scenario**: Malicious extension programs in the browser environment can modify and forge device information, affecting the stability of device fingerprints. In some cases, parameter abnormalities will also coincide with the tampering of device parameters. Common plugins include Canvas Fingerprint Defender, AudioContext Fingerprint Defender, etc.

```
{
"device_risk_score":8,
"device_risk_label": [
"malicious_crx"
]
}
```

# **Debugger Tools**

<span style={{backgroundColor: '#FF7F00', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Web</span>

**Label Description**: Detect that a debugging tool is installed in the browser.

**Scenario**: Developers use H5 debugging tools to detect code. Online pages will not provide users with debugging tools. If it exists, there is a risk of fraud.

```
{
"device_risk_score":6,
"device_risk_label": [
"debug_tool"
]
}
```

# **App Multi Opening**

<span style={{backgroundColor: '#53B160', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Android</span>

**Label Description**: Check whether the current app is a cloned application spawned by app multi-instance software (there are two or more of the same application on one device).

**Scenario**: Through multi-instance software, two or more identical applications can be installed on the same device. Different accounts are logged in respectively, and the activity pages are switched to share and grab coupons to complete fraudulent acts.

```
{
"device_risk_score":6,
"device_risk_label": [
"app_multiple_running"
]
}
```

# **System Multi Opening**

<span style={{backgroundColor: '#53B160', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Android</span>

**Label Description**: Check whether the current app is a cloned application spawned by the system's built-in multi-instance function.

**Scenario**: Through the system's multi-instance function, two or more identical applications can be installed on the same device. Different accounts are logged in respectively, and the activity pages are switched to share and grab coupons to complete fraudulent acts.

```
{
"device_risk_score":4,
"device_risk_label": [
"sys_multiple_running"
]
}
```

# **Virtual Positioning**

**Terminal Types**: Android, iOS, Mini-programs (WeChat)

**Label Description**: Check whether the device's geographical location is camouflaged and mark it with a risk label. Location permission is required.

**Scenario**:In store activities, coupons are issued with restricted usage areas. Fraudsters tamper with the location information to grab the coupons and seek profits.

```
{
"device_risk_score":8,
"device_risk_label": [
"gps_fake"
]
}
```

# **Suspected Risk ROM**

<span style={{backgroundColor: '#53B160', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Android</span>

**Label Description**: The ROM is not the original factory-installed one of the device.

**Scenario**: In order to modify the device, the black market industry flashes a specific Rom package, modifies the device information, creates different new identities, and conducts network fraud and malicious brushing of orders.

```
{
"device_risk_score":13,
"device_risk_label": [
"risk_rom"
]
}
```

# **Camera Fake**

<span style={{backgroundColor: '#53B160', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Android</span> <span style={{backgroundColor: '#9E9E9E', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>iOS</span>

**Label Description**: Detect the photo streams and video streams obtained by tampering with the camera through cheating tools.

**Scenario**: Bypass facial recognition in credit lending detection to prevent illegal fraud.

```
{
"device_risk_score":8,
"device_risk_label": [
"camera_fake"
]
}
```

# **Suspected Reset**

<span style={{backgroundColor: '#53B160', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Android</span> <span style={{backgroundColor: '#9E9E9E', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>iOS</span>

**Label Description**: Check whether the device has been restored to factory settings and returned to its initial state.

**Scenario**: Reset device data to generate a new device identity.

```
{
"device_risk_score":4,
"device_risk_label": [
"suspected_reset"
]
}
```

# **Short Uptime**

<span style={{backgroundColor: '#53B160', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Android</span> <span style={{backgroundColor: '#9E9E9E', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>iOS</span> <span style={{backgroundColor: '#1E90FF', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Harmony</span>

**Label Description**: The time interval from device boot to the collection of device information is relatively short, less than half an hour.

**Scenario**: Emulators or cloud phones will frequently restart the service.

```
{
"device_risk_score":4,
"device_risk_label": [
"short_uptime"
]
}
```

# **Screen Sharing**

<span style={{backgroundColor: '#53B160', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Android</span> <span style={{backgroundColor: '#9E9E9E', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>iOS</span> <span style={{backgroundColor: '#1E90FF', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Harmony</span> <span style={{backgroundColor: '#00BCD4', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Mini-programs(WeChat)</span>

**Label Description**: Check whether the device has initiated a screen sharing service.

**Scenario**: Fraudsters fabricate false information through means such as telephone calls, the Internet and text messages to deceive people out of their property.

```
{
"device_risk_score":6,
"device_risk_label": [
"screen_sharing"
]
}
```

# **Cloud Phone**

<span style={{backgroundColor: '#53B160', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>Android</span> <span style={{backgroundColor: '#9E9E9E', color: 'white', padding: '5px 10px', borderRadius: '5px'}}>iOS</span>

**Label Description**: The application runs on an ARM server and uses virtualization technology to build an Android application platform in the cloud.

**Scenario**: By purchasing multiple cloud phones, fraudsters can control multiple cloud devices in batches to carry out fraudulent acts such as nurturing accounts, hanging up games, and sharing activities to attract new users.

```
{
"device_risk_score":9,
"device_risk_label": [
"cloud_phone"
]
}
```