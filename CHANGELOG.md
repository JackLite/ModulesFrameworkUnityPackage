v0.2.0:
- Fix namespaces;
- Add IActivate and IDeactivate system. They works before EcsModule activated/deactivated;
- Аdd OnActivate and OnDeactivate methods in EcsModule;
- Add DataWorld.IsModuleActive<TModule> for check if module is active.