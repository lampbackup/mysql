# Copyright (c) 2006, 2013, Oracle and/or its affiliates. All rights reserved.
#
# This program is free software; you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation; version 2 of the License.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program; if not, write to the Free Software
# Foundation, Inc., 51 Franklin St, Fifth Floor, Boston, MA  02110-1301  USA

SUBDIRS      = mytap . mysys examples strings my_decimal

EXTRA_DIST = unit.pl
CLEANFILES = unit

unittests = mytap mysys strings my_decimal @mysql_se_unittest_dirs@  @mysql_pg_unittest_dirs@

test:
	perl unit.pl run $(unittests)

test-verbose:
	HARNESS_VERBOSE=1 perl unit.pl run $(unittests)

# Don't update the files from bitkeeper
%::SCCS/s.%
