CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

PROJECT(Remind)

INCLUDE_DIRECTORIES("${CMAKE_CURRENT_SOURCE_DIR}/src")

SET(remind_srcs
	src/calendar.c
	src/dynbuf.c
	src/dorem.c
	src/dosubst.c
	src/expr.c
	src/files.c
	src/funcs.c
	src/globals.c
	src/hbcal.c
	src/init.c
	src/main.c
	src/md5.c
	src/moon.c
	src/omit.c
	src/queue.c
	src/sort.c
	src/token.c
	src/trigger.c
	src/userfns.c
	src/utils.c
	src/var.c
	)
ADD_EXECUTABLE(remind ${remind_srcs})
TARGET_LINK_LIBRARIES(remind m)

SET(rem2ps_srcs
	src/rem2ps.c
	src/dynbuf.c
	)
ADD_EXECUTABLE(rem2ps ${rem2ps_srcs})

