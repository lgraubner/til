# Escape @ in parameters

To use "@" in the `parameters.yml` file it has to be escaped by prepending it with another "@".

```yaml
parameters:
    jwt_key_pass_phrase: "@@thisisakey"
```