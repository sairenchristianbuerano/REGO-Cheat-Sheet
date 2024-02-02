REGO is a declarative language used for policy-as-code in the Open Policy Agent (OPA) framework. Here's a concise cheat sheet of popular built-in functions, syntax idioms, and variables in REGO:

1. Built-in functions:

- Comparison: `eq(x, y)`, `lt(x, y)`, `lte(x, y)`, `gt(x, y)`, `gte(x, y)`
- Arithmetic: `add(x, y)`, `sub(x, y)`, `mul(x, y)`, `div(x, y)`, `mod(x, y)`
- Logical: `and(x, y)`, `or(x, y)`, `not(x)`
- Type Checking: `is_number(x)`, `is_string(x)`, `is_boolean(x)`, `is_array(x)`, `is_set(x)`, `is_object(x)`, `is_null(x)`
- Casting: `to_number(x)`, `to_string(x)`, `to_boolean(x)`
- Arrays: `count(arr)`, `all(arr, func)`, `any(arr, func)`, `filter(arr, func)`, `map(arr, func)`, `reduce(arr, func, initial)`
- Sets: `intersection(set1, set2)`, `union(set1, set2)`, `diff(set1, set2)`
- Objects: `object.get(obj, key, default)`, `keys(obj)`, `values(obj)`, `merge(obj1, obj2)`
- Strings: `concat(sep, arr)`, `format_int(x, base)`, `sprintf(format, values)`, `split(str, sep)`, `trim(str, chars)`, `replace(str, old, new)`, `startswith(str, prefix)`, `endswith(str, suffix)`, `contains(str, substr)`
- Regex: `re_match(pattern, str)`, `re_find_n(pattern, str, n)`, `re_split(pattern, str, n)`, `re_replace(pattern, str, replace)`
- Encoding: `base64.encode(str)`, `base64.decode(str)`, `base64url.encode(str)`, `base64url.decode(str)`, `hex.encode(str)`, `hex.decode(str)`, `json.marshal(v)`, `json.unmarshal(str)`, `yaml.marshal(v)`, `yaml.unmarshal(str)`

2. Syntax idioms:

- Rules: `default rule_name = value`, `rule_name[output] { conditions }`
- Packages: `package pkg_name`
- Imports: `import path.to.module`
- Functions: `function_name(args) = output { conditions }`
- Variables: `x := expression`
- Conditionals: `x = expression1; x = expression2 { conditions }`
- Iteration: `some i; x := arr[i]`
- Existential quantification: `some variable { conditions }`
- Universal quantification: `not any_variable { not conditions }`
- Inline expressions: `[expression | variable <- iterable]`
- Sets: `{expression | variable <- iterable}`

3. Variables:

- Input data: `input`
- Data from other documents: `data`

Remember that REGO is a flexible and powerful language, so there might be other functions, idioms, or variables not listed here. However, this cheat sheet should give you a good starting point for working with REGO and OPA.
