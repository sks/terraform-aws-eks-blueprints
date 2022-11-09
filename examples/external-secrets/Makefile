default: all
VAR_FILE="prod.tfvars"
TF_OUT_FILE="tf.out"

init:
	terraform init \
		-backend-config=backend.conf

plan: init
	terraform plan \
		-out ${TF_OUT_FILE} \
		-var-file=${VAR_FILE}

apply: plan
	terraform apply \
     	${TF_OUT_FILE}

all: plan