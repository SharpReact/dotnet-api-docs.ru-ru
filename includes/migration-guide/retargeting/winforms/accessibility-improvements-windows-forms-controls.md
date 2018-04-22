### <a name="accessibility-improvements-in-windows-forms-controls"></a><span data-ttu-id="dded3-101">Улучшения специальных возможностей для элементов управления Windows Forms</span><span class="sxs-lookup"><span data-stu-id="dded3-101">Accessibility improvements in Windows Forms controls</span></span>

|   |   |
|---|---|
|<span data-ttu-id="dded3-102">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="dded3-102">Details</span></span>|<span data-ttu-id="dded3-103">В Windows Forms улучшено использование специальных возможностей, обеспечивающих большее удобство для пользователей Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="dded3-103">Windows Forms is improving how it works with accessibility technologies to better support Windows Forms customers.</span></span> <span data-ttu-id="dded3-104">Внесены следующие изменения:</span><span class="sxs-lookup"><span data-stu-id="dded3-104">These include the following changes:</span></span><ul><li><span data-ttu-id="dded3-105">Изменения для улучшения видимости в режиме высокой контрастности.</span><span class="sxs-lookup"><span data-stu-id="dded3-105">Changes to improve display during High Contrast mode.</span></span></li><li><span data-ttu-id="dded3-106">Изменения для улучшения работы с обозревателем свойств.</span><span class="sxs-lookup"><span data-stu-id="dded3-106">Changes to improve the property browser experience.</span></span> <span data-ttu-id="dded3-107">Список усовершенствований обозревателя свойств включает:</span><span class="sxs-lookup"><span data-stu-id="dded3-107">Property browser improvements include:</span></span></li><li><span data-ttu-id="dded3-108">Улучшенная навигация с помощью клавиатуры посредством различных окон выбора с раскрывающимися списками.</span><span class="sxs-lookup"><span data-stu-id="dded3-108">Better keyboard navigation through the various drop-down selection windows.</span></span></li><li><span data-ttu-id="dded3-109">Уменьшение числа ненужных позиций табуляции.</span><span class="sxs-lookup"><span data-stu-id="dded3-109">Reduced unnecessary tab stops.</span></span></li><li><span data-ttu-id="dded3-110">Улучшенные отчеты о типах элементов управления.</span><span class="sxs-lookup"><span data-stu-id="dded3-110">Better reporting of control types.</span></span></li><li><span data-ttu-id="dded3-111">Улучшенная работа экранного диктора.</span><span class="sxs-lookup"><span data-stu-id="dded3-111">Improved narrator behavior.</span></span></li><li><span data-ttu-id="dded3-112">Изменения в реализации отсутствующих шаблонов специальных возможностей пользовательского интерфейса в элементах управления.</span><span class="sxs-lookup"><span data-stu-id="dded3-112">Changes to implement missing UI accessibility patterns in controls.</span></span></li></ul>|
|<span data-ttu-id="dded3-113">Предложение</span><span class="sxs-lookup"><span data-stu-id="dded3-113">Suggestion</span></span>|<span data-ttu-id="dded3-114"><strong>Как принять или отклонить изменения</strong>Чтобы эти изменения можно было использовать в приложении, оно должно быть запущено на платформе .NET Framework 4.7.1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="dded3-114"><strong>How to opt in or out of these changes</strong>In order for the application to benefit from these changes, it must run on the .NET Framework 4.7.1 or later.</span></span> <span data-ttu-id="dded3-115">В приложении эти изменения можно использовать одним из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="dded3-115">The application can benefit from these changes in either of the following ways:</span></span><ul><li><span data-ttu-id="dded3-116">Выполнить повторную компиляцию, чтобы нацелить приложение на .NET Framework 4.7.1.</span><span class="sxs-lookup"><span data-stu-id="dded3-116">It is recompiled to target the .NET Framework 4.7.1.</span></span> <span data-ttu-id="dded3-117">Эти специальные возможности включены по умолчанию для приложений Windows Forms, ориентированных на .NET Framework 4.7.1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="dded3-117">These accessibility changes are enabled by default on Windows Forms applications that target the .NET Framework 4.7.1 or later.</span></span></li><li><span data-ttu-id="dded3-118">Для отказа от функций специальных возможностей предыдущих версий [переключатель AppContext](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) добавляется в раздел <code>&lt;runtime&gt;</code> файла конфигурации приложения и получает значение <code>false</code>, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="dded3-118">It opts out of the legacy accessibility behaviors by adding the following [AppContext switch](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) to the <code>&lt;runtime&gt;</code> section of the app.config file and setting it to <code>false</code>, as the following example shows.</span></span></li></ul><pre><code class="language-xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;&#13;&#10;&lt;configuration&gt;&#13;&#10;&lt;startup&gt;&#13;&#10;&lt;supportedRuntime version=&quot;v4.0&quot; sku=&quot;.NETFramework,Version=v4.7&quot;/&gt;&#13;&#10;&lt;/startup&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;!-- AppContextSwitchOverrides value attribute is in the form of &#39;key1=true/false;key2=true/false  --&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.UseLegacyAccessibilityFeatures=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre><span data-ttu-id="dded3-119">В приложениях, предназначенных для .NET Framework 4.7.1 или более поздней версии, где требуется сохранить предыдущие функции специальных возможностей, можно выбрать прежние функции специальных возможностей, явно установив этот переключатель AppContext в значение <code>true</code>. Общие сведения об автоматизации пользовательского интерфейса см. в [этом разделе](~/docs/framework/ui-automation/ui-automation-overview.md). <strong>Добавлена поддержка шаблонов и свойств автоматизации пользовательского интерфейса</strong>Клиенты специальных возможностей могут использовать новые функции специальных возможностей WinForms с помощью общих шаблонов вызова с открытым описанием.</span><span class="sxs-lookup"><span data-stu-id="dded3-119">Applications that target the .NET Framework 4.7.1 or later and want to preserve the legacy accessibility behavior can opt in to the use of legacy accessibility features by explicitly setting this AppContext switch to <code>true</code>.For an overview of UI automation, see the [UI Automation Overview](~/docs/framework/ui-automation/ui-automation-overview.md).<strong>Added support for UI Automation patterns and properties</strong>Accessibility clients can take advantage of new WinForms accessibility functionality by using common, publicly described invocation patterns.</span></span> <span data-ttu-id="dded3-120">Эти шаблоны предназначены не только для WinForms.</span><span class="sxs-lookup"><span data-stu-id="dded3-120">These patterns are not WinForms-specific.</span></span> <span data-ttu-id="dded3-121">Например, клиенты специальных возможностей могут вызывать метод QueryInterface для интерфейса IAccessible (MAAS), чтобы получить интерфейс IServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="dded3-121">For instance, accessibility clients can call the QueryInterface method on the IAccessible interface (MAAS) to obtain an IServiceProvider interface.</span></span> <span data-ttu-id="dded3-122">Если этот интерфейс доступен, клиенты могут использовать его метод QueryService для запроса интерфейса IAccessibleEx.</span><span class="sxs-lookup"><span data-stu-id="dded3-122">If this interface is available, clients can use its QueryService method to request an IAccessibleEx interface.</span></span> <span data-ttu-id="dded3-123">Дополнительные сведения см. в разделе [Использование интерфейса IAccessibleEx из клиента](https://msdn.microsoft.com/library/windows/desktop/dd561924.aspx).</span><span class="sxs-lookup"><span data-stu-id="dded3-123">For more information, see [Using IAccessibleEx from a Client](https://msdn.microsoft.com/library/windows/desktop/dd561924.aspx).</span></span> <span data-ttu-id="dded3-124">Начиная с версии .NET Framework 4.7.1, интерфейсы IServiceProvider и [IAccessibleEx](https://msdn.microsoft.com/library/windows/desktop/dd561898.aspx) (где применимо) доступны объектам специальных возможностей WinForms. В .NET Framework 4.7.1 добавлена поддержка следующих шаблонов и свойств автоматизации пользовательского интерфейса:</span><span class="sxs-lookup"><span data-stu-id="dded3-124">Starting with the .NET Framework 4.7.1, IServiceProvider and [IAccessibleEx](https://msdn.microsoft.com/library/windows/desktop/dd561898.aspx) (where applicable) are available for WinForms accessibility objects.The .NET Framework 4.7.1 adds support for the following UI automation patterns and properties:</span></span><ul><li><span data-ttu-id="dded3-125">Элементы управления <code>T:System.Windows.Forms.ToolStripSplitButton</code> и <code>T:System.Windows.Forms.ComboBox</code> поддерживают [шаблон развертывания/свертывания](~/docs/framework/ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md).</span><span class="sxs-lookup"><span data-stu-id="dded3-125">The <code>T:System.Windows.Forms.ToolStripSplitButton</code> and <code>T:System.Windows.Forms.ComboBox</code> controls support the [Expand/Collapse pattern](~/docs/framework/ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md).</span></span></li><li><span data-ttu-id="dded3-126">Элемент управления <code>T:System.Windows.Forms.ToolStripMenuItem</code> использует для свойства [ControlType](~/docs/framework/ui-automation/ui-automation-support-for-the-menubar-control-type.md) значение <xref:System.Windows.Automation.ControlType.MenuItem?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="dded3-126">The <code>T:System.Windows.Forms.ToolStripMenuItem</code> control has a [ControlType](~/docs/framework/ui-automation/ui-automation-support-for-the-menubar-control-type.md) property value <xref:System.Windows.Automation.ControlType.MenuItem?displayProperty=nameWithType>.</span></span></li><li><span data-ttu-id="dded3-127">Элемент управления <code>T:System.Windows.Forms.ToolStripItem</code> поддерживает свойство [Name](xref:System.Windows.Automation.AutomationElement.NameProperty) и [шаблон развертывания/свертывания](~/docs/framework/ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md).</span><span class="sxs-lookup"><span data-stu-id="dded3-127">The <code>T:System.Windows.Forms.ToolStripItem</code> control supports the [Name](xref:System.Windows.Automation.AutomationElement.NameProperty) property and [Expand/Collapse pattern](~/docs/framework/ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md).</span></span></li><li><span data-ttu-id="dded3-128">Элемент управления <code>T:System.Windows.Forms.ToolStripDropDownItem</code> поддерживает <xref:System.Windows.Forms.AccessibleEvents> с указанием StateChange и NameChange при развертывании или свертывании раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="dded3-128">The <code>T:System.Windows.Forms.ToolStripDropDownItem</code> control supports <xref:System.Windows.Forms.AccessibleEvents> indicating StateChange and NameChange when drop down is expanded or collapsed.</span></span></li><li><span data-ttu-id="dded3-129">Элемент управления <code>T:System.Windows.Forms.ToolStripDropDownButton</code> использует для свойства [ControlType](~/docs/framework/ui-automation/ui-automation-support-for-the-menubar-control-type.md) значение <xref:System.Windows.Automation.ControlType.MenuItem?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="dded3-129">The <code>T:System.Windows.Forms.ToolStripDropDownButton</code> control has a [ControlType](~/docs/framework/ui-automation/ui-automation-support-for-the-menubar-control-type.md) property value of <xref:System.Windows.Automation.ControlType.MenuItem?displayProperty=nameWithType>.</span></span></li><li><span data-ttu-id="dded3-130">Элемент управления <code>T:System.Windows.Forms.DataGridViewCheckBoxCell</code> поддерживает [шаблон переключения](xref:System.Windows.Automation.TogglePattern).</span><span class="sxs-lookup"><span data-stu-id="dded3-130">The <code>T:System.Windows.Forms.DataGridViewCheckBoxCell</code> control supports the [Toggle Pattern](xref:System.Windows.Automation.TogglePattern).</span></span></li><li><span data-ttu-id="dded3-131">Элементы управления <code>T:System.Windows.Forms.NumericUpDown</code> и <code>T:System.Windows.Forms.DomainUpDown</code> поддерживают [Name](xref:System.Windows.Automation.AutomationElement.NameProperty) и используют для свойства [ControlType](~/docs/framework/ui-automation/ui-automation-support-for-the-spinner-control-type.md) значение <xref:System.Windows.Automation.ControlType.Spinner?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="dded3-131">The <code>T:System.Windows.Forms.NumericUpDown</code> and <code>T:System.Windows.Forms.DomainUpDown</code> controls support the [Name](xref:System.Windows.Automation.AutomationElement.NameProperty) and have a [ControlType](~/docs/framework/ui-automation/ui-automation-support-for-the-spinner-control-type.md) of <xref:System.Windows.Automation.ControlType.Spinner?displayProperty=nameWithType>.</span></span></li></ul><span data-ttu-id="dded3-132"><strong>Улучшения элемента управления PropertyGrid</strong>В .NET Framework 4.7.1 добавлены следующие улучшения браузерного элемента управления PropertyBrowser:</span><span class="sxs-lookup"><span data-stu-id="dded3-132"><strong>Improvements to the PropertyGrid control</strong>The .NET Framework 4.7.1 adds the following improvements to the PropertyBrowser control:</span></span><ul><li><span data-ttu-id="dded3-133">Кнопка <strong>Подробнее</strong> в диалоговом окне ошибки, которое появляется при вводе пользователем неверного значения в элемент управления <code>T:System.Windows.Forms.PropertyGrid</code>, поддерживает [шаблон развертывания/свертывания](~/docs/framework/ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md), уведомления об изменении имени и состояния, а также свойство [ControlType](~/docs/framework/ui-automation/ui-automation-support-for-the-menubar-control-type.md) со значением <xref:System.Windows.Automation.ControlType.MenuItem?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="dded3-133">The <strong>Details</strong> button in the error dialog that is displayed when the user enters an incorrect value in the <code>T:System.Windows.Forms.PropertyGrid</code> control supports the [Expand/Collapse pattern](~/docs/framework/ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md), state and name change notifications, and a [ControlType](~/docs/framework/ui-automation/ui-automation-support-for-the-menubar-control-type.md) property with a value of <xref:System.Windows.Automation.ControlType.MenuItem?displayProperty=nameWithType>.</span></span></li><li><span data-ttu-id="dded3-134">Область сообщений, которая отображается при развертывании кнопки <strong>Подробнее</strong> в диалоговом окне ошибки, теперь доступна с клавиатуры и поддерживает объявление содержимого сообщения об ошибке с помощью экранного диктора.</span><span class="sxs-lookup"><span data-stu-id="dded3-134">The message pane displayed when the <strong>Details</strong> button of the error dialog is expanded is now keyboard accessible and allows Narrator to announce the content of the error message.</span></span></li><li><span data-ttu-id="dded3-135">Значение <xref:System.Windows.Forms.AccessibleRole> для строк в элементе управления <code>T:System.Windows.Forms.PropertyGrid</code> изменилось со &quot;Строка&quot; на &quot;Ячейка&quot;.</span><span class="sxs-lookup"><span data-stu-id="dded3-135">The <xref:System.Windows.Forms.AccessibleRole> of rows in <code>T:System.Windows.Forms.PropertyGrid</code> control have changed from &quot;Row&quot; to &quot;Cell&quot;.</span></span> <span data-ttu-id="dded3-136">Ячейка сопоставляется с типом элемента управления &quot;DataItem&quot; модели автоматизации пользовательского интерфейса, благодаря чему обеспечивается поддержка соответствующих сочетаний клавиш и объявлений экранного диктора.</span><span class="sxs-lookup"><span data-stu-id="dded3-136">The cell maps to UIA ControlType &quot;DataItem&quot;, which allows it to support appropriate keyboard shortcuts and Narrator announcements.</span></span></li><li><span data-ttu-id="dded3-137">Строки элемента управления <code>T:System.Windows.Forms.PropertyGrid</code>, которые представляют элементы заголовка в том случае, если для элемента управления <code>T:System.Windows.Forms.PropertyGrid</code> свойство <code>P:System.Windows.Forms.PropertySort</code> имеет значение <code>F:System.Windows.Forms.PropertySory.Categorized</code>, имеют значение свойства [ControlType](~/docs/framework/ui-automation/ui-automation-support-for-the-menubar-control-type.md), равное <xref:System.Windows.Automation.ControlType.Button?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="dded3-137">The <code>T:System.Windows.Forms.PropertyGrid</code> control rows which represent header items when the <code>T:System.Windows.Forms.PropertyGrid</code> control has a <code>P:System.Windows.Forms.PropertySort</code> property set to <code>F:System.Windows.Forms.PropertySory.Categorized</code> have a [ControlType](~/docs/framework/ui-automation/ui-automation-support-for-the-menubar-control-type.md) property value of <xref:System.Windows.Automation.ControlType.Button?displayProperty=nameWithType></span></span></li><li><span data-ttu-id="dded3-138">Строки элемента управления <code>T:System.Windows.Forms.PropertyGrid</code>, которые представляют элементы заголовка в том случае, если для элемента управления <code>T:System.Windows.Forms.PropertyGrid</code> свойство <code>P:System.Windows.Forms.PropertySort</code> имеет значение <code>F:System.Windows.Forms.PropertySory.Categorized</code>, поддерживают [шаблон развертывания/свертывания](~/docs/framework/ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md).</span><span class="sxs-lookup"><span data-stu-id="dded3-138">The <code>T:System.Windows.Forms.PropertyGrid</code> control rows which represent header items when the <code>T:System.Windows.Forms.PropertyGrid</code> control has a <code>P:System.Windows.Forms.PropertySort</code> property set to <code>F:System.Windows.Forms.PropertySory.Categorized</code> support the [Expand/Collapse pattern](~/docs/framework/ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md).</span></span></li><li><span data-ttu-id="dded3-139">Улучшена навигация с помощью клавиатуры между сеткой и расположенной над ней панелью инструментов.</span><span class="sxs-lookup"><span data-stu-id="dded3-139">Improved keyboard navigation between the grid and the ToolBar above it.</span></span> <span data-ttu-id="dded3-140">При нажатии клавиш &quot;SHIFT+TAB&quot; теперь выбирается не вся панель инструментов, а только ее первая кнопка</span><span class="sxs-lookup"><span data-stu-id="dded3-140">Pressing &quot;Shift-Tab&quot; now selects the first ToolBar button, instead of the whole ToolBar</span></span></li><li><span data-ttu-id="dded3-141">Элементы управления <code>T:System.Windows.Forms.PropertyGrid</code>, отображаемые в режиме высокой контрастности, теперь отрисовывают прямоугольник фокуса вокруг кнопки панели инструментов, которая соответствует текущему значению свойства <code>P:System.Windows.Forms.PropertySort</code>.</span><span class="sxs-lookup"><span data-stu-id="dded3-141"><code>T:System.Windows.Forms.PropertyGrid</code> controls displayed in High Contrast mode will now draw a focus rectangle around the ToolBar button which corresponds to the current <code>P:System.Windows.Forms.PropertySort</code> property value.</span></span></li><li><span data-ttu-id="dded3-142">Элементы управления <code>T:System.Windows.Forms.PropertyGrid</code>, которые отображаются в режиме высокой контрастности и имеют свойство <code>P:System.Windows.Forms.PropertySort</code>, равное <code>F:System.Windows.Forms.PropertySory.Categorized</code>, теперь используют цвет высокой контрастности для отображения фона заголовков категорий.</span><span class="sxs-lookup"><span data-stu-id="dded3-142"><code>T:System.Windows.Forms.PropertyGrid</code> controls displayed in High Contrast mode and with a <code>P:System.Windows.Forms.PropertySort</code> property set to <code>F:System.Windows.Forms.PropertySory.Categorized</code> will now display the background of category headers in a highly contrasting color.</span></span></li><li><span data-ttu-id="dded3-143">Элементы управления <code>T:System.Windows.Forms.PropertyGrid</code> обеспечивают более заметные различия между находящимися в фокусе элементами панели инструментов и теми элементами панели инструментов, которые указывают текущее значение свойства <code>P:System.Windows.Forms.PropertySort</code>.</span><span class="sxs-lookup"><span data-stu-id="dded3-143"><code>T:System.Windows.Forms.PropertyGrid</code> controls better differentiates between ToolBar items with focus and the ToolBar items which indicate the current value of the <code>P:System.Windows.Forms.PropertySort</code> property.</span></span> <span data-ttu-id="dded3-144">Это исправление включает в себя изменение режима высокой контрастности, а также изменения других сценариев.</span><span class="sxs-lookup"><span data-stu-id="dded3-144">This fix consists of a High Contrast change and a change for non-High Contrast scenarios.</span></span></li><li><span data-ttu-id="dded3-145">Элементы панели инструментов для элемента управления <code>T:System.Windows.Forms.PropertyGrid</code>, которые указывают текущее значение свойства <code>P:System.Windows.Forms.PropertySort</code>, поддерживают [шаблон переключения](xref:System.Windows.Automation.TogglePattern).</span><span class="sxs-lookup"><span data-stu-id="dded3-145"><code>T:System.Windows.Forms.PropertyGrid</code> control ToolBar items which indicates the current value of the <code>P:System.Windows.Forms.PropertySort</code> property support the [Toggle Pattern](xref:System.Windows.Automation.TogglePattern).</span></span></li><li><span data-ttu-id="dded3-146">Улучшенная поддержка экранного диктора для различения выбранного режима выравнивания в соответствующем средстве.</span><span class="sxs-lookup"><span data-stu-id="dded3-146">Improved Narrator support for distinguishing the selected alignment in the Alignment Picker.</span></span></li><li><span data-ttu-id="dded3-147">Если в форме отображается пустой элемент управления <code>T:System.Windows.Forms.PropertyGrid</code>, он будет получать фокус в тех случаях, в которых это ранее не происходило.</span><span class="sxs-lookup"><span data-stu-id="dded3-147">When an empty <code>T:System.Windows.Forms.PropertyGrid</code> control is displayed on a form, it will now receive focus where previously it would not.</span></span></li></ul><span data-ttu-id="dded3-148"><strong>Использование определенных в ОС цветов в темах высокой контрастности</strong></span><span class="sxs-lookup"><span data-stu-id="dded3-148"><strong>Use of OS-defined colors in High Contrast themes</strong></span></span><ul><li><span data-ttu-id="dded3-149">Элементы управления <code>T:System.Windows.Forms.Button</code> и <code>T:System.Windows.Forms.CheckBox</code>, для которых свойству <code>P:System.Windows.Forms.Control.FlatStyle</code> присвоено значение <xref:System.Windows.Forms.FlatStyle.System?displayProperty=nameWithType> (стиль по умолчанию), теперь используют определенные в ОС цвета при выборе темы высокой контрастности.</span><span class="sxs-lookup"><span data-stu-id="dded3-149"><code>T:System.Windows.Forms.Button</code> and <code>T:System.Windows.Forms.CheckBox</code> controls with <code>P:System.Windows.Forms.Control.FlatStyle</code> set to <xref:System.Windows.Forms.FlatStyle.System?displayProperty=nameWithType>, which is the default style, now use OS-defined colors in High Contrast theme when selected.</span></span> <span data-ttu-id="dded3-150">Ранее цвета текста и фона не были контрастными, что ухудшало разборчивость.</span><span class="sxs-lookup"><span data-stu-id="dded3-150">Previously, text and background colors were not contrasting and were hard to read.</span></span></li><li><span data-ttu-id="dded3-151">Элементы управления <code>T:System.Windows.Forms.Button</code>, <code>T:System.Windows.Forms.CheckBox</code>, <code>T:System.Windows.Forms.RadioButton</code>, <code>T:System.Windows.Forms.Label</code>, <code>T:System.Windows.Forms.LinkLabel</code> и <code>T:System.Windows.Forms.GroupBox</code>, для которых свойству <code>P:System.Windows.Forms.Control.Enabled</code> присвоено значение <em>false</em>, использовали затененный цвет для отображения текста в темах высокой контрастности, в результате чего не обеспечивался достаточный контраст между текстом и фоном.</span><span class="sxs-lookup"><span data-stu-id="dded3-151"><code>T:System.Windows.Forms.Button</code>, <code>T:System.Windows.Forms.CheckBox</code>, <code>T:System.Windows.Forms.RadioButton</code>, <code>T:System.Windows.Forms.Label</code>, <code>T:System.Windows.Forms.LinkLabel</code> and <code>T:System.Windows.Forms.GroupBox</code> with<code>P:System.Windows.Forms.Control.Enabled</code> set to <em>false</em>, used a shaded color to render text in High Contrast themes, resulting in low contrast against the background.</span></span> <span data-ttu-id="dded3-152">Теперь для этих элементов управления используется цвет &quot;Выключенный текст&quot;, определенный в ОС.</span><span class="sxs-lookup"><span data-stu-id="dded3-152">Now these controls use &quot;Disabled Text&quot; color defined by the OS.</span></span> <span data-ttu-id="dded3-153">Это исправление применяется к элементам управления, для которых свойству <code>P:System.Windows.Forms.Control.FlatStyle</code> присвоено значение, отличное от <code>F:System.Windows.Forms.FlatStyle.System</code>.</span><span class="sxs-lookup"><span data-stu-id="dded3-153">This fix applies to controls with <code>P:System.Windows.Forms.Control.FlatStyle</code> property set to a value other than <code>F:System.Windows.Forms.FlatStyle.System</code>.</span></span> <span data-ttu-id="dded3-154">Последние элементы управления отображаются операционной системой.</span><span class="sxs-lookup"><span data-stu-id="dded3-154">The latter controls are rendered by the OS.</span></span></li><li><span data-ttu-id="dded3-155"><code>T:System.Windows.Forms.DataGridView</code> теперь отображает видимый прямоугольник вокруг содержимого ячейки, в которой в данный момент установлен фокус.</span><span class="sxs-lookup"><span data-stu-id="dded3-155"><code>T:System.Windows.Forms.DataGridView</code> now renders a visible rectangle around the content of the cell which has the current focus.</span></span> <span data-ttu-id="dded3-156">Ранее в некоторых темах высокой контрастности этот прямоугольник был незаметен.</span><span class="sxs-lookup"><span data-stu-id="dded3-156">Previously, this was not visible in certain High Contrast themes.</span></span></li><li><span data-ttu-id="dded3-157">Элементы управления <code>T:System.Windows.Forms.ToolStripMenuItem</code>, для которых свойству <code>P:System.Windows.Forms.ToolStripItem.Enabled</code> присвоено значение <em>false</em>, теперь используют цвет &quot;Выключенный цвет&quot;, определенный в ОС.</span><span class="sxs-lookup"><span data-stu-id="dded3-157"><code>T:System.Windows.Forms.ToolStripMenuItem</code> controls with a <code>P:System.Windows.Forms.ToolStripItem.Enabled</code> property set to <em>false</em> now use the &quot;Disabled Text&quot; color defined by the OS.</span></span></li><li><span data-ttu-id="dded3-158">Элементы управления <code>T:System.Windows.Forms.ToolStripMenuItem</code>, для которых свойству <code>P:System.Windows.Forms.ToolStripItem.Checked</code> присвоено значение <em>true</em>, теперь отображают соответствующий флажок с использованием контрастного системного цвета.</span><span class="sxs-lookup"><span data-stu-id="dded3-158"><code>T:System.Windows.Forms.ToolStripMenuItem</code> controls with a <code>P:System.Windows.Forms.ToolStripItem.Checked</code> property set to <em>true</em> now render the associated check mark in a contrasting system color.</span></span>  <span data-ttu-id="dded3-159">Ранее цвет флажка был недостаточно контрастным, в результате чего он был не виден в некоторых темах высокой контрастности.</span><span class="sxs-lookup"><span data-stu-id="dded3-159">Previously the check mark color was not contrasting enough and not visible in High Contrast themes.</span></span></li></ul><span data-ttu-id="dded3-160">ПРИМЕЧАНИЕ. В Windows 10 изменены значения некоторых системных цветов для тем высокой контрастности.</span><span class="sxs-lookup"><span data-stu-id="dded3-160">NOTE: Windows10 has changed values for some high contrast system colors.</span></span> <span data-ttu-id="dded3-161">Платформа Windows Forms Framework построена на основе Win32.</span><span class="sxs-lookup"><span data-stu-id="dded3-161">Windows Forms Framework is based on the Win32 framework.</span></span> <span data-ttu-id="dded3-162">Для достижения наилучших результатов используйте самую последнюю версию Windows и согласитесь на последние изменения операционной системы, добавив файл app.manifest в тестовое приложение и раскомментировав следующий код:</span><span class="sxs-lookup"><span data-stu-id="dded3-162">For the best experience, run on the latest version of Windows and opt in to the latest OS changes by adding an app.manifest file in a test application and uncommenting the following code:</span></span><pre><code>&lt;!-- Windows 10 --&gt;&#13;&#10;&lt;supportedOS Id=&quot;{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}&quot; /&gt;&#13;&#10;</code></pre><span data-ttu-id="dded3-163"><strong>Улучшение навигации с помощью клавиатуры</strong></span><span class="sxs-lookup"><span data-stu-id="dded3-163"><strong>Improved keyboard navigation</strong></span></span><ul><li><span data-ttu-id="dded3-164">Если для элемента управления <code>T:System.Windows.Forms.ComboBox</code> свойство <code>P:System.Windows.Forms.ComboBox.DropDownStyle</code> имеет значение <code>F:System.Windows.Forms.DropDownStyle.DropDownList</code> и он является первым элементом управления на вкладке формы, при открытии родительской формы с помощью клавиатуры он теперь отображает прямоугольник фокуса.</span><span class="sxs-lookup"><span data-stu-id="dded3-164">When a <code>T:System.Windows.Forms.ComboBox</code> control has <code>P:System.Windows.Forms.ComboBox.DropDownStyle</code> set to <code>F:System.Windows.Forms.DropDownStyle.DropDownList</code> and is the first control in the tab order on the form, it now displays a focus rectangle when the parent form is opened using the keyboard.</span></span> <span data-ttu-id="dded3-165">До этого изменения фокус устанавливался в этот элемент управления, однако индикатор фокуса не отображался.</span><span class="sxs-lookup"><span data-stu-id="dded3-165">Before this change, keyboard focus was on this control, but a focus indicator was not rendered.</span></span></li></ul><span data-ttu-id="dded3-166"><strong>Улучшенная поддержка экранного диктора</strong></span><span class="sxs-lookup"><span data-stu-id="dded3-166"><strong>Improved Narrator support</strong></span></span><ul><li><span data-ttu-id="dded3-167">Для элемента управления <code>T:System.Windows.Forms.MonthCalendar</code> добавлена поддержка вспомогательных технологий, обеспечивающих доступ к элементу управления, в том числе возможность объявления значения элемента управления с помощью экранного диктора, которая ранее отсутствовала.</span><span class="sxs-lookup"><span data-stu-id="dded3-167">The <code>T:System.Windows.Forms.MonthCalendar</code> control has added support for assistive technologies to access the control, including the ability for Narrator to read the value of the control when previously it could not.</span></span></li><li><span data-ttu-id="dded3-168">Элемент управления <code>T:System.Windows.Forms.CheckedListBox</code> теперь направляет в экранный диктор уведомления об изменении свойства <code>P:System.Windows.Forms.CheckState</code>.</span><span class="sxs-lookup"><span data-stu-id="dded3-168">The <code>T:System.Windows.Forms.CheckedListBox</code> control now notifies Narrator when the <code>P:System.Windows.Forms.CheckState</code> property has been changed.</span></span> <span data-ttu-id="dded3-169">Ранее экранный диктор не получал уведомления, в результате чего пользователи на знали об обновлении <code>P:System.Windows.Forms.CheckState</code>.</span><span class="sxs-lookup"><span data-stu-id="dded3-169">Previously, Narrator did not recieve notification and as a result users would not be informed that the <code>P:System.Windows.Forms.CheckState</code> had been updated.</span></span></li><li><span data-ttu-id="dded3-170">Для элемента управления <code>T:System.Windows.Forms.LinkLabel</code> изменился способ уведомления экранного диктора о тексте элемента управления.</span><span class="sxs-lookup"><span data-stu-id="dded3-170">The <code>T:System.Windows.Forms.LinkLabel</code> control has changed the way it notifies Narrator of the text of in the control.</span></span> <span data-ttu-id="dded3-171">Ранее экранный диктор объявлял этот текст дважды и читал символы &quot;&amp;&quot; как реальный текст, хотя они не были видны пользователю.</span><span class="sxs-lookup"><span data-stu-id="dded3-171">Previously, Narrator announced this text twice and read &quot;&amp;&quot; symbols as real text even though they are not visible to a user.</span></span> <span data-ttu-id="dded3-172">Из объявлений экранного диктора исключены ненужные символы &quot;&amp;&quot; и повторяющийся текст.</span><span class="sxs-lookup"><span data-stu-id="dded3-172">The duplicated text was removed from the Narrator announcements, as well as unnecessary &quot;&amp;&quot; symbols.</span></span></li><li><span data-ttu-id="dded3-173">Типы элемента управления <code>T:System.Windows.Forms.DataGridViewCell</code> теперь корректно сообщают о состоянии только для чтения экранному диктору и другим вспомогательным технологиям.</span><span class="sxs-lookup"><span data-stu-id="dded3-173">The <code>T:System.Windows.Forms.DataGridViewCell</code> control types now correctly report the read-only status to Narrator and other assistive technologies.</span></span></li><li><span data-ttu-id="dded3-174">Экранный диктор теперь может читать системное меню дочерних окон в приложениях с [многодокументным интерфейсом](~/docs/framework/winforms/advanced/multiple-document-interface-mdi-applications.md).</span><span class="sxs-lookup"><span data-stu-id="dded3-174">Narrator is now able to read the System Menu of child windows in [Multiple-Document Interface](~/docs/framework/winforms/advanced/multiple-document-interface-mdi-applications.md) applications.</span></span></li><li><span data-ttu-id="dded3-175">Экранный диктор теперь может читать элементы управления <code>T:System.Windows.Forms.ToolStripMenuItem</code>, для которых свойству <code>P:System.Windows.Forms.ToolStripItem.Enabled</code> присвоено значение <em>false</em>.</span><span class="sxs-lookup"><span data-stu-id="dded3-175">Narrator is now able to read <code>T:System.Windows.Forms.ToolStripMenuItem</code> controls with a <code>P:System.Windows.Forms.ToolStripItem.Enabled</code> property set to <em>false</em>.</span></span> <span data-ttu-id="dded3-176">Ранее экранный диктор не мог получить фокус для отключенных пунктов меню, чтобы считывать их содержимое.</span><span class="sxs-lookup"><span data-stu-id="dded3-176">Previously, Narrator was unable to focus on disabled menu items to read hte content.</span></span></li></ul>|
|<span data-ttu-id="dded3-177">Область</span><span class="sxs-lookup"><span data-stu-id="dded3-177">Scope</span></span>|<span data-ttu-id="dded3-178">Значительно</span><span class="sxs-lookup"><span data-stu-id="dded3-178">Major</span></span>|
|<span data-ttu-id="dded3-179">Версия</span><span class="sxs-lookup"><span data-stu-id="dded3-179">Version</span></span>|<span data-ttu-id="dded3-180">4.7.1</span><span class="sxs-lookup"><span data-stu-id="dded3-180">4.7.1</span></span>|
|<span data-ttu-id="dded3-181">Тип</span><span class="sxs-lookup"><span data-stu-id="dded3-181">Type</span></span>|<span data-ttu-id="dded3-182">Изменение целевой платформы</span><span class="sxs-lookup"><span data-stu-id="dded3-182">Retargeting</span></span>|
|<span data-ttu-id="dded3-183">Затронутые API</span><span class="sxs-lookup"><span data-stu-id="dded3-183">Affected APIs</span></span>|<ul><li><xref:System.Windows.Forms.ToolStripDropDownButton.CreateAccessibilityInstance?displayProperty=nameWithType></li><li><xref:System.Windows.Forms.DomainUpDown.DomainUpDownAccessibleObject.Name?displayProperty=nameWithType></li><li>[<span data-ttu-id="dded3-184">MonthCalendar.AccessibilityObject</span><span class="sxs-lookup"><span data-stu-id="dded3-184">MonthCalendar.AccessibilityObject</span></span>](xref:System.Windows.Forms.Control.AccessibilityObject)</li></ul>|
