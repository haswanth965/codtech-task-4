# codtech-task-4

COMPANY: CODTECH IT SOLUTIONS

NAME:HASWANTH REDDY GOGIREDDY

INTERN ID:CT04DF1989

DOMAIN: Embedded Systems

DURATION: 4 WEEKS

MENTOR: Neela Santhosh Kumar

DESCRIPTION : 6SHHFKUHFRJQLWLRQV\VWHPVKDYHDQRWKHUFRQVWUDLQWFRQFHUQLQJWKHVW\OHRIVSHHFKWKH\FDQUHFRJQL]H 7KH\DUHWKUHHVW\OHVRIVSHHFKLVRODWHGFRQQHFWHGDQGFRQWLQXRXV A. Isolated 7KLV VSHHFK UHFRJQLWLRQ V\VWHPFDQMXVW KDQGOHZRUGVWKDW DUH VSRNHQ VHSDUDWHO\7KLVLVWKHPRVWFRPPRQ VSHHFKUHFRJQLWLRQV\VWHPVDYDLODEOHWRGD\7KHXVHUPXVWSDXVHEHWZHHQHDFKZRUGDQGFRPPDQGVSRNHQ7KH VSHHFKUHFRJQLWLRQFLUFXLWLVVHWXSWRLGHQWLI\LVRODWHGZRUGVRIVHFRQGOHQJWKV,VRODWHGZRUGUHFRJQL]HUV XVXDOO\UHTXLUHHDFKXWWHUDQFHWRKDYHTXLHWODFNRIDQDXGLRVLJQDORQ%27+VLGHVRIWKHVDPSOHZLQGRZ,WGRHVQ WPHDQWKDWLWDFFHSWVVLQJOHZRUGVEXWGRHVUHTXLUHDVLQJOHXWWHUDQFHDWDWLPH2IWHQWKHVHV\VWHPVKDYH /LVWHQ1RW/LVWHQVWDWHVZKHUHWKH\UHTXLUHWKHVSHDNHUWRZDLWEHWZHHQXWWHUDQFHVXVXDOO\GRLQJSURFHVVLQJ GXULQJWKHSDXVHV,VRODWHG8WWHUDQFHPLJKWEHDEHWWHUQDPHIRUWKLVFODVV>@ B. Connected &RQQHFWZRUGV\VWHPV RUPRUHFRUUHFWO
FRQQHFWHGXWWHUDQFHV DUHVLPLODUWR,VRODWHGZRUGV EXWDOORZVHSDUDWH XWWHUDQFHVWREH UXQWRJHWKHU ZLWKDPLQLPDOSDXVHEHWZHHQWKHP,WLVDKDOIZD\SRLQWEHWZHHQLVRODWHGZRUG DQGFRQWLQXRXVVSHHFKUHFRJQLWLRQ

SYSTEM DESIGN:

![WhatsApp Image 2025-07-06 at 21 39 01_8f13d4a7](https://github.com/user-attachments/assets/8d4e5fc9-74d0-4ddc-9645-5d3d2499a688)

CODE :

// Callback function for VR engine void VRCallback(int nFlag, int nID, int nScore, int nSG, int nEnergy) { if (nFlag==DSpotterSDKHL::InitSuccess) { //ToDo } else if (nFlag==DSpotterSDKHL::GetResult) { /* When getting an recognition result, the following index and scores are also return to the VRCallback function: nID The result command id nScore nScore is used to evaluate how good or bad the result is. The higher the score, the more similar the voice and the result command are. nSG nSG is the gap between the voice and non-command (Silence/Garbage) models. The higher the score, the less similar the voice and non-command (Silence/Garbage) models are. nEnergy nEnergy is the voice energy level. The higher the score, the louder the voice. */ //ToDo switch(nID) { case 100: Serial.println("The Trigger was heard"); // Add your own code here break; case 10000: Serial.println("The Command -read- was heard"); // Add your own code here break; case 10001: Serial.println("The Command -upload- was heard"); // Add your own code here break; case 10002: Serial.println("The Command -share- was heard"); // Add your own code here break; default: break; }

} else if (nFlag==DSpotterSDKHL::ChangeStage) { switch(nID) { case DSpotterSDKHL::TriggerStage: LED_RGB_Off(); LED_BUILTIN_Off(); break; case DSpotterSDKHL::CommandStage: LED_BUILTIN_On(); break; default: break; } } else if (nFlag==DSpotterSDKHL::GetError) { if (nID == DSpotterSDKHL::LicenseFailed) { //Serial.print("DSpotter license failed! The serial number of your device is "); //Serial.println(DSpotterSDKHL::GetSerialNumber()); } g_oDSpotterSDKHL.Release(); while(1);//hang loop } else if (nFlag == DSpotterSDKHL::LostRecordFrame) { //ToDo } }

![WhatsApp Image 2025-07-06 at 21 39 56_6ad2d44a](https://github.com/user-attachments/assets/7de6212c-196c-46fb-a0a1-4cdcf499d829)

WORKING DEMO :

https://youtu.be/fRSVQ4Fkwjc?si=QLlAV47lBe3NE9zf
