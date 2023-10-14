# Serialization

**serialization**: the process of turning an object in memory into a stream of bytes so that we can store it on disk or send it over the network

**deserialization**: the reverse process which turns a stream of bytes into an object in memory

**Notes**:

1. Developers just need to implement the `Serializable` interface without writing any extra code (Java handles serialization internally);

2. `static` and `transient` variables cannot be serialized.