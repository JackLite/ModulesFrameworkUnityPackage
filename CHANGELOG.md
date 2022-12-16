v0.3.0:
- New method bool Entity.HasComponent<T>();
- New method int Query.Count();
- Query is class now;
- InitModule and other methods that control state of module work immediately now;
- Add bool arg for InitModule to Activate after initialization;
- Method ActivateModule throw excepyion now if module was not initialized;
- EcsModule now has protected field with DataWorld.