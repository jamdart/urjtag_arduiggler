#
# $Id$
#
# Copyright (C) 2002,2011 ETC s.r.o.
#
# This program is free software; you can redistribute it and/or
# modify it under the terms of the GNU General Public License
# as published by the Free Software Foundation; either version 2
# of the License, or (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program; if not, write to the Free Software
# Foundation, Inc., 59 Temple Place - Suite 330, Boston, MA
# 02111-1307, USA.
#
# Written by Steve Tell <tell@telltronics.org> 2011
#

EXTRA_DIST = setup.py chain.c pycompat23.h t_urjtag_chain.py

all-local: build

build: chain.c
	{ $(PYTHON) setup.py build && touch build; } || { $(RM) -r build; exit 1; }

install-data-local:
	$(PYTHON) setup.py install --prefix=$(DESTDIR)$(prefix)

clean-local:
	$(RM) -fr build

