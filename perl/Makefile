ROOT := $(shell cd ..; pwd)
LANG := perl
BIN := perl
GRAMMAR := lib/Grammar.pm

TEST_DEPS := \
    ../test/testml \
    ../test/suite \
    ext-perl \


include $(ROOT)/.common.mk


export PERL5LIB := $(ROOT)/perl/ext-perl/lib/perl5

ext-perl:
	git branch --track $@ origin/$@ 2>/dev/null || true
	git worktree add -f $@ $@

clean::
	rm -fr ext-perl
