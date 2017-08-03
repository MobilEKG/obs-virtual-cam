cmake_minimum_required(VERSION 3.5)

project(baseclasses)

set(baseclasses_SOURCES
    amextra.cpp
    amfilter.cpp
    amvideo.cpp
    arithutil.cpp
    combase.cpp
    cprop.cpp
    ctlutil.cpp
    ddmm.cpp
    dllentry.cpp
    dllsetup.cpp
    mtype.cpp
    outputq.cpp
    perflog.cpp
    pstream.cpp
    pullpin.cpp
    refclock.cpp
    renbase.cpp
    schedule.cpp
    seekpt.cpp
    source.cpp
    strmctl.cpp
    sysclock.cpp
    transfrm.cpp
    transip.cpp
    videoctl.cpp
    vtrans.cpp
    winctrl.cpp
    winutil.cpp
    wxdebug.cpp
    wxlist.cpp
    wxutil.cpp
	)

set(baseclasses_HEADERS
    amextra.h
    amfilter.h
    cache.h
    checkbmi.h
    combase.h
    cprop.h
    ctlutil.h
    ddmm.h
    dllsetup.h
    dxmperf.h
    fourcc.h
    measure.h
    msgthrd.h
    mtype.h
    outputq.h
    perflog.h
    perfstruct.h
    pstream.h
    pullpin.h
    refclock.h
    reftime.h
    renbase.h
    schedule.h
    seekpt.h
    source.h
    streams.h
    strmctl.h
    sysclock.h
    transfrm.h
    transip.h
    videoctl.h
    vtrans.h
    winctrl.h
    winutil.h
    wxdebug.h
    wxlist.h
    wxutil.h
	)

# Properties->C/C++->General->Additional Include Directories
include_directories(
    .
    )

add_library(baseclasses STATIC
	${baseclasses_SOURCES}
	${baseclasses_HEADERS}
    )

# Properties->General->Output Directory
set_target_properties(baseclasses PROPERTIES RUNTIME_OUTPUT_DIRECTORY_DEBUG "Debug")
set_target_properties(baseclasses PROPERTIES RUNTIME_OUTPUT_DIRECTORY_RELEASE "Release")

set_target_properties(baseclasses PROPERTIES OUTPUT_NAME_DEBUG ${OutDir}strmbasd)
set_target_properties(baseclasses PROPERTIES OUTPUT_NAME_RELEASE ${OutDir}strmbase)



