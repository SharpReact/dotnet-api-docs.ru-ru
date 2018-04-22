### <a name="httprequestcontentencoding-property-prohibits-utf7"></a><span data-ttu-id="b8b12-101">Свойство HttpRequest.ContentEncoding запрещает кодировку UTF7</span><span class="sxs-lookup"><span data-stu-id="b8b12-101">HttpRequest.ContentEncoding property prohibits UTF7</span></span>

|   |   |
|---|---|
|<span data-ttu-id="b8b12-102">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="b8b12-102">Details</span></span>|<span data-ttu-id="b8b12-103">Начиная с .NET Framework 4.5 кодировка UTF-7 запрещена в теле <xref:System.Web.HttpRequest?displayProperty=name>.</span><span class="sxs-lookup"><span data-stu-id="b8b12-103">Beginning in .NET Framework 4.5, UTF-7 encoding is prohibited in <xref:System.Web.HttpRequest?displayProperty=name>s' bodies.</span></span> <span data-ttu-id="b8b12-104">Данные для приложений, которые зависят от поступающих данных UTF-7, в некоторых случаях декодируются неверно.</span><span class="sxs-lookup"><span data-stu-id="b8b12-104">Data for applications that depend on incoming UTF-7 data will not decode properly in some cases.</span></span>|
|<span data-ttu-id="b8b12-105">Предложение</span><span class="sxs-lookup"><span data-stu-id="b8b12-105">Suggestion</span></span>|<span data-ttu-id="b8b12-106">В идеальном случае приложения необходимо обновить, чтобы они не использовали кодировку UTF-7 в <xref:System.Web.HttpRequest?displayProperty=name>.</span><span class="sxs-lookup"><span data-stu-id="b8b12-106">Ideally, applications should be updated to not use UTF-7 encoding in <xref:System.Web.HttpRequest?displayProperty=name>s.</span></span> <span data-ttu-id="b8b12-107">Кроме того, устаревшее поведение можно восстановить с помощью атрибута <code>aspnet:AllowUtf7RequestContentEncoding</code> элемента [appSettings](https://msdn.microsoft.com/library/hh975440(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="b8b12-107">Alternatively, legacy behavior can be restored by using the <code>aspnet:AllowUtf7RequestContentEncoding</code> attribute of the [appSettings](https://msdn.microsoft.com/library/hh975440(v=vs.110).aspx) element.</span></span>|
|<span data-ttu-id="b8b12-108">Область</span><span class="sxs-lookup"><span data-stu-id="b8b12-108">Scope</span></span>|<span data-ttu-id="b8b12-109">Пограничный случай</span><span class="sxs-lookup"><span data-stu-id="b8b12-109">Edge</span></span>|
|<span data-ttu-id="b8b12-110">Версия</span><span class="sxs-lookup"><span data-stu-id="b8b12-110">Version</span></span>|<span data-ttu-id="b8b12-111">4.5</span><span class="sxs-lookup"><span data-stu-id="b8b12-111">4.5</span></span>|
|<span data-ttu-id="b8b12-112">Тип</span><span class="sxs-lookup"><span data-stu-id="b8b12-112">Type</span></span>|<span data-ttu-id="b8b12-113">Среда выполнения</span><span class="sxs-lookup"><span data-stu-id="b8b12-113">Runtime</span></span>|
|<span data-ttu-id="b8b12-114">Затронутые API</span><span class="sxs-lookup"><span data-stu-id="b8b12-114">Affected APIs</span></span>|<ul><li><xref:System.Web.HttpRequest.ContentEncoding?displayProperty=nameWithType></li></ul>|
