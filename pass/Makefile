CLANG_PATH=/home/xudaliang/llvm-march-rve/llvm/build/bin  #change to your path

SOURCES = sgxbounds.cpp
LIB_NAME = sgxbounds.so

LDFLAGS = -L/home/xudaliang/llvm-sgxbounds/llvm/install/lib
CXXFLAGS = -ggdb3 -Wall -fno-rtti -fPIC -shared -I/home/xudaliang/llvm-sgxbounds/llvm/install/include  -D_DEBUG -D_GNU_SOURCE -D__STDC_CONSTANT_MACROS -D__STDC_FORMAT_MACROS -D__STDC_LIMIT_MACROS -O3 -fomit-frame-pointer -std=c++11 -fvisibility-inlines-hidden -fno-exceptions -fno-rtti -fPIC -ffunction-sections -fdata-sections -Wcast-qual

all: $(LIB_NAME)

$(LIB_NAME): $(SOURCES)
	g++ $(CXXFLAGS) $(LDFLAGS) $^ -o $@

clean:
	rm -f $(LIB_NAME)

