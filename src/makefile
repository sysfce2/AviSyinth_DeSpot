
# Use these for MS VC (by Fizick)
CXX=cl.exe
CXXFLAGS= /LD /Ox /O2 /D "NDEBUG" /D "WIN32" /D "_WINDOWS"

LINK32=link.exe
LINK32FLAGS= /dll /nologo

# Resource compiler. 
RC=rc.exe

despot.dll: despot.obj despot-f.obj despot.res
	$(LINK32) $(LINK32FLAGS) despot.obj despot-f.obj despot.res /out:despot.dll

despot.obj: despot.cpp despot.hpp
	$(CXX) $(CXXFLAGS) despot.cpp /c

despot-f.obj: despot-f.cpp despot.hpp
	$(CXX) $(CXXFLAGS) despot-f.cpp /c

despot.res: despot.rc
	$(RC) despot.rc
