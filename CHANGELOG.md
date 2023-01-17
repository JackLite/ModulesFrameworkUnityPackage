v0.5.1:
- Add Query.SelectFirstEntity and Query.TrySelectFirstEntity;
- Fix Query.Count with multiple With, Without and Where;

v0.5.0:
- Add event systems;
- Add GetEcsTable<T> for fast iterations;
- Add GetDependency<T> for third-party IoC;

v0.4.6:
- Query now IDisposable for zero-allocations;
- Add SelectFirst<TRet> in Query;
- Update documentation;

v0.4.5:
- Fix editor scripts

v0.4.4:
- Add support nested structs

v0.4.3:
- Fix recreating one data
- Add generation for one data

v0.4.2:
- Fix support string in debug
- Improvement of one data

v0.4.1:
- Fix support GameObject in debug

v0.4.0:
- EcsOneData now lives in DataWorld. You still can get them by private fields in your system. But you should use DataWorld.GetOneData<T>() in future.
- First iteration of debug for Unity Engine. You can see all created Entities with all Components. It shows simple types (including Enum), IEnumerable and IDictionary collections, VectorX, Quaternion (euler angles) and Unity Objects (like GameObject and MonoBehaviour)

v0.3.0:
- New method bool Entity.HasComponent<T>();
- New method int Query.Count();
- Query is class now;
- InitModule and other methods that control state of module work immediately now;
- Add bool arg for InitModule to Activate after initialization;
- Method ActivateModule throw excepyion now if module was not initialized;
- EcsModule now has protected field with DataWorld.

v0.2.2:
- Fix IndexOutOfRangeException when remove entity
- Fix IndexOutOfRangeException when size of tables increase fast

v0.2.0:
- Fix namespaces;
- Add IActivate and IDeactivate system. They works before EcsModule activated/deactivated;
- Аdd OnActivate and OnDeactivate methods in EcsModule;
- Add DataWorld.IsModuleActive for check if module is active.