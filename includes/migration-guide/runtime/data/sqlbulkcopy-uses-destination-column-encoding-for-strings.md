### <a name="sqlbulkcopy-uses-destination-column-encoding-for-strings"></a><span data-ttu-id="12902-101">SqlBulkCopy использует кодировку целевого столбца для строк</span><span class="sxs-lookup"><span data-stu-id="12902-101">SqlBulkCopy uses destination column encoding for strings</span></span>

|   |   |
|---|---|
|<span data-ttu-id="12902-102">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="12902-102">Details</span></span>|<span data-ttu-id="12902-103">При вставке данных в столбец <xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=name> использует кодировку целевого столбца, а не кодировку по умолчанию для типов <code>VARCHAR</code> и <code>CHAR</code>.</span><span class="sxs-lookup"><span data-stu-id="12902-103">When inserting data into a column, <xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=name> uses the encoding of the destination column rather than the default encoding for <code>VARCHAR</code> and <code>CHAR</code> types.</span></span> <span data-ttu-id="12902-104">Это изменение исключает возможность повреждения данных, вызванного использованием кодировки по умолчанию, если в целевом столбце не используется кодировка по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="12902-104">This change eliminates the possibility of data corruption caused by using the default encoding when the destination column does not use the default encoding.</span></span> <span data-ttu-id="12902-105">В редких случаях существующее приложение может создавать исключение SqlException, если при изменении кодировки создаются слишком большие для целевого столбца данные.</span><span class="sxs-lookup"><span data-stu-id="12902-105">In rare cases, an existing application may throw a SqlException exception if the change in encoding produces data that is too big to fit into the destination column.</span></span>|
|<span data-ttu-id="12902-106">Предложение</span><span class="sxs-lookup"><span data-stu-id="12902-106">Suggestion</span></span>|<span data-ttu-id="12902-107">Учитывайте, что <xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=name> больше не будет повреждать данные из-за различий в кодировке.</span><span class="sxs-lookup"><span data-stu-id="12902-107">Expect that <xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=name> will no longer corrupt data due to encoding differences.</span></span> <span data-ttu-id="12902-108">Если размер копируемых строк близок к установленному для целевого столбца ограничению, может потребоваться предварительное кодирование данных (с целью копирования для проверки того, что они поместятся в целевом столбце) или перехват исключений <xref:System.Data.SqlClient.SqlException?displayProperty=name>.</span><span class="sxs-lookup"><span data-stu-id="12902-108">If strings near the destination column's size limit are being copied, it may be necessary to either pre-encode data (to be copied to check that the data will fit in the destination column) or catch <xref:System.Data.SqlClient.SqlException?displayProperty=name>s.</span></span>|
|<span data-ttu-id="12902-109">Область</span><span class="sxs-lookup"><span data-stu-id="12902-109">Scope</span></span>|<span data-ttu-id="12902-110">Пограничный случай</span><span class="sxs-lookup"><span data-stu-id="12902-110">Edge</span></span>|
|<span data-ttu-id="12902-111">Версия</span><span class="sxs-lookup"><span data-stu-id="12902-111">Version</span></span>|<span data-ttu-id="12902-112">4.5</span><span class="sxs-lookup"><span data-stu-id="12902-112">4.5</span></span>|
|<span data-ttu-id="12902-113">Тип</span><span class="sxs-lookup"><span data-stu-id="12902-113">Type</span></span>|<span data-ttu-id="12902-114">Среда выполнения</span><span class="sxs-lookup"><span data-stu-id="12902-114">Runtime</span></span>|
|<span data-ttu-id="12902-115">Затронутые API</span><span class="sxs-lookup"><span data-stu-id="12902-115">Affected APIs</span></span>|<ul><li><xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlBulkCopy.%23ctor(System.Data.SqlClient.SqlConnection)?displayProperty=nameWithType></li></ul>|
