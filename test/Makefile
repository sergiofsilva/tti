
#export LD_LIBRARY_PATH=${TORCS_BASE}/export/lib:$LD_LIBRARY_PATH

ttest: ttest.o SimpleDriver.o
	g++ -L${TORCS_BASE}/export/lib -L/usr/lib  -o ttest ttest.o SimpleDriver.o -ltti -ltgf -ltxml

ttest.o: ttest.cpp 
	g++ -I${TORCS_BASE}/export/include -I/usr/src/torcs/torcs-1.3.4 -I. -std=c++11 -pthread -c ttest.cpp 

SimpleDriver.o: SimpleDriver.h SimpleDriver.cpp 
	g++ -I${TORCS_BASE}/export/include -I/usr/src/torcs/torcs-1.3.4 -I. -c SimpleDriver.cpp 

