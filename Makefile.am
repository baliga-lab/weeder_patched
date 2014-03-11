TESTS = test/weeder_util_test

MAX_SEQ = 100000
ADVISER = adviser
WEEDER_TFBS = weederTFBS
WEEDERLAUNCHER = weederlauncher
LOCATOR = locator
STD_CFLAGS = -Wall -std=c89 -pedantic -O2 -Wshadow -Wpointer-arith \
	-Wcast-qual -Wcast-align -Wwrite-strings \
	-Wstrict-prototypes -Wmissing-prototypes -Wnested-externs -Wno-long-long


bin_PROGRAMS = weederlauncher weederTFBS adviser locator

weederlauncher_SOURCES = src/weederlauncher.c src/weeder_util.c
weederlauncher_CFLAGS  = $(STD_CFLAGS) -DADVISER_CMD="\"$(ADVISER)\"" -DWEEDER_TFBS_CMD="\"$(WEEDER_TFBS)\""
weederlauncher_LDADD = -lm

weederTFBS_SOURCES = src/weederTFBS.c src/weeder_util.c
weederTFBS_CFLAGS  = $(STD_CFLAGS) -DMAXSEQ=$(MAX_SEQ)
weederTFBS_LDADD = -lm

adviser_SOURCES = src/adviser.c src/weeder_util.c
adviser_CFLAGS  = $(STD_CFLAGS) -DMAXSEQ=$(MAX_SEQ)
adviser_LDADD = -lm

locator_SOURCES = src/locator.c src/weeder_util.c
locator_CFLAGS  = $(STD_CFLAGS) -DMAXSEQ=$(MAX_SEQ)
locator_LDADD = -lm

check_PROGRAMS = $(TESTS)

test_weeder_util_test_SOURCES = test/CuTest.c test/weeder_util_test.c src/weeder_util.c
test_weeder_util_test_CFLAGS  = $(STD_CFLAGS) -Isrc
test_weeder_util_test_LDADD = -lm
