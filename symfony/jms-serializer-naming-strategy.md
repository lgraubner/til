# JMS Serializer naming strategy

It's easily possible to switch the naming strategy of properties with JMS Serializer. That means you can for example switch between snake case and camel case with a single line of code.

Simple add the following to your `parameters.yml` to use camel case:

```yaml
parameters:
    jms_serializer.camel_case_naming_strategy.class: JMS\Serializer\Naming\IdenticalPropertyNamingStrategy
```