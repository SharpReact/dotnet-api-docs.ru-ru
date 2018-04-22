### <a name="a-concurrentdictionary-serialized-in-net-45-with-netdatacontractserializer-cannot-be-deserialized-by-net-451-or-452"></a><span data-ttu-id="40720-101">Объект ConcurrentDictionary, сериализованный в .NET 4.5 с помощью NetDataContractSerializer, нельзя десериализовать в .NET 4.5.1 или 4.5.2</span><span class="sxs-lookup"><span data-stu-id="40720-101">A ConcurrentDictionary serialized in .NET 4.5 with NetDataContractSerializer cannot be deserialized by .NET 4.5.1 or 4.5.2</span></span>

|   |   |
|---|---|
|<span data-ttu-id="40720-102">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="40720-102">Details</span></span>|<span data-ttu-id="40720-103">Из-за внутренних изменений типа объекты <xref:System.Collections.Concurrent.ConcurrentDictionary%602>, сериализованные в .NET Framework 4.5 с помощью <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>, не могут быть десериализованы в .NET Framework 4.5.1 или .NET Framework 4.5.2. Обратите внимание, что сериализация в .NET Framework 4.5.x с последующей десериализацией в .NET Framework 4.5 будет работать нормально.</span><span class="sxs-lookup"><span data-stu-id="40720-103">Due to internal changes to the type, <xref:System.Collections.Concurrent.ConcurrentDictionary%602> objects that are serialized with the .NET Framework 4.5 using the <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> cannot be deserialized in the .NET Framework 4.5.1 or in the .NET Framework 4.5.2.Note that moving in the other direction (serializing with the .NET Framework 4.5.x and deserializing with the .NET Framework 4.5) works.</span></span> <span data-ttu-id="40720-104">Аналогичным образом, сериализация в версиях 4.x работает в .NET Framework 4.6. Сериализация и десериализация в одной версии платформы .NET Framework не затрагивается.</span><span class="sxs-lookup"><span data-stu-id="40720-104">Similarly, all 4.x cross-version serialization works with the .NET Framework 4.6.Serializing and deserializing with a single version of the .NET Framework is not affected.</span></span>|
|<span data-ttu-id="40720-105">Предложение</span><span class="sxs-lookup"><span data-stu-id="40720-105">Suggestion</span></span>|<span data-ttu-id="40720-106">Если требуется выполнить сериализацию и десериализацию объектов <xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> между версиями .NET Framework 4.5 и .NET Framework 4.5.1/4.5.2, следует использовать альтернативный сериализатор, например <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name> или <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name>, вместо <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>. Кроме того, поскольку эта проблема была устранена в .NET Framework 4.6, она может быть решена путем обновления до этой версии платформы .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="40720-106">If it is necessary to serialize and deserialize a <xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> between the .NET Framework 4.5 and .NET Framework 4.5.1/4.5.2, an alternate serializer like the <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name> or <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> serializer should be used instead of the <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>.Alternatively, because this issue is addressed in the .NET Framework 4.6, it may be solved by upgrading to that version of the .NET Framework.</span></span>|
|<span data-ttu-id="40720-107">Область</span><span class="sxs-lookup"><span data-stu-id="40720-107">Scope</span></span>|<span data-ttu-id="40720-108">Дополнительный номер</span><span class="sxs-lookup"><span data-stu-id="40720-108">Minor</span></span>|
|<span data-ttu-id="40720-109">Версия</span><span class="sxs-lookup"><span data-stu-id="40720-109">Version</span></span>|<span data-ttu-id="40720-110">4.5.1</span><span class="sxs-lookup"><span data-stu-id="40720-110">4.5.1</span></span>|
|<span data-ttu-id="40720-111">Тип</span><span class="sxs-lookup"><span data-stu-id="40720-111">Type</span></span>|<span data-ttu-id="40720-112">Среда выполнения</span><span class="sxs-lookup"><span data-stu-id="40720-112">Runtime</span></span>|
