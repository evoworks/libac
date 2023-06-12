# Wedit Makefile for project libac
SRCDIR=d:\projects\le_libac\libac_code
CFLAGS=-Ic:\lcc\include  -g2 
CC=$(LCCROOT)\bin\lcc.exe
LINKER=$(LCCROOT)\bin\lcclnk.exe
OBJS=\
	treesub.obj \
	treespace.obj \
	tools.obj \
	libac_mod.obj

LIBS=
EXE=libac.exe

$(EXE):	$(OBJS) Makefile
	$(LINKER)  -subsystem console -o $(SRCDIR)\lcc\libac.exe $(OBJS) $(LIBS)

# Build treesub.c
TREESUB_C=\

treesub.obj: $(TREESUB_C) $(SRCDIR)\treesub.c
	$(CC) -c $(CFLAGS) $(SRCDIR)\treesub.c

# Build treespace.c
TREESPACE_C=\
	$(SRCDIR)\paml.h\

treespace.obj: $(TREESPACE_C) $(SRCDIR)\treespace.c
	$(CC) -c $(CFLAGS) $(SRCDIR)\treespace.c

# Build tools.c
TOOLS_C=\
	$(SRCDIR)\paml.h\

tools.obj: $(TOOLS_C) $(SRCDIR)\tools.c
	$(CC) -c $(CFLAGS) $(SRCDIR)\tools.c

# Build libac_mod.c
LIBAC_MOD_C=\
	$(SRCDIR)\paml.h\
	$(SRCDIR)\treesub.c\
	$(SRCDIR)\treespace.c\
	$(SRCDIR)\paml.h\

libac_mod.obj: $(LIBAC_MOD_C) $(SRCDIR)\libac_mod.c
	$(CC) -c $(CFLAGS) $(SRCDIR)\libac_mod.c

link:
	$(LINKER)  -subsystem console -o $(SRCDIR)\lcc\libac.exe $(OBJS) $(LIBS)

clean:
	del $(OBJS) libac.exe
