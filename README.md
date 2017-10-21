# gst-json

GNU Smalltalk JSON Encoder/Decoder Implementation

## Usage

### Decode

```st
'{"foo": 42, "bar": [{"baz": true}]}' readStream nextJSON
```

### Encode

```st
{'foo'. 42. 'baz'. true} asJSON
```

----

## Library Pollution

### Encode

```st
OrderedCollection#removeLast:
ReadStream#nextJSON
ReadStream#nextJSONCharacterToken
ReadStream#nextJSONEscapedCharacterToken
ReadStream#nextJSONStringToken
```

### Decode

```st
Boolean#printJSONOn:
Character#printJSONOn:
CharacterArray#printJSONOn:
Dictionary#printJSONOn:
Float#printJSONOn:
Integer#printJSONOn:
Number#printJSONOn:
Object#asJSON
Object#printJSONOn:
SequenceableCollection#printJSONOn:
UndefinedObject#printJSONOn:
```

----

## License

BSD 2-Clause
