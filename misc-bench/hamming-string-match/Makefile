# Makefile: C++ version of hamming string match
# Copyright (c) 2025 University of Virginia
# This file is licensed under the MIT License.
# See the LICENSE file in the root of this repository for more details.

SUBDIRS := PIM hamming-data-generator

.PHONY: debug perf dramsim3_integ clean $(SUBDIRS)
.DEFAULT_GOAL := perf

USE_OPENMP ?= 0

debug perf dramsim3_integ clean: $(SUBDIRS)

$(SUBDIRS):
	$(MAKE) -C $@ $(MAKECMDGOALS) USE_OPENMP=$(USE_OPENMP)