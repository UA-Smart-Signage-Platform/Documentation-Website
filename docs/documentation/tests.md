## Tests

In this project, two major types of tests were conducted: Unit Tests and Integration Tests.

### Unitary Tests

To run the unitary tests we can use the following commands:

```
mvn clean test
```

### Integration Tests

To run the integration:

- First, make sure the docker application is running in your system.
- Then you can run the following command:
```
mvn clean verify failsafe:integration-test
```

