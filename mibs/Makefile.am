## Makefile.am
## vim: ts=3
##
## Process this file with automake to produce Makefile.in

mibs_DATA = SIGSCALE-SMI.mib \
		SIGSCALE-TC.mib \
		SIGSCALE-MODULES-MIB.mib \
		SIGSCALE-PRODUCTS-MIB.mib

check_DATA = .tree_ok

.tree_ok:
	@if snmptranslate -V > /dev/null 2>&1; then \
		snmptranslate -M +$(top_srcdir)/mibs \
			-m +SIGSCALE-SMI:SIGSCALE-MODULES-MIB:SIGSCALE-PRODUCTS-MIB \
			-Lo -Tp -IR sigscale; \
	fi

