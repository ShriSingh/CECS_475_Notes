Methods used to liberate the unmanaged resources kept by an object:

| Features             | Dispose() Method                                                                                | Finalize() Method                                                                       |
| -------------------- | ----------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| **Defined**          | Defined in the IDisposable interface                                                            | Defined in java.lang.object class                                                       |
| **Basic**            | Used to close or release unmanaged resources stored by an object, like files or streams         | Used to clear up unmanaged resources owned by the current object before it is destroyed |
| **Syntax**           | `public void Dispose() { // Dispose code here }`                                                | `protected void finalize() { // Finalization code here }`                               |
| **Access Specifier** | Declared as `public`                                                                            | Declared as `private`                                                                   |
| **Invoked**          | Invoked by the user                                                                             | Invoked by the garbage collector(GC)                                                    |
| **Speed**            | Invoked very quickly                                                                            | Invoked slower than `Dispose()` method                                                  |
| **Performance**      | - Executes immediate action<br>- No impact on the performance of the site                       | Has an impact on the performance of the site                                            |
| **Implementation**   | Every time whenever there is a `close()` function, the `dispose()` method should be implemented | Unmanaged resources must be implemented using the `finalize()` method                   |
