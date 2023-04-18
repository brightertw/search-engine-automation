TOP_DIR := $(patsubst %/,%,$(dir $(realpath $(lastword $(MAKEFILE_LIST)))))

COMMIT_REV := $(shell git rev-parse HEAD)

# This can be used to customized local builds.
-include $(TOP_DIR)/Local.mk
GO ?= go

export TOP_DIR
GOBIN ?= $(TOP_DIR)/bin
export GOBIN
CONDA_ENV_DIR := $(TOP_DIR)/conda-env
PATH := $(CONDA_ENV_DIR)/bin:$(PATH)
export PATH

include conda-env.mk
.PHONY: conda-env
conda-env: conda-env-reusable

PREFERRED_INTERACTIVE_SHELL ?= bash
PS1_NAME ?= 'search'
MAKE_SHELL_PS1 ?= '$(PS1_NAME) $$ '
.PHONY: shell
shell:
	@INIT_FILE=$(shell mktemp); \
	printf '[ -e $$HOME/.bashrc ] && source $$HOME/.bashrc\n' > $$INIT_FILE; \
	printf '[ -e Local.env ] && source Local.env\n' >> $$INIT_FILE; \
	printf '[ "$$(which gocomplete)" != "" ] && complete -C "$$(which gocomplete)" go\n' >> $$INIT_FILE; \
	printf 'PS1='"$(MAKE_SHELL_PS1) "'\n' >> $$INIT_FILE; \
	$(shell which bash) --init-file $$INIT_FILE || true
