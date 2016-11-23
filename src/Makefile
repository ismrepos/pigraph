TARGET 		= pigraph

CXX 			= icc

CXXFLAGS	= -std=c++1y -O3 -Wall
LIBS      = -I/usr/include/boost

SRCS = $(shell ls *.cc)
OBJS = $(SRCS:.cc=.o)

$(TARGET): $(OBJS) $(HEADS)
	$(CXX) ${CXXFLAGS} -o $(TARGET) $(OBJS) $(LIBS)

all: $(TARGET)

clean:
	rm -f *.o $(TARGET)
