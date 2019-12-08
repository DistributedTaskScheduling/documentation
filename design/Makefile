all:
	mkdir -p build
	mkdir -p build/sequence
	mkdir -p build/activity
	export PLANTUML_LIMIT_SIZE=1000000
	plantuml -output ../build/sequence sequence/*.puml
	plantuml -output ../build/activity activity/*.puml
