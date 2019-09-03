CXXFLAGS = -I /home/sky/anaconda3/include/python3.6m -I include   -std=c++11 -O3 -lopencv_world -L /usr/local/lib64

DEPS = lanms.h $(shell find include -xtype f)
CXX_SOURCES = adaptor.cpp include/clipper/clipper.cpp
OPENCV = `pkg-config --cflags --libs opencv_world`

LIB_SO = adaptor.so

$(LIB_SO): $(CXX_SOURCES) $(DEPS)
	$(CXX) -o $@ $(CXXFLAGS) $(LDFLAGS) $(CXX_SOURCES) --shared -fPIC $(OPENCV)

clean:
	rm -rf $(LIB_SO)
