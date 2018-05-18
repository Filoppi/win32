# [WPD Automation Object Model](wpd-automation-object-model.md)
## [About the WPD Automation Object Model](about-the-wpd-automation-object-model.md)
### [Using WPD Automation](using-wpd-automation.md)
### [About the Device Object](about-the-device-object.md)
### [About the servicesCollection and storagesCollection Objects](about-the-servicescollection-and-storagescollection-objects.md)
### [About the WPDobject](about-the-wpdobject-.md)
### [About the Service Object](about-the-service-object.md)
### [About the Storage Object](about-the-storage-object.md)
### [About the childrenCollection Object](about-the-childrencollection-object.md)
### [About the Creation Container Object](about-the-creation-container-object.md)
### [About the Resource Object](about-the-resource-object.md)
## [WPD Automation Programming Guide](wpd-automation-programming-guide.md)
### [Best Practices for Writing WPD Automation Scripts](best-practices-for-writing-wpd-automation-scripts.md)
#### [WPDDeviceInspector Automation Profiles](wpddeviceinspector-automation-profiles.md)
#### [Error and Exception Handling](error-and-exception-handling.md)
#### [Instantiating the WPD Automation Factory Interface](instantiating-the-wpd-automation-factory-interface.md)
### [Enumerating Services and Storages](enumerating-services-and-storages.md)
### [Enumerating the Content of a Service or a Storage](enumerating-the-content-of-a-service-or-a-storage.md)
### [Creating and Deleting Objects](creating-and-deleting-objects.md)
### [Assigning and Getting Object Properties](assigning-and-getting-object-properties.md)
### [Reading and Writing Resource Data](reading-and-writing-resource-data.md)
#### [Synchronous Reading and Writing](synchronous-reading-and-writing.md)
#### [Asynchronous Functions](asynchronous-functions.md)
### [Invoking a Service-Defined Method](invoking-a-service-defined-method.md)
### [Handling Service-Defined Events](handling-service-defined-events.md)
## [WPD Automation Reference](wpd-automation-reference.md)
### [childrenCollection Object](childrencollection-object.md)
#### [Count Property](childrencollection-count.md)
### [Creation Container Object](creation-container-object.md)
#### [Data Property](createcontainerobject-data.md)
#### [ServiceProperty Property](createcontainerobject-serviceproperty.md)
#### [WpdProperty Property](createcontainerobject-wpdproperty.md)
#### [onTransferProgress Event](createcontainerobject-ontransferprogress.md)
### [Device Object](device-object.md)
#### [GetServicesByType Method](device-getservicesbytype.md)
#### [Services Property](device-services.md)
#### [Storages Property](device-storages.md)
#### [WpdProperty Property](device-wpdproperty.md)
#### [onDeviceReset Event](ondevicereset.md)
#### [onDeviceUpdated Event](ondeviceupdated.md)
### [Resource Object](resource-object.md)
#### [Format Property](resource-format.md)
#### [IsReadOnly Property](resource-isreadonly.md)
#### [Size Property](resource-size.md)
#### [Stream Property](resource-stream.md)
#### [onTransferProgress Event](ontransferprogress.md)
### [Service Object](service-object.md)
#### [AddChild Method](service-addchild.md)
#### [CreateNewObject Method](service-createnewobject.md)
#### [GetChildrenByFormat Method](service-getchildrenbyformat.md)
#### [Method Method](service-method.md)
#### [RemoveChild Method](service-removechild.md)
#### [AbstractServices Property](service-abstractservices.md)
#### [Children Property](service-children.md)
#### [ServiceProperty Property](service-serviceproperty.md)
#### [WpdProperty Property](service-wpdproperty.md)
#### [onAddChildComplete Event](service-onaddchildcomplete.md)
#### [onGetChildrenByFormatComplete Event](service-ongetchildrenbyformatcomplete.md)
#### [onMethodComplete Event](service-onmethodcomplete.md)
#### [onObjectAdded Event](onobjectadded.md)
#### [onObjectRemoved Event](onobjectremoved.md)
#### [onObjectUpdated Event](onobjectupdated.md)
#### [onRemoveChildComplete Event](service-onremovechildcomplete.md)
#### [onServiceEventName Event](onserviceeventname.md)
### [servicesCollection Object](servicescollection-object.md)
#### [Count Property](servicescollection-count.md)
### [Storage Object](storage-object.md)
#### [AddChild Method](storage-addchild.md)
#### [CreateNewObject Method](storage-createnewobject.md)
#### [GetChildrenByFormat Method](storage-getchildrenbyformat.md)
#### [RemoveChild Method](storage-removechild.md)
#### [Children Property](storage-children.md)
#### [WpdProperty Property](storage-wpdproperty.md)
#### [onAddChildComplete Event](storage-onaddchildcomplete.md)
#### [onGetChildrenByFormatComplete Event](storage-ongetchildrenbyformatcomplete.md)
#### [onObjectAdded Event](storage-onobjectadded.md)
#### [onObjectRemoved Event](storage-onobjectremoved.md)
#### [onObjectUpdated Event](storage-onobjectupdated.md)
#### [onRemoveChildComplete Event](storage-onremovechildcomplete.md)
### [storagesCollection Object](storagescollection-object.md)
#### [Count Property](storagescollection-count.md)
### [WPDObject](wpdobject.md)
#### [AddChild method](wpdobject-addchild.md)
#### [GetChildrenByFormat method](wpdobject-getchildrenbyformat.md)
#### [RemoveChild method](wpdobject-removechild.md)
#### [Children property](wpdobject-children.md)
#### [Parent property](wpdobject-parent.md)
#### [Resource property](wpdobject-resource.md)
#### [Service property](wpdobject-service.md)
#### [ServiceProperty property](wpdobject-serviceproperty.md)
#### [Storage property](wpdobject-storage.md)
#### [WpdProperty property](wpdobject-wpdproperty.md)
#### [onAddChildComplete event](onaddchildcomplete.md)
#### [onRemoveChildComplete event](onremovechildcomplete.md)
### [Names for WPD GUIDs](names-for-wpd-guids.md)
### [Names for WPD PROPERTYKEYs](names-for-wpd-propertykeys.md)
### [IPortableDeviceDispatchFactory](/windows/win32/content/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedispatchfactory?branch=dev)
#### [GetDeviceDispatch method](/windows/win32/content/PortableDeviceApi/nf-portabledeviceapi-iportabledevicedispatchfactory-getdevicedispatch?branch=dev)
### [IPortableDeviceWebControl](/windows/win32/content/portabledeviceapi/nn-portabledeviceapi-iportabledevicewebcontrol?branch=dev)
#### [GetDeviceFromId method](/windows/win32/content/portabledeviceapi/nf-portabledeviceapi-iportabledevicewebcontrol-getdevicefromid?branch=dev)
#### [GetDeviceFromIdAsync method](/windows/win32/content/portabledeviceapi/nf-portabledeviceapi-iportabledevicewebcontrol-getdevicefromidasync?branch=dev)
