### <a name="xmltextreader-dtd-entity-expansion-is-limited-to-10000000-characters"></a><span data-ttu-id="94370-101">Развертывание сущностей DTD XmlTextReader не может превышать 10 000 000 символов</span><span class="sxs-lookup"><span data-stu-id="94370-101">XmlTextReader DTD entity expansion is limited to 10,000,000 characters</span></span>

|   |   |
|---|---|
|<span data-ttu-id="94370-102">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="94370-102">Details</span></span>|<span data-ttu-id="94370-103">Развертывание сущностей DTD теперь не может превышать 10 000 000 символов.</span><span class="sxs-lookup"><span data-stu-id="94370-103">DTD entity expansion is now limited to 10,000,000 characters.</span></span> <span data-ttu-id="94370-104">Загрузка XML-файлов без развертывания сущностей DTD или с ограниченным развертыванием сущностей DTD не изменяется.</span><span class="sxs-lookup"><span data-stu-id="94370-104">Loading XML files without DTD entity expansion or with limited DTD entity expansion is unaffected.</span></span> <span data-ttu-id="94370-105">Файлы с сущностями DTD, которые развертываются до более чем 10 000 000 символов, не загружаются и теперь вызывают исключение.</span><span class="sxs-lookup"><span data-stu-id="94370-105">Files with DTD entities that expand to more than 10,000,000 characters fail to load, and now throw an exception.</span></span>|
|<span data-ttu-id="94370-106">Предложение</span><span class="sxs-lookup"><span data-stu-id="94370-106">Suggestion</span></span>|<span data-ttu-id="94370-107">Если ограничение развертывания сущностей DTD существенно ниже 10 000 000, значение может быть переопределено с помощью свойства <xref:System.Xml.XmlReaderSettings.MaxCharactersFromEntities>.</span><span class="sxs-lookup"><span data-stu-id="94370-107">If the limit of DTD entity expansion is too low 10,000,000, the value can be overridden with the <xref:System.Xml.XmlReaderSettings.MaxCharactersFromEntities> property.</span></span> <span data-ttu-id="94370-108"><xref:System.Xml.XmlReaderSettings?displayProperty=name> с соответствующим значением <xref:System.Xml.XmlReaderSettings.MaxCharactersFromEntities?displayProperty=name> может передаваться в <code>XmlReader.Create</code>, который принимает <xref:System.Xml.XmlReaderSettings?displayProperty=name> (т. е. <xref:System.Xml.XmlReader.Create(System.String,System.Xml.XmlReaderSettings)>)</span><span class="sxs-lookup"><span data-stu-id="94370-108">An <xref:System.Xml.XmlReaderSettings?displayProperty=name> with the proper <xref:System.Xml.XmlReaderSettings.MaxCharactersFromEntities?displayProperty=name> value can be passed to <code>XmlReader.Create</code> that takes <xref:System.Xml.XmlReaderSettings?displayProperty=name> (ie. <xref:System.Xml.XmlReader.Create(System.String,System.Xml.XmlReaderSettings)>)</span></span>|
|<span data-ttu-id="94370-109">Область</span><span class="sxs-lookup"><span data-stu-id="94370-109">Scope</span></span>|<span data-ttu-id="94370-110">Пограничный случай</span><span class="sxs-lookup"><span data-stu-id="94370-110">Edge</span></span>|
|<span data-ttu-id="94370-111">Версия</span><span class="sxs-lookup"><span data-stu-id="94370-111">Version</span></span>|<span data-ttu-id="94370-112">4.5</span><span class="sxs-lookup"><span data-stu-id="94370-112">4.5</span></span>|
|<span data-ttu-id="94370-113">Тип</span><span class="sxs-lookup"><span data-stu-id="94370-113">Type</span></span>|<span data-ttu-id="94370-114">Среда выполнения</span><span class="sxs-lookup"><span data-stu-id="94370-114">Runtime</span></span>|
|<span data-ttu-id="94370-115">Затронутые API</span><span class="sxs-lookup"><span data-stu-id="94370-115">Affected APIs</span></span>|<ul><li><xref:System.Xml.XmlTextReader?displayProperty=nameWithType></li><li><xref:System.Xml.XmlTextReader.%23ctor?displayProperty=nameWithType></li><li><xref:System.Xml.XmlTextReader.%23ctor(System.IO.Stream)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlTextReader.%23ctor(System.IO.Stream,System.Xml.XmlNameTable)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlTextReader.%23ctor(System.IO.Stream,System.Xml.XmlNodeType,System.Xml.XmlParserContext)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlTextReader.%23ctor(System.IO.TextReader)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlTextReader.%23ctor(System.IO.TextReader,System.Xml.XmlNameTable)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlTextReader.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlTextReader.%23ctor(System.String,System.IO.Stream)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlTextReader.%23ctor(System.String,System.IO.Stream,System.Xml.XmlNameTable)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlTextReader.%23ctor(System.String,System.IO.TextReader)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlTextReader.%23ctor(System.String,System.IO.TextReader,System.Xml.XmlNameTable)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlTextReader.%23ctor(System.String,System.Xml.XmlNameTable)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlTextReader.%23ctor(System.String,System.Xml.XmlNodeType,System.Xml.XmlParserContext)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlTextReader.%23ctor(System.Xml.XmlNameTable)?displayProperty=nameWithType></li></ul>|
