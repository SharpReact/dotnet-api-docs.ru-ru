## <a name="introduction"></a>Вступление
Изменения при смене целевой платформы влияют на приложения, которые перекомпилируются с изменением целевой версии среды .NET Framework. В их число входят следующее.

* Изменения в среде разработки. Например, инструменты построения могут начать выдавать предупреждения, тогда как раньше они этого не делали.

* Изменения в среде выполнения. Влияют только на приложения, которые предназначены специально для новой целевой платформы .NET Framework. Приложения, которые предназначены для предыдущих версий .NET Framework, работают нормально.

В разделах с описанием изменений в среде выполнения используется следующая классификация отдельных элементов по их ожидаемому влиянию.

**Крупное изменение**. Это существенное изменение, влияющее на большое количество приложений или требующее объемного изменения кода.

**Небольшое изменение**. Это изменение влияет на небольшое количество приложений или требует незначительного изменения кода.

**Пограничный случай**. Это изменение влияет на приложения в исключительных ситуациях.

**Прозрачное изменение**. Это изменение не оказывает особого влияния на разработчиков и пользователей приложения. При этом вносить изменения в приложения не требуется.