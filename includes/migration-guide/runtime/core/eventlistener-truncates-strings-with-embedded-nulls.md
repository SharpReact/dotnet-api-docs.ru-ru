### <a name="eventlistener-truncates-strings-with-embedded-nulls"></a><span data-ttu-id="bad01-101">EventListener усекает строки с внедренными значениями NULL</span><span class="sxs-lookup"><span data-stu-id="bad01-101">EventListener truncates strings with embedded nulls</span></span>

|   |   |
|---|---|
|<span data-ttu-id="bad01-102">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="bad01-102">Details</span></span>|<span data-ttu-id="bad01-103"><xref:System.Diagnostics.Tracing.EventListener?displayProperty=name> усекает строки с внедренными значениями NULL.</span><span class="sxs-lookup"><span data-stu-id="bad01-103"><xref:System.Diagnostics.Tracing.EventListener?displayProperty=name> truncates strings with embedded nulls.</span></span> <span data-ttu-id="bad01-104">Символы NULL не поддерживаются классом <xref:System.Diagnostics.Tracing.EventSource?displayProperty=name>.</span><span class="sxs-lookup"><span data-stu-id="bad01-104">Null characters are not supported by the <xref:System.Diagnostics.Tracing.EventSource?displayProperty=name> class.</span></span> <span data-ttu-id="bad01-105">Изменение влияет только на приложения, использующие <xref:System.Diagnostics.Tracing.EventListener?displayProperty=name> для чтения данных <xref:System.Diagnostics.Tracing.EventSource?displayProperty=name> в процессе и значения NULL в качестве разделителей.</span><span class="sxs-lookup"><span data-stu-id="bad01-105">The change only affects apps that use <xref:System.Diagnostics.Tracing.EventListener?displayProperty=name> to read <xref:System.Diagnostics.Tracing.EventSource?displayProperty=name> data in process and that use null characters as delimiters.</span></span>|
|<span data-ttu-id="bad01-106">Предложение</span><span class="sxs-lookup"><span data-stu-id="bad01-106">Suggestion</span></span>|<span data-ttu-id="bad01-107">Если возможно, следует обновить данные <xref:System.Diagnostics.Tracing.EventSource?displayProperty=name>, чтобы не использовать внедренные символы NULL.</span><span class="sxs-lookup"><span data-stu-id="bad01-107"><xref:System.Diagnostics.Tracing.EventSource?displayProperty=name> data should be updated, if possible, to not use embedded null characters.</span></span>|
|<span data-ttu-id="bad01-108">Область</span><span class="sxs-lookup"><span data-stu-id="bad01-108">Scope</span></span>|<span data-ttu-id="bad01-109">Пограничный случай</span><span class="sxs-lookup"><span data-stu-id="bad01-109">Edge</span></span>|
|<span data-ttu-id="bad01-110">Версия</span><span class="sxs-lookup"><span data-stu-id="bad01-110">Version</span></span>|<span data-ttu-id="bad01-111">4.5.1</span><span class="sxs-lookup"><span data-stu-id="bad01-111">4.5.1</span></span>|
|<span data-ttu-id="bad01-112">Тип</span><span class="sxs-lookup"><span data-stu-id="bad01-112">Type</span></span>|<span data-ttu-id="bad01-113">Среда выполнения</span><span class="sxs-lookup"><span data-stu-id="bad01-113">Runtime</span></span>|
|<span data-ttu-id="bad01-114">Затронутые API</span><span class="sxs-lookup"><span data-stu-id="bad01-114">Affected APIs</span></span>|<ul><li><xref:System.Diagnostics.Tracing.EventListener.%23ctor?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel,System.Diagnostics.Tracing.EventKeywords)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel,System.Diagnostics.Tracing.EventKeywords,System.Collections.Generic.IDictionary{System.String,System.String})?displayProperty=nameWithType></li></ul>|
