# OP_PC-
optimzation for  for all windows 
step <1> 
@echo off
title PC Optimization Script
color 0A

echo ---------------------------------
echo       🚀 Windows PC Optimization 🚀
echo -———————————————--

:: Cleanup temporary files
echo [1] Cleaning temporary files...
del /s /f /q %temp%\*.* >nul 2>&1
del /s /f /q C:\Windows\Temp\*.* >nul 2>&1

:: Clear Prefetch
echo [2] Clearing Prefetch...
del /s /f /q C:\Windows\Prefetch\*.* >nul 2>&1

:: Empty Recycle Bin
echo [3] Emptying Recycle Bin...
rd /s /q %systemdrive%\$Recycle.Bin

:: Flush DNS
echo [4] Flushing DNS cache...
ipconfig /flushdns

:: Check disk
echo [5] Checking and repairing disk (quick)...
chkdsk C: /f

:: Optimize drives
echo [6] Optimizing drives...
defrag C: /O

:: End
echo -————————————————
echo ✅ Optimization Completed!
echo ---------------------------------
pause
exit
for xit pro exit for applicoaton
