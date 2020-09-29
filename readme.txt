android manifest:

<?xml version="1.0" encoding="utf-8"?>
<manifest ... >
    <application android:networkSecurityConfig="@xml/network_security_config"
                    ... >
        ...
    </application>
</manifest>


https://ibotpeaches.github.io/Apktool/ (used for extracting and changing).

Windows:
Download Windows wrapper script (Right click, Save Link As apktool.bat)
Download apktool-2 (find newest here)
Rename downloaded jar to apktool.jar
Move both files (apktool.jar & apktool.bat) to your Windows directory (Usually C://Windows)
If you do not have access to C://Windows, you may place the two files anywhere then add that directory to your Environment Variables System PATH variable.
Try running apktool via command prompt



https://raw.githubusercontent.com/iBotPeaches/Apktool/master/scripts/windows/apktool.bat

https://bitbucket.org/iBotPeaches/apktool/downloads/


olase below code in @xml/network_security_config
<network-security-config>  
      <base-config>  
            <trust-anchors>  
                <!-- Trust preinstalled CAs -->  
                <certificates src="system" />  
                <!-- Additionally trust user added CAs -->  
                <certificates src="user" />  
           </trust-anchors>  
      </base-config>  
 </network-security-config>
 
 
 
 
 apktool d sample.apk
 
 apktool b sample -o samplenew.apk



after apk build sign the apk with apk signer
