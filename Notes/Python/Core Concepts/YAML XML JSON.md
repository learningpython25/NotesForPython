## JSON – *JavaScript Object Notation*

* Based on `key: value` pairs
* Supports:

  * Numbers, strings, booleans
  * Arrays (lists)
  * Objects (dicts)
  * null

### Example

```json
{
  "name": "Alice",
  "age": 30,
  "married": false,
  "children": null,
  "skills": ["Python", "SQL"],
  "education": {
    "degree": "MSc",
    "university": "MIT"
  }
}
```

### Python Usage

```python
import json

# Encoding (Python → JSON string)
person = {
    "name": "Alice",
    "age": 30,
    "skills": ["Python", "SQL"]
}
json_str = json.dumps(person)

# Decoding (JSON string → Python)
parsed = json.loads(json_str)
print(parsed["name"])  # ➜ Alice
```

### Good For
* Web APIs (REST)
* Cross-language data exchange
* Fast serialization

---

## YAML – *YAML Ain’t Markup Language*

### Structure

* Indentation-based
* Supports:

  * All JSON types
  * Comments (`#`)
  * References & anchors (`&` and `*`)
  * Multi-line strings
  * Complex mappings

### Example

```yaml
name: Alice
age: 30
married: false
children: null
skills:
  - Python
  - SQL
education:
  degree: MSc
  university: MIT
bio: |
  Alice is a software engineer
  with over 10 years of experience.
```

### Advanced Example (Anchors & Aliases)

```yaml
default: &default
  role: user
  access: read-only

admin:
  <<: *default
  access: full
```

### Python Usage

```python
import yaml

yaml_str = """
name: Alice
skills:
  - Python
  - SQL
"""

data = yaml.safe_load(yaml_str)
print(data["skills"])  # ➜ ['Python', 'SQL']
```

> ⚠️ Install with `pip install pyyaml`

### Good For

* Config files (Docker, Ansible, GitHub Actions, etc.)
* Human-editable settings

## XML – *eXtensible Markup Language*

### Structure

* Tree-like tag structure
* Supports:

  * Attributes (`<tag attr="value">`)
  * Nested elements
  * Mixed content (text + elements)

### Example

```xml
<person>
  <name>Alice</name>
  <age>30</age>
  <skills>
    <skill>Python</skill>
    <skill>SQL</skill>
  </skills>
  <education degree="MSc" university="MIT"/>
</person>
```

### Python Usage

```python
import xml.etree.ElementTree as ET

xml_str = """<person><name>Alice</name><age>30</age></person>"""
root = ET.fromstring(xml_str)
print(root.find("name").text)  # ➜ Alice
```

* For writing:

```python
ET.Element("person")
ET.SubElement(root, "name").text = "Alice"
ET.tostring(root)
```

> Also available: `lxml`, `minidom` for advanced parsing.

### Good For

* Enterprise software
* Interoperability with legacy systems
* Configurations (Android, Maven)

---

## Comparison 

| Feature                | JSON    | YAML         | XML         |
| ---------------------- | ------- | ------------ | ----------- |
| Readability            | ✅ Good  | ✅✅ Excellent | ⚠️ Moderate |
| Verbosity              | ✅ Low   | ✅ Low        | ❌ Very High |
| Comments               | ❌ No    | ✅ Yes        | ✅ Yes       |
| Parsing Speed          | ✅ Fast  | ⚠️ Moderate  | ⚠️ Slower   |
| Schema Validation      | ❌ No    | ✅ (Custom)   | ✅ DTD/XSD   |
| Human Editing          | ⚠️ Okay | ✅ Excellent  | ❌ Poor      |
| Supports Mixed Content | ❌ No    | ❌ No         | ✅ Yes       |
| Nesting                | ✅ Good  | ✅ Good       | ✅ Good      |

---

## What to use?

| Use Case                        | Recommended Format |
| ------------------------------- | ------------------ |
| Web API Response (REST)         | **JSON**           |
| Application Config File         | **YAML**           |
| Document Storage (rich text)    | **XML**            |
| Interfacing with legacy systems | **XML**            |
| Scripting / DevOps pipelines    | **YAML**           |
