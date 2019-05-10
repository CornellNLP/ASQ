### Human annotations

This directory contains three files:

- *asq_annotation.json*: 
	- a file containing test instances we set aside for human annotations.
-  *annotation_first.json*: 
	- first round annotations on a subset of 200 instances.
- *annotation_second.json*: 
	- second round annotations on 75 of the above 200 instances. 

#### Annotations labels 

For each test item, we obtain two types of annotations, and have number-coded them as follows:

```python
# the annotator's answer for the test instance 
annotator_choice = {"qn1": 0, "qn2": 1}

# the compatibility category of a candidate question to the given narrative
# this annotation is done for both question options
compatibility_type = {"Very general": 0, 
	"Compatible and likely": 1, 
	"Compatible but unlikely": 2, 
	"Incompatible (explicit)": 3, 
	"Incompatible (implicit)": 4}
``` 

The annotation-prefixed files contain human annotation information only. For each annotated instance, we provide the following fields:

- id: post id of the test instance being annotated 
- true_label: actual correct answer for the test instance
- annotated_label: annotator's answer choice for the test instance
- true_qn_type: compatibility type rated by the annotator for the actual question. 
- paired_qn_type: compatibility type rated by the annotator for the paired alternative question. 

These human judgments can be matched with the actual instances in asq_annotation.json by id. Note that we have reserved aside 500 such instances, out of which only 200 are actually annotated. 