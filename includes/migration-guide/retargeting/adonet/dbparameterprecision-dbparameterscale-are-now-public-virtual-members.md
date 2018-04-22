### <a name="dbparameterprecision-and-dbparameterscale-are-now-public-virtual-members"></a><span data-ttu-id="25b23-101">DbParameter.Precision и DbParameter.Scale теперь являются открытыми виртуальными членами</span><span class="sxs-lookup"><span data-stu-id="25b23-101">DbParameter.Precision and DbParameter.Scale are now public virtual members</span></span>

|   |   |
|---|---|
|<span data-ttu-id="25b23-102">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="25b23-102">Details</span></span>|<span data-ttu-id="25b23-103"><xref:System.Data.Common.DbParameter.Precision> и <xref:System.Data.Common.DbParameter.Scale> реализованы как открытые виртуальные свойства.</span><span class="sxs-lookup"><span data-stu-id="25b23-103"><xref:System.Data.Common.DbParameter.Precision> and <xref:System.Data.Common.DbParameter.Scale> are implemented as public virtual properties.</span></span> <span data-ttu-id="25b23-104">Они заменяют соответствующие явные реализации интерфейса: <xref:System.Data.Common.DbParameter.System%23Data%23IDbDataParameter%23Precision> и <xref:System.Data.Common.DbParameter.System%23Data%23IDbDataParameter%23Scale>.</span><span class="sxs-lookup"><span data-stu-id="25b23-104">They replace the corresponding explicit interface implementations, <xref:System.Data.Common.DbParameter.System%23Data%23IDbDataParameter%23Precision> and <xref:System.Data.Common.DbParameter.System%23Data%23IDbDataParameter%23Scale>.</span></span>|
|<span data-ttu-id="25b23-105">Предложение</span><span class="sxs-lookup"><span data-stu-id="25b23-105">Suggestion</span></span>|<span data-ttu-id="25b23-106">При повторном создании поставщика базы данных ADO.NET эти различия потребуют применения ключевого слова override к свойствам Precision и Scale.</span><span class="sxs-lookup"><span data-stu-id="25b23-106">When re-building an ADO.NET database provider, these differences will require the 'override' keyword to be applied to the Precision and Scale properties.</span></span> <span data-ttu-id="25b23-107">Это требуется только в случае повторного создания компонентов; существующие двоичные файлы будут продолжать работать.</span><span class="sxs-lookup"><span data-stu-id="25b23-107">This is only needed when re-building the components; existing binaries will continue to work.</span></span>|
|<span data-ttu-id="25b23-108">Область</span><span class="sxs-lookup"><span data-stu-id="25b23-108">Scope</span></span>|<span data-ttu-id="25b23-109">Дополнительный номер</span><span class="sxs-lookup"><span data-stu-id="25b23-109">Minor</span></span>|
|<span data-ttu-id="25b23-110">Версия</span><span class="sxs-lookup"><span data-stu-id="25b23-110">Version</span></span>|<span data-ttu-id="25b23-111">4.5.1</span><span class="sxs-lookup"><span data-stu-id="25b23-111">4.5.1</span></span>|
|<span data-ttu-id="25b23-112">Тип</span><span class="sxs-lookup"><span data-stu-id="25b23-112">Type</span></span>|<span data-ttu-id="25b23-113">Изменение целевой платформы</span><span class="sxs-lookup"><span data-stu-id="25b23-113">Retargeting</span></span>|
|<span data-ttu-id="25b23-114">Затронутые API</span><span class="sxs-lookup"><span data-stu-id="25b23-114">Affected APIs</span></span>|<ul><li><xref:System.Data.Common.DbParameter.Precision?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbParameter.Scale?displayProperty=nameWithType></li></ul>|
