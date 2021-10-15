objects= digital_factory/platform/datalake/ContainerForIngressAndStorage.markdown

all:$(objects)

clean:
	@rm -rf $(objects)

$(objects): %.markdown: %.puml
	@echo '### Diagram of '$< > $@ 																						\
	    && echo "" >> $@																								\
		&& echo '![image](http://www.plantuml.com/plantuml/svg/'$(shell cat $< | docker run --rm -i -a STDIN -a STDOUT 	\
			zhangli2946/render:puml-1.2021.12-openjdk8 java -jar plantuml.jar -p -tsvg -encodeurl)')' >> $@ 			\
	    && echo "" >> $@

