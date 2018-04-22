### <a name="previewlostkeyboardfocus-is-called-repeatedly-if-its-handler-shows-a-windows-forms-message-box"></a><span data-ttu-id="43e08-101">PreviewLostKeyboardFocus вызывается повторно, если соответствующий обработчик выводит окно сообщения Windows Forms</span><span class="sxs-lookup"><span data-stu-id="43e08-101">PreviewLostKeyboardFocus is called repeatedly if its handler shows a Windows Forms message box</span></span>

|   |   |
|---|---|
|<span data-ttu-id="43e08-102">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="43e08-102">Details</span></span>|<span data-ttu-id="43e08-103">Начиная с .NET Framework 4.5, вызов <code>System.Windows.Forms.MessageBox.Show</code> из обработчика <xref:System.Windows.UIElement.PreviewLostKeyboardFocus> приведет к повторному запуску обработчика после закрытия окна сообщения. В результате может начаться бесконечный цикл вывода окон сообщений.</span><span class="sxs-lookup"><span data-stu-id="43e08-103">Beginning in the .NET Framework 4.5, calling <code>System.Windows.Forms.MessageBox.Show</code> from a <xref:System.Windows.UIElement.PreviewLostKeyboardFocus> handler will cause the handler to re-fire when the message box is closed, potentially resulting in an infinite loop of message boxes.</span></span>|
|<span data-ttu-id="43e08-104">Предложение</span><span class="sxs-lookup"><span data-stu-id="43e08-104">Suggestion</span></span>|<span data-ttu-id="43e08-105">Существует два способа решения этой проблемы.</span><span class="sxs-lookup"><span data-stu-id="43e08-105">There are two options to work around this issue -</span></span><ol><li><span data-ttu-id="43e08-106">Ее можно избежать, вызвав <code>System.Windows.MessageBox.Show</code> вместо <code>System.Windows.Forms.MessageBox.Show</code>.</span><span class="sxs-lookup"><span data-stu-id="43e08-106">It may be avoided by calling <code>System.Windows.MessageBox.Show</code> instead of <code>System.Windows.Forms.MessageBox.Show</code>.</span></span></li><li><span data-ttu-id="43e08-107">Ее можно избежать, открыв окно сообщения из обработчика событий <xref:System.Windows.UIElement.LostKeyboardFocus> (в отличие от обработчика событий <xref:System.Windows.UIElement.PreviewLostKeyboardFocus?displayProperty=name>).</span><span class="sxs-lookup"><span data-stu-id="43e08-107">It may be avoided by showing the message box from a <xref:System.Windows.UIElement.LostKeyboardFocus> event handler (as opposed to a <xref:System.Windows.UIElement.PreviewLostKeyboardFocus?displayProperty=name> event handler).</span></span></li></ol>|
|<span data-ttu-id="43e08-108">Область</span><span class="sxs-lookup"><span data-stu-id="43e08-108">Scope</span></span>|<span data-ttu-id="43e08-109">Пограничный случай</span><span class="sxs-lookup"><span data-stu-id="43e08-109">Edge</span></span>|
|<span data-ttu-id="43e08-110">Версия</span><span class="sxs-lookup"><span data-stu-id="43e08-110">Version</span></span>|<span data-ttu-id="43e08-111">4.5</span><span class="sxs-lookup"><span data-stu-id="43e08-111">4.5</span></span>|
|<span data-ttu-id="43e08-112">Тип</span><span class="sxs-lookup"><span data-stu-id="43e08-112">Type</span></span>|<span data-ttu-id="43e08-113">Среда выполнения</span><span class="sxs-lookup"><span data-stu-id="43e08-113">Runtime</span></span>|
|<span data-ttu-id="43e08-114">Затронутые API</span><span class="sxs-lookup"><span data-stu-id="43e08-114">Affected APIs</span></span>|<ul><li><xref:System.Windows.ContentElement.PreviewLostKeyboardFocus?displayProperty=nameWithType></li><li><xref:System.Windows.IInputElement.PreviewLostKeyboardFocus?displayProperty=nameWithType></li><li><xref:System.Windows.UIElement.PreviewLostKeyboardFocus?displayProperty=nameWithType></li><li><xref:System.Windows.UIElement3D.PreviewLostKeyboardFocus?displayProperty=nameWithType></li></ul>|
