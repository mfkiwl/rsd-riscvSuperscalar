# テスト対象となるモジュールの名前を指定．
UNIT_NAME         = MultiWidthFreeList

# ライブラリ名とトップレベルモジュール（シミュレーション対象）
TEST_BENCH_MODULE = Test$(UNIT_NAME)
TOP_MODULE        = $(TEST_BENCH_MODULE)Top

SOURCE_ROOT  = ../../../
TOOLS_ROOT   = ../../../../Tools/
PROJECT_WORK = ../../../../Project/ModelSim
ISE_PROJECT_ROOT = ../../../../Project/Synplify/$(UNIT_NAME)/pr_1/

# TYPES には型定義を含む package を含んだファイルを指定する．
# ファイルごとの依存関係に気をつけて，依存先が依存元より前にくるようにならべること．
TYPES = \
	BasicTypes.sv \

# テスト時のみ使用し、合成時は使用しない module の定義があるファイルを指定する．
# ここの順番は適当でも大丈夫．
TEST_MODULES = \
	Verification/TestBenchClockGenerator.sv \
	Verification/UnitTest/MultiWidthFreeList/TestMultiWidthFreeList.sv \

# それ以外の module, interface の定義があるファイルを指定する．
# ここの順番は適当でも大丈夫．
MODULES = \
	Synthesis/TED/TED_ClockGenerator.v \
	Primitives/RAM.sv \
	Primitives/Queue.sv \
	Primitives/FreeList.sv \
	Verification/UnitTest/MultiWidthFreeList/TestMultiWidthFreeListTop.sv \

# 合成時に、特定の警告を非表示にする
VLOG_OPTIONS = \
	-suppress 2605 \

# シミュレーション時に、特定の警告を非表示にする
VSIM_OPTIONS = \
	-suppress 2605 \
	-suppress 8233 \

include ../../../Makefile.inc
