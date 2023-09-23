cmake_minimum_required(VERSION 3.10)

project(af_lib)
set(LIB_INCLUDES 
        /home/ustb5g/5gc/open5gs/lib
        /home/ustb5g/5gc/open5gs/lib/app
        /home/ustb5g/5gc/open5gs/lib/asn1c
        /home/ustb5g/5gc/open5gs/lib/asn1c/common
        /home/ustb5g/5gc/open5gs/lib/asn1c/ngap
        /home/ustb5g/5gc/open5gs/lib/asn1c/s1ap
        /home/ustb5g/5gc/open5gs/lib/asn1c/support
        /home/ustb5g/5gc/open5gs/lib/asn1c/support/ngap-r16.1.0
        /home/ustb5g/5gc/open5gs/lib/asn1c/support/ngap-r16.4.0
        /home/ustb5g/5gc/open5gs/lib/asn1c/support/ngap-r16.7.0
        /home/ustb5g/5gc/open5gs/lib/asn1c/support/ngap-r17.3.0
        /home/ustb5g/5gc/open5gs/lib/asn1c/support/s1ap-r16.1.0
        /home/ustb5g/5gc/open5gs/lib/asn1c/support/s1ap-r16.4.0
        /home/ustb5g/5gc/open5gs/lib/asn1c/support/s1ap-r16.7.0
        /home/ustb5g/5gc/open5gs/lib/asn1c/support/s1ap-r17.3.0
        /home/ustb5g/5gc/open5gs/lib/asn1c/util
        /home/ustb5g/5gc/open5gs/lib/core
        /home/ustb5g/5gc/open5gs/lib/crypt
        /home/ustb5g/5gc/open5gs/lib/dbi
        /home/ustb5g/5gc/open5gs/lib/diameter
        /home/ustb5g/5gc/open5gs/lib/diameter/common
        /home/ustb5g/5gc/open5gs/lib/diameter/cx
        /home/ustb5g/5gc/open5gs/lib/diameter/gx
        /home/ustb5g/5gc/open5gs/lib/diameter/gy
        /home/ustb5g/5gc/open5gs/lib/diameter/rx
        /home/ustb5g/5gc/open5gs/lib/diameter/s6a
        /home/ustb5g/5gc/open5gs/lib/diameter/s6b
        /home/ustb5g/5gc/open5gs/lib/diameter/swx
        /home/ustb5g/5gc/open5gs/lib/gtp
        /home/ustb5g/5gc/open5gs/lib/gtp/v1
        /home/ustb5g/5gc/open5gs/lib/gtp/v1/support
        /home/ustb5g/5gc/open5gs/lib/gtp/v1/support/cache
        /home/ustb5g/5gc/open5gs/lib/gtp/v2
        /home/ustb5g/5gc/open5gs/lib/gtp/v2/support
        /home/ustb5g/5gc/open5gs/lib/gtp/v2/support/cache
        /home/ustb5g/5gc/open5gs/lib/ipfw
        /home/ustb5g/5gc/open5gs/lib/ipfw/objs
        /home/ustb5g/5gc/open5gs/lib/ipfw/objs/include_e
        /home/ustb5g/5gc/open5gs/lib/ipfw/objs/include_e/net
        /home/ustb5g/5gc/open5gs/lib/ipfw/objs/include_e/netinet
        /home/ustb5g/5gc/open5gs/lib/ipfw/objs/include_e/sys
        /home/ustb5g/5gc/open5gs/lib/metrics
        /home/ustb5g/5gc/open5gs/lib/metrics/prometheus
        /home/ustb5g/5gc/open5gs/lib/metrics/void
        /home/ustb5g/5gc/open5gs/lib/nas
        /home/ustb5g/5gc/open5gs/lib/nas/5gs
        /home/ustb5g/5gc/open5gs/lib/nas/5gs/support
        /home/ustb5g/5gc/open5gs/lib/nas/5gs/support/cache
        /home/ustb5g/5gc/open5gs/lib/nas/common
        /home/ustb5g/5gc/open5gs/lib/nas/eps
        /home/ustb5g/5gc/open5gs/lib/nas/eps/support
        /home/ustb5g/5gc/open5gs/lib/nas/eps/support/cache
        /home/ustb5g/5gc/open5gs/lib/ngap
        /home/ustb5g/5gc/open5gs/lib/pfcp
        /home/ustb5g/5gc/open5gs/lib/pfcp/support
        /home/ustb5g/5gc/open5gs/lib/pfcp/support/cache
        /home/ustb5g/5gc/open5gs/lib/proto
        /home/ustb5g/5gc/open5gs/lib/s1ap
        /home/ustb5g/5gc/open5gs/lib/sbi
        /home/ustb5g/5gc/open5gs/lib/sbi/contrib
        /home/ustb5g/5gc/open5gs/lib/sbi/custom
        /home/ustb5g/5gc/open5gs/lib/sbi/openapi
        /home/ustb5g/5gc/open5gs/lib/sbi/openapi/external
        /home/ustb5g/5gc/open5gs/lib/sbi/openapi/include
        /home/ustb5g/5gc/open5gs/lib/sbi/openapi/model
        /home/ustb5g/5gc/open5gs/lib/sbi/openapi/src
        /home/ustb5g/5gc/open5gs/lib/sbi/support
        /home/ustb5g/5gc/open5gs/lib/sbi/support/r16-20210629-openapitools-5.2.0
        /home/ustb5g/5gc/open5gs/lib/sbi/support/r16-20210629-openapitools-5.2.0/modified
        /home/ustb5g/5gc/open5gs/lib/sbi/support/r16-20210629-openapitools-5.2.0/openapi-generator
        /home/ustb5g/5gc/open5gs/lib/sbi/support/r16-20210629-openapitools-5.2.0/openapi-generator/templates
        /home/ustb5g/5gc/open5gs/lib/sbi/support/r16-20210629-openapitools-5.2.0/standard
        /home/ustb5g/5gc/open5gs/lib/sbi/support/r16-20230226-openapitools-6.4.0
        /home/ustb5g/5gc/open5gs/lib/sbi/support/r16-20230226-openapitools-6.4.0/modified
        /home/ustb5g/5gc/open5gs/lib/sbi/support/r16-20230226-openapitools-6.4.0/openapi-generator
        /home/ustb5g/5gc/open5gs/lib/sbi/support/r16-20230226-openapitools-6.4.0/openapi-generator/templates
        /home/ustb5g/5gc/open5gs/lib/sbi/support/r16-20230226-openapitools-6.4.0/standard
        /home/ustb5g/5gc/open5gs/lib/sbi/support/r17-20230301-openapitools-6.4.0
        /home/ustb5g/5gc/open5gs/lib/sbi/support/r17-20230301-openapitools-6.4.0/modified
        /home/ustb5g/5gc/open5gs/lib/sbi/support/r17-20230301-openapitools-6.4.0/openapi-generator
        /home/ustb5g/5gc/open5gs/lib/sbi/support/r17-20230301-openapitools-6.4.0/openapi-generator/templates
        /home/ustb5g/5gc/open5gs/lib/sbi/support/r17-20230301-openapitools-6.4.0/standard
        /home/ustb5g/5gc/open5gs/lib/sctp
        /home/ustb5g/5gc/open5gs/lib/tun
        /home/ustb5g/5gc/open5gs/build/lib/core
)
set(LIB_INCLUDES1 
        /home/ustb5g/5gc/open5gs/src
        /home/ustb5g/5gc/open5gs/src/amf
        /home/ustb5g/5gc/open5gs/src/ausf
        /home/ustb5g/5gc/open5gs/src/bsf
        /home/ustb5g/5gc/open5gs/src/hss
        /home/ustb5g/5gc/open5gs/src/mme
        /home/ustb5g/5gc/open5gs/src/nrf
        /home/ustb5g/5gc/open5gs/src/nssf
        /home/ustb5g/5gc/open5gs/src/pcf
        /home/ustb5g/5gc/open5gs/src/pcrf
        /home/ustb5g/5gc/open5gs/src/scp
        /home/ustb5g/5gc/open5gs/src/sgwc
        /home/ustb5g/5gc/open5gs/src/sgwu
        /home/ustb5g/5gc/open5gs/src/smf
        /home/ustb5g/5gc/open5gs/src/udm
        /home/ustb5g/5gc/open5gs/src/udr
        /home/ustb5g/5gc/open5gs/src/upf)
set(LIB_INCLUDES2 
        /home/ustb5g/5gc/open5gs/tests
        /home/ustb5g/5gc/open5gs/tests/310014
        /home/ustb5g/5gc/open5gs/tests/af
        /home/ustb5g/5gc/open5gs/tests/af/build
        /home/ustb5g/5gc/open5gs/tests/af/build/CMakeFiles
        /home/ustb5g/5gc/open5gs/tests/af/build/CMakeFiles/3.22.1
        /home/ustb5g/5gc/open5gs/tests/af/build/CMakeFiles/3.22.1/CompilerIdC
        /home/ustb5g/5gc/open5gs/tests/af/build/CMakeFiles/3.22.1/CompilerIdC/tmp
        /home/ustb5g/5gc/open5gs/tests/af/build/CMakeFiles/3.22.1/CompilerIdCXX
        /home/ustb5g/5gc/open5gs/tests/af/build/CMakeFiles/3.22.1/CompilerIdCXX/tmp
        /home/ustb5g/5gc/open5gs/tests/af/build/CMakeFiles/CMakeTmp
        /home/ustb5g/5gc/open5gs/tests/af/build/CMakeFiles/af.dir
        /home/ustb5g/5gc/open5gs/tests/af/build/CMakeFiles/ims_af_test.dir
        /home/ustb5g/5gc/open5gs/tests/app
        /home/ustb5g/5gc/open5gs/tests/attach
        /home/ustb5g/5gc/open5gs/tests/common
        /home/ustb5g/5gc/open5gs/tests/core
        /home/ustb5g/5gc/open5gs/tests/crypt
        /home/ustb5g/5gc/open5gs/tests/csfb
        /home/ustb5g/5gc/open5gs/tests/fuzzing
        /home/ustb5g/5gc/open5gs/tests/handover
        /home/ustb5g/5gc/open5gs/tests/non3gpp
        /home/ustb5g/5gc/open5gs/tests/registration
        /home/ustb5g/5gc/open5gs/tests/sctp
        /home/ustb5g/5gc/open5gs/tests/slice
        /home/ustb5g/5gc/open5gs/tests/unit
        /home/ustb5g/5gc/open5gs/tests/volte
        /home/ustb5g/5gc/open5gs/tests/vonr
        )
# 将目录路径变量添加到include
include_directories(${LIB_INCLUDES})
include_directories(${LIB_INCLUDES1})
include_directories(${LIB_INCLUDES2})
set(CMAKE_C_STANDARD 11) 

file(GLOB SRC_FILES s.c)
file(GLOB HEADER_FILES *.h)
add_library(af ${SRC_FILES} ${HEADER_FILES})

# target_link_libraries(af m)
file(GLOB_RECURSE LIB_SO "/home/ustb5g/5gc/open5gs/*.so")

# 生成库目标
add_library(extra_libs ${LIB_SO})
message(STATUS "Lib headers: ${LIB_SO}") 
# target_link_libraries(af m)
file(GLOB_RECURSE LIB_SO1 "/home/ustb5g/5gc/open5gs/*.a")

# 生成库目标
# add_library(extra_libs1 ${LIB_SO1})
message(STATUS "Lib headers: ${LIB_SO1}") 

# 设置库类型为SHARED
set_target_properties(extra_libs PROPERTIES LINKER_LANGUAGE C)

add_executable(s s.c)
target_link_libraries(s ${LIB_SO}  ${LIB_SO1}  /home/ustb5g/5gc/open5gs/build/lib/core/libogscore.so /home/ustb5g/5gc/open5gs/build/tests/af/libaf.a /home/ustb5g/5gc/open5gs/build/lib/app/libogsapp.so /lib/x86_64-linux-gnu/libtalloc.so  )