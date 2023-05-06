cmake_minimum_required(VERSION 3.0.0)
project(RTKLIB)
set(SOURCES
    convkml.c
    convrnx.c
    datum.c
    download.c
    ephemeris.c
    geoid.c
    ionex.c
    lambda.c
    options.c
    pntpos.c
    postpos.c
    ppp.c
    ppp_ar.c
    preceph.c
    # qzslex.c
    rcvraw.c
    rinex.c
    rtcm.c
    rtcm2.c
    rtcm3.c
    rtcm3e.c
    rtkcmn.c
    rtkpos.c
    rtksvr.c
    sbas.c
    solution.c
    stream.c
    streamsvr.c
    tle.c
    rcv/binex.c
    rcv/crescent.c
    # rcv/gw10.c
    rcv/javad.c
    rcv/novatel.c
    rcv/nvs.c
    # rcv/rcvlex.c
    rcv/rt17.c
    rcv/septentrio.c
    rcv/ss2.c
    rcv/ublox.c
)
add_library(RTKLIB STATIC ${SOURCES})
# Add include directory
target_include_directories(RTKLIB PUBLIC ${CMAKE_CURRENT_SOURCE_DIR} ${CMAKE_CURRENT_SOURCE_DIR}/rcv)