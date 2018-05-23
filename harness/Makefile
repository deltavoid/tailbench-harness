
#include ../Makefile.config

CXX = g++
CXXFLAGS = -O3 -g -fPIC -std=c++0x
COMMON_INCLUDES = dist.h helpers.h msgs.h


default: client.o  tbench_server_networked.o tbench_client_networked.o 


client.o : client.cpp client.h $(COMMON_INCLUDES)
	$(CXX) $(CXXFLAGS) -c $< -o $@

tbench_server_networked.o : tbench_server_networked.cpp tbench_server.h \
	server.h $(COMMON_INCLUDES)
	$(CXX) $(CXXFLAGS) -c $< -o $@

tbench_client_networked.o : tbench_client_networked.cpp tbench_client.h \
	server.h client.h $(COMMON_INCLUDES)
	$(CXX) $(CXXFLAGS) -c $< -o $@


clean:
	rm *.o 

