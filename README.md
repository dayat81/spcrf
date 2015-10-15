CXXFLAGS =	-O2 -g -Wall -fmessage-length=0

OBJS =		main.o avputil.o diameter.o avp.o entry.o logic.o

LIBS =

TARGET =	main

$(TARGET):	$(OBJS)
	$(CXX) -o $(TARGET) $(OBJS) $(LIBS)

all:	$(TARGET)

clean:
	rm -f $(OBJS) $(TARGET)
