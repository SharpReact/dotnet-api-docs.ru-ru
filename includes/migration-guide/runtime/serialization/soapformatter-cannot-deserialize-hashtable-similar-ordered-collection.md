### <a name="soapformatter-cannot-deserialize-hashtable-and-similar-ordered-collection-objects"></a><span data-ttu-id="14cba-101">Классу SoapFormatter не удается выполнить десериализацию хэш-таблицы и подобных упорядоченных объектов коллекции</span><span class="sxs-lookup"><span data-stu-id="14cba-101">SoapFormatter cannot deserialize Hashtable and similar ordered collection objects</span></span>

|   |   |
|---|---|
|<span data-ttu-id="14cba-102">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="14cba-102">Details</span></span>|<span data-ttu-id="14cba-103">Класс <xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name> не гарантирует, что объекты, сериализованные в одной версии .NET Framework, будут успешно десериализованы в другой версии платформы.</span><span class="sxs-lookup"><span data-stu-id="14cba-103">The <xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name> does not guarantee that objects serialized under one .NET Framework version will successfully deserialize under a different version.</span></span> <span data-ttu-id="14cba-104">В частности, в некоторые упорядоченные коллекции (например, <xref:System.Collections.Hashtable?displayProperty=name>) добавлены элементы в версиях с 4.0 по 4.5, поэтому объекты этих типов не могут быть десериализованы в .NET 4.0, если бы они были сериализованы в .NET 4.5.</span><span class="sxs-lookup"><span data-stu-id="14cba-104">Specifically, some ordered collections (like <xref:System.Collections.Hashtable?displayProperty=name>) added members between 4.0 and 4.5 such that objects of these types cannot deserialize with .NET 4.0 if they were serialized with .NET 4.5.</span></span> <span data-ttu-id="14cba-105">Обратите внимание, что если сериализованные данные сериализуются и десериализуются в одной версии .NET Framework, проблемы не возникают.</span><span class="sxs-lookup"><span data-stu-id="14cba-105">Note that if the serialized data is both serialized and deserialized with the same .NET Framework version, no issue will occur.</span></span>|
|<span data-ttu-id="14cba-106">Предложение</span><span class="sxs-lookup"><span data-stu-id="14cba-106">Suggestion</span></span>|<span data-ttu-id="14cba-107">Чтобы обеспечить поддержку изменений в .NET Framework, сериализацию <xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name> следует заменить на сериализацию <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> или <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>.</span><span class="sxs-lookup"><span data-stu-id="14cba-107"><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name> serialization should be replaced with <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> serialization or <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> to be resilient to .NET Framework changes.</span></span>|
|<span data-ttu-id="14cba-108">Область</span><span class="sxs-lookup"><span data-stu-id="14cba-108">Scope</span></span>|<span data-ttu-id="14cba-109">Дополнительный номер</span><span class="sxs-lookup"><span data-stu-id="14cba-109">Minor</span></span>|
|<span data-ttu-id="14cba-110">Версия</span><span class="sxs-lookup"><span data-stu-id="14cba-110">Version</span></span>|<span data-ttu-id="14cba-111">4.5</span><span class="sxs-lookup"><span data-stu-id="14cba-111">4.5</span></span>|
|<span data-ttu-id="14cba-112">Тип</span><span class="sxs-lookup"><span data-stu-id="14cba-112">Type</span></span>|<span data-ttu-id="14cba-113">Среда выполнения</span><span class="sxs-lookup"><span data-stu-id="14cba-113">Runtime</span></span>|
|<span data-ttu-id="14cba-114">Затронутые API</span><span class="sxs-lookup"><span data-stu-id="14cba-114">Affected APIs</span></span>|<ul><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object,System.Runtime.Remoting.Messaging.Header[])?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream,System.Runtime.Remoting.Messaging.HeaderHandler)?displayProperty=nameWithType></li></ul>|
