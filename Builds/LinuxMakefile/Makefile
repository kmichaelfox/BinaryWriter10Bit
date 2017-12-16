# Automatically generated makefile, created by the Projucer
# Don't edit this file! Your changes will be overwritten when you re-save the Projucer project!

# (this disables dependency generation if multiple architectures are set)
DEPFLAGS := $(if $(word 2, $(TARGET_ARCH)), , -MMD)

ifndef CONFIG
  CONFIG=Debug
endif

ifeq ($(CONFIG),Debug)
  BINDIR := build
  LIBDIR := build
  OBJDIR := build/intermediate/Debug
  OUTDIR := build

  ifeq ($(TARGET_ARCH),)
    TARGET_ARCH := -march=native
  endif

  CPPFLAGS := $(DEPFLAGS) -D "LINUX=1" -D "DEBUG=1" -D "_DEBUG=1" -D "JUCER_LINUX_MAKE_6D53C8B4=1" -D "JUCE_APP_VERSION=1.0.0" -D "JUCE_APP_VERSION_HEX=0x10000" -I /usr/include -I /usr/include/freetype2 -I ../../JuceLibraryCode
  CFLAGS += $(CPPFLAGS) $(TARGET_ARCH) -g -ggdb -O0
  CXXFLAGS += $(CFLAGS) -std=c++11
  LDFLAGS += $(TARGET_ARCH) -L$(BINDIR) -L$(LIBDIR) -L/usr/X11R6/lib/ 

  TARGET := BinaryWriter10Bit
  BLDCMD = $(CXX) -o $(OUTDIR)/$(TARGET) $(OBJECTS) $(LDFLAGS) $(RESOURCES) $(TARGET_ARCH)
  CLEANCMD = rm -rf $(OUTDIR)/$(TARGET) $(OBJDIR)
endif

ifeq ($(CONFIG),Release)
  BINDIR := build
  LIBDIR := build
  OBJDIR := build/intermediate/Release
  OUTDIR := build

  ifeq ($(TARGET_ARCH),)
    TARGET_ARCH := -march=native
  endif

  CPPFLAGS := $(DEPFLAGS) -D "LINUX=1" -D "NDEBUG=1" -D "JUCER_LINUX_MAKE_6D53C8B4=1" -D "JUCE_APP_VERSION=1.0.0" -D "JUCE_APP_VERSION_HEX=0x10000" -I /usr/include -I /usr/include/freetype2 -I ../../JuceLibraryCode
  CFLAGS += $(CPPFLAGS) $(TARGET_ARCH) -O3
  CXXFLAGS += $(CFLAGS) -std=c++11
  LDFLAGS += $(TARGET_ARCH) -L$(BINDIR) -L$(LIBDIR) -fvisibility=hidden -L/usr/X11R6/lib/ 

  TARGET := BinaryWriter10Bit
  BLDCMD = $(CXX) -o $(OUTDIR)/$(TARGET) $(OBJECTS) $(LDFLAGS) $(RESOURCES) $(TARGET_ARCH)
  CLEANCMD = rm -rf $(OUTDIR)/$(TARGET) $(OBJDIR)
endif

OBJECTS := \
  $(OBJDIR)/BinaryRecording_c2346f51.o \
  $(OBJDIR)/NpyFile_cb184ff4.o \
  $(OBJDIR)/OpenEphysLib_e6930301.o \
  $(OBJDIR)/SequentialBlockFile_8184f6cb.o \

.PHONY: clean

$(OUTDIR)/$(TARGET): $(OBJECTS) $(RESOURCES)
	@echo Linking BinaryWriter10Bit
	-@mkdir -p $(BINDIR)
	-@mkdir -p $(LIBDIR)
	-@mkdir -p $(OUTDIR)
	@$(BLDCMD)

clean:
	@echo Cleaning BinaryWriter10Bit
	@$(CLEANCMD)

strip:
	@echo Stripping BinaryWriter10Bit
	-@strip --strip-unneeded $(OUTDIR)/$(TARGET)

$(OBJDIR)/BinaryRecording_c2346f51.o: ../../Source/BinaryRecording.cpp
	-@mkdir -p $(OBJDIR)
	@echo "Compiling BinaryRecording.cpp"
	@$(CXX) $(CXXFLAGS) -o "$@" -c "$<"

$(OBJDIR)/NpyFile_cb184ff4.o: ../../Source/NpyFile.cpp
	-@mkdir -p $(OBJDIR)
	@echo "Compiling NpyFile.cpp"
	@$(CXX) $(CXXFLAGS) -o "$@" -c "$<"

$(OBJDIR)/OpenEphysLib_e6930301.o: ../../Source/OpenEphysLib.cpp
	-@mkdir -p $(OBJDIR)
	@echo "Compiling OpenEphysLib.cpp"
	@$(CXX) $(CXXFLAGS) -o "$@" -c "$<"

$(OBJDIR)/SequentialBlockFile_8184f6cb.o: ../../Source/SequentialBlockFile.cpp
	-@mkdir -p $(OBJDIR)
	@echo "Compiling SequentialBlockFile.cpp"
	@$(CXX) $(CXXFLAGS) -o "$@" -c "$<"

-include $(OBJECTS:%.o=%.d)
