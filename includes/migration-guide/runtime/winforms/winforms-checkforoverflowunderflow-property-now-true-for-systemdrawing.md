### <a name="winforms-checkforoverflowunderflow-property-is-now-true-for-systemdrawing"></a><span data-ttu-id="d5b42-101">Свойство CheckForOverflowUnderflow WinForm теперь имеет значение true для System.Drawing</span><span class="sxs-lookup"><span data-stu-id="d5b42-101">WinForm's CheckForOverflowUnderflow property is now true for System.Drawing</span></span>

|   |   |
|---|---|
|<span data-ttu-id="d5b42-102">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="d5b42-102">Details</span></span>|<span data-ttu-id="d5b42-103">Свойство CheckForOverflowUnderflow для сборки System.Drawing.dll имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="d5b42-103">The CheckForOverflowUnderflow property for the System.Drawing.dll assembly is set to true.</span></span>|
|<span data-ttu-id="d5b42-104">Предложение</span><span class="sxs-lookup"><span data-stu-id="d5b42-104">Suggestion</span></span>|<span data-ttu-id="d5b42-105">Раньше при переполнениях результат усекался без уведомления.</span><span class="sxs-lookup"><span data-stu-id="d5b42-105">Previously when overflows occurred, the result would be silently truncated.</span></span> <span data-ttu-id="d5b42-106">Теперь создается исключение <xref:System.OverflowException?displayProperty=name>,</span><span class="sxs-lookup"><span data-stu-id="d5b42-106">Now an <xref:System.OverflowException?displayProperty=name> exception is thrown.</span></span>|
|<span data-ttu-id="d5b42-107">Область</span><span class="sxs-lookup"><span data-stu-id="d5b42-107">Scope</span></span>|<span data-ttu-id="d5b42-108">Пограничный случай</span><span class="sxs-lookup"><span data-stu-id="d5b42-108">Edge</span></span>|
|<span data-ttu-id="d5b42-109">Версия</span><span class="sxs-lookup"><span data-stu-id="d5b42-109">Version</span></span>|<span data-ttu-id="d5b42-110">4.5</span><span class="sxs-lookup"><span data-stu-id="d5b42-110">4.5</span></span>|
|<span data-ttu-id="d5b42-111">Тип</span><span class="sxs-lookup"><span data-stu-id="d5b42-111">Type</span></span>|<span data-ttu-id="d5b42-112">Среда выполнения</span><span class="sxs-lookup"><span data-stu-id="d5b42-112">Runtime</span></span>|
