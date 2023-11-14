# M031BSP_CRC32_checksum
 M031BSP_CRC32_checksum


update @ 2023/11/14


1. user SRecrod tool , to calculate checksum and save into binary file

2. check generateChecksum.bat , will call generateChecksum.cmd and generateCRCbinary.cmd , to process CRC32 calculation

3. check define : ENABLE_SW_CRC32 , 

- if use hardware module to get CRC32 , disable define ENABLE_SW_CRC32

- if use software to calculate CRC32 , check define : USE_SRAM_TABLE and USE_FLASH_TABLE

4. when use hardware CRC32 , code size and ram size wille be

- code size : 6340 + 416 + 32 (base)

- ram size : 32 + 512 (base)

![image](https://github.com/released/M031BSP_CRC32_checksum/blob/main/HW_CRC32.jpg)

5. when use software CRC32 and enable USE_SRAM_TABLE , code size and ram size wille be

- code size : 6404 + 416 + 36 ( code size add extra 68 bytes)

- ram size : 36 + 1540 ( ram size add extra 1032 bytes)  

![image](https://github.com/released/M031BSP_CRC32_checksum/blob/main/SW_CRC32_SRAM_TABLE.jpg)


6. when use software CRC32 and enable USE_FLASH_TABLE , code size and ram size wille be

- code size : 6332 +1440 + 36 ( code size add extra 1020 bytes)

- ram size : 36 + 516 ( ram size add extra 8 bytes)    

![image](https://github.com/released/M031BSP_CRC32_checksum/blob/main/SW_CRC32_FLASH_TABLE.jpg)


7. under KEIL user , 

![image](https://github.com/released/M031BSP_CRC32_checksum/blob/main/KEIL_User_generatechecksum.jpg)
	

8. under KEIL Utilities , 

![image](https://github.com/released/M031BSP_CRC32_checksum/blob/main/KEIL_Utilities_programming.jpg)
	

