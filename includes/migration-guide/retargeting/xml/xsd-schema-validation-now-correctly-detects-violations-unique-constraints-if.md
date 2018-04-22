### <a name="xsd-schema-validation-now-correctly-detects-violations-of-unique-constraints-if-compound-keys-are-used-and-one-key-is-empty"></a><span data-ttu-id="74642-101">Проверка схемы XSD теперь правильно обнаруживает нарушения уникальных ограничений, если используются составные ключи и один ключ пуст</span><span class="sxs-lookup"><span data-stu-id="74642-101">XSD Schema validation now correctly detects violations of unique constraints if compound keys are used and one key is empty</span></span>

|   |   |
|---|---|
|<span data-ttu-id="74642-102">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="74642-102">Details</span></span>|<span data-ttu-id="74642-103">В версиях платформы .NET Framework, предшествовавших версии 4.6, была ошибка, из-за которой проверка XSD не могла обнаруживать уникальные ограничения по составным ключам, если один из ключей был пуст.</span><span class="sxs-lookup"><span data-stu-id="74642-103">Versions of the .NET Framework prior to 4.6 had a bug that caused XSD validation to not detect unique constraints on compound keys if one of the keys was empty.</span></span> <span data-ttu-id="74642-104">Эта проблема решена в .NET Framework 4.6.</span><span class="sxs-lookup"><span data-stu-id="74642-104">In the .NET Framework 4.6, this issue is corrected.</span></span> <span data-ttu-id="74642-105">Это приведет к выполнению более правильной проверки, но также может привести к невозможности проверки некоторого XML-кода, которая осуществлялась раньше.</span><span class="sxs-lookup"><span data-stu-id="74642-105">This will result in more correct validation, but it may also result in some XML not validating which previously would have.</span></span>|
|<span data-ttu-id="74642-106">Предложение</span><span class="sxs-lookup"><span data-stu-id="74642-106">Suggestion</span></span>|<span data-ttu-id="74642-107">Если требуется менее строгая проверка .NET Framework 4.0, проверяющее приложение может быть предназначено для версии 4.5 (или более ранней) платформы .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="74642-107">If looser .NET Framework 4.0 validation is needed, the validating application can target version 4.5 (or earlier) of the .NET Framework.</span></span> <span data-ttu-id="74642-108">Однако при изменении целевой платформы на .NET 4.6 следует выполнить проверку кода, чтобы не проверять повторяющиеся составные ключи (как указано в описании этой проблемы).</span><span class="sxs-lookup"><span data-stu-id="74642-108">When retargeting to .NET 4.6, however, code review should be done to be sure that duplicate compound keys (as described in this issue's description) are not expected to validate.</span></span>|
|<span data-ttu-id="74642-109">Область</span><span class="sxs-lookup"><span data-stu-id="74642-109">Scope</span></span>|<span data-ttu-id="74642-110">Пограничный случай</span><span class="sxs-lookup"><span data-stu-id="74642-110">Edge</span></span>|
|<span data-ttu-id="74642-111">Версия</span><span class="sxs-lookup"><span data-stu-id="74642-111">Version</span></span>|<span data-ttu-id="74642-112">4.6</span><span class="sxs-lookup"><span data-stu-id="74642-112">4.6</span></span>|
|<span data-ttu-id="74642-113">Тип</span><span class="sxs-lookup"><span data-stu-id="74642-113">Type</span></span>|<span data-ttu-id="74642-114">Изменение целевой платформы</span><span class="sxs-lookup"><span data-stu-id="74642-114">Retargeting</span></span>|
