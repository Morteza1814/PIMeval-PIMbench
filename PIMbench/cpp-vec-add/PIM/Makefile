# Makefile: C++ version of vector addition
# Copyright (c) 2024 University of Virginia
# This file is licensed under the MIT License.
# See the LICENSE file in the root of this repository for more details.

LIBPIMEVAL_PATH = ../../../libpimeval
include ../../Makefile.common

EXEC := vec-add.out
SRC := vec-add.cpp

# make USE_OPENMP=1
USE_OPENMP ?= 0
ifeq ($(USE_OPENMP),1)
	CXXFLAGS += -fopenmp
endif

debug perf dramsim3_integ: $(EXEC)

$(EXEC): $(SRC) $(DEPS)
	$(CXX) $< $(CXXFLAGS) -o $@

clean:
	rm -rf $(EXEC) *.dSYM