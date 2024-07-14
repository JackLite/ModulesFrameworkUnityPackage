v1.3.0:
- new types of systems ISubscriptionInitSystem<T> and ISubscriptionActivateSystem<T>;
- MF.World is static property that returns main world;
- custom id for entities, based on indices feature;

v1.2.3:
- fix autostart stripping;

v1.2.2:
- fix collection drawers;

v1.2.1:
- fix drawer for null;
- fix destroying debug view of OneData/Entity from OnTrigger/OnCollider, animation events, etc.

v1.2.0:
- Entity.IsEmpty() and DataWorld.IsEmptyEntity(int eid) to check if there is any component that binds to entity;
- new API for keys (aka indices);
- new unity debug using UIToolkit;
- increase speed of Query.GetEntities();
- add DataWorld.OneDataGeneration<T>() and DataWorld.ReplaceOneData<T>() methods;

v1.1.5:
- fix drawing of const fields in unity inspector

v1.1.4:
- add MFHooks extension for immediate events;
- add MFEntityFilter extension for checking entity like a query;

v1.1.3:
- add ability to create custom index for components that dramatically increase speed of finding components and entity by custom index;

v1.1.2:
- Query.Where<T>() no check if T exists in table;

v1.1.1:
- fix bug with recuse removing of submodules;

v1.1.0:
- add filter for Or operations in query;

v1.0.10:
- fix bug with quaternions in debug;

v1.0.9:
- fix bug when one data viewer created after play mode stopped;

v1.0.8:
- free entity id now storages in queue instead of stack;
- fix some errors in unity adapter;

v1.0.7:
- exception in one system now will not prevent other systems from executing;

v1.0.6:
- fix some adapter issues;

v1.0.5:
- check if entity viewer already created in unity adapter;

v1.0.4:
- fix inject of EcsOneData<T> in fields of systems;

v1.0.3:
- fix GetComponents<T> in complex queries;

v1.0.2:
- fix inspector for OneData;

v1.0.1:
- remove auto apply for changes for now;
- fix applying changes;
- add sorting for components in inspector;
- add sorting for one data in hierarchy;

v1.0.0:
- Add check if one data exists
- Now you can change data in inspector

v0.9.1:
- Fix removing multiple components in foreach. Now you should use iterator for this

v0.9.0:
- Multiple components added
- Multiple worlds added
- Several critical bugs fixed

v0.8.1:
- Fix activating module when it's already active;
- GetModule<T> now can't return null, but throw exception if module not found;

v0.8.0:
- Add submodules to core
- Add submodules debug
- Improvements of custom drawers

v0.7.0:
- Add global systems. They work always and can't have dependency but DataWorld;

v0.6.6:
- Add debug for modules
- Remove warning when type not implemented for debug

v0.6.5:
- Add performance log and settings for it

v0.6.4:
- Fix bug with multiple event systems
- improvements for modules control

v0.6.3:
- bool Entity.IsAlive() method. It can be usefull when you store the entity and wants to check that it is still alive and this id was not reused

v0.6.2:
- OnActivate and OnDeactivate calls now after events systems registered, so it calls after module really fully activated/deactivated

v0.6.1:
- Add settings for choose start method and log filter;
- Add support for custom types in debug;
- Add EntryPoint component for start MF by GameObject in concrete scene;
- Some minor improvements;

v0.6.0:
- Add IModulesLogger and UnityLogger. You can use your own logger if need;
- Add DataWorld.GetRawData<T>() for fast iterations;
- Add Query.GetComponents<T> so you can iterate components in query without get them from entity or world;
- Several minor fixes and improvements;

v0.5.2:
- Fix using multiple queries with common main table;

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