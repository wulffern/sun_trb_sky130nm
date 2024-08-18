
#- Core makefile provides the following commands:
# -----------------------------------------------------------
# ip: generate ../design/<LIB> from ../cic/ip.json
# gds: generate gds/<CELL>.gds
# cdl: generate cdl/<CELL>.cdl
# lvs: Check cdl/<CELL>.cdl versus ../design/<LIB>/<CELL>.mag
# lpe: Extract parasitics lpe/<CELL>.spi
# drc: Run design rule checks on ../design/<LIB>/<CELL>.mag
# -----------------------------------------------------------
include ../tech/make/core.make

LIB=SUN_TRB_SKY130NM
CELL=DFRNQNX1_CV
PREFIX=SUNTRB_

#- Provide cells you want to check for the lvsall drcall commands
CELLS = ANX1_CV ANX2_CV ANX4_CV ANX8_CV BFX1_CV DFRNQNX1_CV IVTRIX1_CV IVX1_CV IVX2_CV IVX4_CV IVX8_CV NCHDL NCHDLR NDTRIX1_CV NDX1_CV NRX1_CV ORX1_CV ORX2_CV ORX4_CV PCHDL SCX1_CV SWX2_CV SWX4_CV TAPCELLAVSS_CV TAPCELLBAVSS_CV TAPCELLB_CV TGPD_CV TIEH_CV TIEL_CV

test:
	make ip
	make drcall
	make lvsall
