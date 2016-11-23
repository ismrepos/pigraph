TARGET 		= pigraph

CXX 			= icc

CXXFLAGS = 
LIB = 
MKLROOT = /opt/intel/mkl
CXXFLAGS	+= -std=c++1y -O3 -Wall -I${MKLROOT}/include 
LIB				+= -L${MKLROOT}/lib/intel64 -lmkl_rt -lpthread -lm -ldl

SRCS = $(shell ls *.cc)
OBJS = $(SRCS:.cc=.o)

$(TARGET): $(OBJS) $(HEADS)
	$(CXX) ${CXXFLAGS} -o $(TARGET) $(OBJS) ${LIB}

all: $(TARGET)

clean:
	rm -f *.o $(TARGET)
