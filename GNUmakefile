##############################################################################
#
# GNUmakefile
#
##############################################################################


default: egg


egg:
    # setup.py will call 'make build' before creating the egg
	python setup.py bdist_egg


build:


clean:
	rm -rf build temp
	rm -rf *.egg-info
	find . -name *.pyc | xargs rm
