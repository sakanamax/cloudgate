案例
benchSPECT
Tomosynthesis_Simulation.tar

** Case 1 benchSPECT
執行方式, 進入 benchSPECT
$ Gate  benchSPECT.mac

相關設定
benchSPECT.mac

# O U T P U T
#####
# Select the options of the data output 
# As there are several modules, settings have to be defined for each module, especially in SPECT, where there 
# are a lots of hits for only a few counts, so it's better to limit the amount of data produced
# Here the SingleDigi output can be used if you have your own program to process the data
##

/gate/output/root/enable
/gate/output/root/setFileName benchSPECT
/gate/output/root/setRootSinglesAdderFlag 1
/gate/output/root/setRootSinglesBlurringFlag 1
/gate/output/root/setRootSinglesSpblurringFlag 1
/gate/output/root/setRootSinglesThresholderFlag 1
/gate/output/root/setRootSinglesUpholderFlag 1

Notes
* 使用 root 輸出, 輸出檔名為 xxxx.root
* 相關輸入可以參考 p207 http://www.opengatecollaboration.org/sites/default/files/GATE-UsersGuideV7.1.pdf
* Root 官方網站 https://root.cern.ch/


** Case 2

$ ls         
Seed_03


$./AMT
USAGE: ./AMT [1st Angle(int)] [Last Angle(int)] [First output index] [Total simulation number]
 EXAMPLE: 1000 simulations from angle 60 to 79 -> ./AMT 60 79 0 1000
 NOTE: if the last two terms are the same, merge only

執行方式, 進入目錄後
$./AMT   60 79  0  1000
* 從 60 度 開始 到 79度 為止
* 檔案名稱 從0 開始
* 做 1000 次

產出會到 Result/
產出為 xxx.dat
* ACII 檔案 - 使用文字編輯器開啟
  * 產出為  xxx.proj  -- 產出之後即為工作完成
* 影像檔案 -- 可以用 imageJ 或是其他影像軟體開啟

Notes
* auto_multi_threaded.c  相關設定

