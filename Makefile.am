#
#   This file is part of Sylverant PSO Server.
#
#   Copyright (C) 2009, 2011, 2018 Lawrence Sebald
#
#   This program is free software: you can redistribute it and/or modify
#   it under the terms of the GNU Affero General Public License version 3
#   as published by the Free Software Foundation.
#
#   This program is distributed in the hope that it will be useful,
#   but WITHOUT ANY WARRANTY; without even the implied warranty of
#   MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
#   GNU Affero General Public License for more details.
#
#   You should have received a copy of the GNU Affero General Public License
#   along with this program.  If not, see <http://www.gnu.org/licenses/>.

ACLOCAL_AMFLAGS = -I m4

LIBS += $(MYSQL_LIBS) $(LIBICONV)

bin_PROGRAMS = login_server
login_server_SOURCES = src/dclogin.c src/login.c src/login.h \
                       src/login_packets.c src/login_packets.h \
                       src/login_server.c src/bblogin.c src/bbcharacter.c \
                       src/patch.h src/patch.c src/patch_stubs.h

if NEED_PIDFILE
AM_CFLAGS = -DNEED_PIDFILE=1
login_server_SOURCES += src/pidfile.c
endif

datarootdir = @datarootdir@

EXTRA_DIST = config.rpath patch/dreamcast/patch_stub.s \
             patch/dreamcast/version_detect.s
SUBDIRS = l10n
