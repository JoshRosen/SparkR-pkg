SCALA_VERSION := 2.10
JAR_NAME := sparkr-assembly-0.1.jar
TARGET_NAME := target/scala-$(SCALA_VERSION)/$(JAR_NAME)
SCALA_SOURCE_DIR := src/main/scala/edu/berkeley/cs/amplab/sparkr
RESOURCE_DIR := src/main/resources

SCALA_FILES := $(wildcard $(SCALA_SOURCE_DIR)/*.scala)
RESOURCE_FILES := $(wildcard $(RESOURCE_DIR)/*)

all: $(TARGET_NAME)

$(TARGET_NAME): $(SCALA_FILES) $(RESOURCE_FILES)
	./sbt/sbt assembly
	cp $(TARGET_NAME) ../inst/

clean:
	./sbt/sbt clean
	rm -rf target
	rm -rf project/target
	rm -rf project/project
	rm sbt/sbt-launch-*.jar
	rm ../inst/$(JAR_NAME)

.PHONY: all clean
