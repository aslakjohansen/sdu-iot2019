TARGETS = \
	results.txt \


main: ${TARGETS}

clean:
	touch ${TARGETS} model.ttl ontology.ttl
	rm -f ${TARGETS} model.ttl ontology.ttl

mrproper: clean
	touch dummy~
	rm -f     *~


ontology.ttl: generate-ontology
	./generate-ontology

model.ttl: generate-model
	./generate-model

results.txt: query-model ontology.ttl model.ttl
	./query-model > results.txt

