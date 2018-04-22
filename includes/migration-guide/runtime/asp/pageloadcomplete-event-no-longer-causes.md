### <a name="pageloadcomplete-event-no-longer-causes-systemwebuiwebcontrolsentitydatasource-control-to-invoke-data-binding"></a><span data-ttu-id="10dbd-101">Событие Page.LoadComplete больше не заставляет элемент управления System.Web.UI.WebControls.EntityDataSource вызывать привязку данных</span><span class="sxs-lookup"><span data-stu-id="10dbd-101">Page.LoadComplete event no longer causes System.Web.UI.WebControls.EntityDataSource control to invoke data binding</span></span>

|   |   |
|---|---|
|<span data-ttu-id="10dbd-102">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="10dbd-102">Details</span></span>|<span data-ttu-id="10dbd-103">Событие <xref:System.Web.UI.Page.LoadComplete> больше не заставляет элемент управления <xref:System.Web.UI.WebControls.EntityDataSource?displayProperty=name> вызывать привязку данных для изменений в параметрах создания/обновления/удаления.</span><span class="sxs-lookup"><span data-stu-id="10dbd-103">The <xref:System.Web.UI.Page.LoadComplete> event no longer causes the <xref:System.Web.UI.WebControls.EntityDataSource?displayProperty=name> control to invoke data binding for changes to create/update/delete parameters.</span></span> <span data-ttu-id="10dbd-104">Это изменение исключает лишнее обращение к базе данных, не допускает сброса значений элементов управления и позволяет получить поведение, согласованное с другими элементами управления данными, такими как <xref:System.Web.UI.WebControls.SqlDataSource?displayProperty=name> и <xref:System.Web.UI.WebControls.ObjectDataSource?displayProperty=name>.</span><span class="sxs-lookup"><span data-stu-id="10dbd-104">This change eliminates an extraneous trip to the database, prevents the values of controls from being reset, and produces behavior that is consistent with other data controls, such as <xref:System.Web.UI.WebControls.SqlDataSource?displayProperty=name> and <xref:System.Web.UI.WebControls.ObjectDataSource?displayProperty=name>.</span></span> <span data-ttu-id="10dbd-105">Это изменение дает другое поведение в том маловероятном случае, когда в приложении предполагается вызов привязки данных в событии <xref:System.Web.UI.Page.LoadComplete>.</span><span class="sxs-lookup"><span data-stu-id="10dbd-105">This change produces different behavior in the unlikely event that applications rely on invoking data binding in the <xref:System.Web.UI.Page.LoadComplete> event.</span></span>|
|<span data-ttu-id="10dbd-106">Предложение</span><span class="sxs-lookup"><span data-stu-id="10dbd-106">Suggestion</span></span>|<span data-ttu-id="10dbd-107">Если есть необходимость в привязке данных, вручную вызовите ее в событии, которое возникает раньше в обратной передаче.</span><span class="sxs-lookup"><span data-stu-id="10dbd-107">If there is a need for databinding, manually invoke databind in an event that is earlier in the post-back.</span></span>|
|<span data-ttu-id="10dbd-108">Область</span><span class="sxs-lookup"><span data-stu-id="10dbd-108">Scope</span></span>|<span data-ttu-id="10dbd-109">Пограничный случай</span><span class="sxs-lookup"><span data-stu-id="10dbd-109">Edge</span></span>|
|<span data-ttu-id="10dbd-110">Версия</span><span class="sxs-lookup"><span data-stu-id="10dbd-110">Version</span></span>|<span data-ttu-id="10dbd-111">4.5</span><span class="sxs-lookup"><span data-stu-id="10dbd-111">4.5</span></span>|
|<span data-ttu-id="10dbd-112">Тип</span><span class="sxs-lookup"><span data-stu-id="10dbd-112">Type</span></span>|<span data-ttu-id="10dbd-113">Среда выполнения</span><span class="sxs-lookup"><span data-stu-id="10dbd-113">Runtime</span></span>|
