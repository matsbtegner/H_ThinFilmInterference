
ARNOLDINC := PATH_TO_ARNOLD_INCLUDE_DIR
ARNOLDLIB := PATH_TO_ARNOLD_INCLUDE_LIB

# if your g++ is located somewhere else
GXXLOC    := 
TARGETLOC := 

INCLUDES := -I$(ARNOLDINC)
LDFLAGS  := -L$(ARNOLDLIB) -lai
CXXFLAGS := -w -O2 -fPIC -DLINUX -D_BOOL -ffast-math -DGCC_VERSION=4.1.2
CXX	     := $(GXXLOC)g++

SOURCES  := H_ThinFilmInterference.cpp
OBJECTS  := $(SOURCES:.cpp=.o)
TARGET   := $(TARGETLOC)H_ThinFilmInterference.so

$(TARGET) : $(OBJECTS)
	$(CXX) $(inputs) -shared $< -o $@ $(LDFLAGS)

%.o : %.cpp
	$(CXX) $(CXXFLAGS) $(INCLUDES) -c $< -o $@

all: $(TARGET)

clean:
	rm $(OBJECTS) $(TARGET)