@echo off
title IP Tool
color a
cls
echo "#####################################"
echo "#####---#|--\####---#/-\#/-\#|#######"
echo "######|##|--/#####|##| |#| |#|#######"
echo "#####---#|########|##\-/#\-/#|--#####"
echo "#####################################"
set /p ip=IP Address: 
echo IP Tool Results>>result.txt
echo --------------->>result.txt
echo IP Address: "%ip%">>result.txt
ping "%ip%"
ping "%ip%">>result.txt
timeout 10
nmap "%ip%"
nmap "%ip%">>result.txt
timeout 10
tracert "%ip%"
tracert "%ip%">>result.txt
timeout 10
nslookup "%ip%"
nslookup "%ip%">>result.txt
timeout 10
pathping "%ip%"
pathping "%ip%">>result.txt
pause >nil
