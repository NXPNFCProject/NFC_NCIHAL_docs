----------------------------------------------------------------------
MW Configurations to be used during Execution of CTS Tests
----------------------------------------------------------------------
Following are the configurations used for CTS testing.

I.  Default MW configurations are as below:
    DEFAULT_AID_ROUTE=0x00 (HOST)
    DEFAULT_DESFIRE_ROUTE=0x02 (UICC)
    DEFAULT_MIFARE_CLT_ROUTE=0x02 (UICC)
    DEFAULT_FELICA_CLT_ROUTE=0x01 (UICC)
		
	Following is the list of tests cases performed with default MW configurations
	1. Protocol Parameters
	2. Single Payment
	3. Two payment services
	4. Change default payment services
	5. Single non-payment
	6. Two non-payment services
	7. Two conflicting non-payment services
	8. HCE throughput test
	9. 50 successful taps test
	10.Foreground override payment services
	11.Foreground override non-payment services
	12.Dynamic Payment AIDS
        13.Payment prefix AIDs
	14.Payment prefix AIDs 2
	15.Other prefix AIDs
	16.Conflicting non-payment prefix AIDs
	17.Off-host service -> if UICC Presence UICC AID will be registered in routing table and transaction will happen to off host else Tx will happen to on-host
	18.On and off-host services
	19.Large number of AIDs
    

II. For following test case to check the overflow handling in MW, set DEFAULT_AID_ROUTE to 0x02(UICC) or 0x01(eSE) in config
        1.Large number of AIDs   	

	 
-----------------------------------
Execution of VTS Tests
-----------------------------------
 For running the VTS test cases using the Default MW configurations.
 Following are the steps used to run VTS
  
	Steps to Install the VtsHalNfcV1_0TargetTest binary ,
	adb root
	adb remount
	adb push VtsHalNfcV1_0TargetTest   /system/bin/
	adb reboot

	Steps to execute the VtsHalNfcV1_0TargetTest binary
	1.	Switch-off the NFC Service
	2.	cd  /system/bin/    
	4.	chmod 777 VtsHalNfcV1_0TargetTest
	5.	./VtsHalNfcV1_0TargetTest

---------------------------------------------------------------------------------
