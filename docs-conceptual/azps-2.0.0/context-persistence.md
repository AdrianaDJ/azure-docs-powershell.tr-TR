---
title: Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme
description: Farklı PowerShell oturumlarında Azure kimlik bilgilerini ve diğer bilgileri yeniden kullanmayı öğrenin.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 8702de48429482748939fb1a43ff911bed15f6c0
ms.sourcegitcommit: accff0c2cd6035fcda2d917f6051a5b509eb6255
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/06/2019
ms.locfileid: "65048572"
---
# <a name="persist-user-credentials-across-powershell-sessions"></a>Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme

Azure PowerShell aşağıdaki özellikleri getiren **Azure Context Autosave** adlı bir özellik sunar:

- Yeni PowerShell oturumlarında yeniden kullanım için oturum açma bilgilerini tutma.
- Uzun süre çalışan cmdlet'leri yürütmek için arka plan görevlerini daha kolay kullanma.
- Ayrı bir oturum açma olmadan hesaplar, abonelikler ve ortamlar arasında geçiş yapma.
- Farklı kimlik bilgileri ve abonelikler kullanarak, görevleri aynı PowerShell oturumundan aynı anda yürütme.

## <a name="azure-contexts-defined"></a>Tanımlanan Azure bağlamları

*Azure bağlamı*, Azure PowerShell cmdlet’lerinin hedefini tanımlayan bilgiler kümesidir. Bağlam beş bölümden oluşur:

- *Hesap* - Azure ile iletişimin kimliğini doğrulamak için kullanılan UserName veya Hizmet Sorumlusu
- *Abonelik* - Üzerinde işlem yapılan Kaynakların bulunduğu Azure Aboneliği.
- *Kiracı* - Aboneliğinizi içeren Azure Active Directory kiracısı. Kiracılar ServicePrincipal kimlik doğrulaması için daha önemlidir.
- *Ortam* - Hedeflenen Azure Bulutu, genellikle Azure genel bulutudur.
  Ancak, ortamı ayarı Ulusal, Kamu ve şirket içi (Azure Stack) bulutları da hedeflemenize olanak tanır.
- *Kimlik Bilgileri* - Kimliğinizi doğrulamak ve Azure’daki kaynaklara erişim yetkinizi onaylamak için Azure tarafından kullanılan bilgiler

Azure PowerShell’in son sürümüyle birlikte, her yeni PowerShell oturumunun açılışında Azure Bağlamları otomatik olarak kaydedilebilir.

## <a name="automatically-save-the-context-for-the-next-sign-in"></a>Sonraki oturum için bağlamı otomatik olarak kaydetme

Azure PowerShell, oturumlar arasında bağlam bilgilerinizi otomatik olarak tutar. PowerShell’i bağlam ve kimlik bilgilerinizi unutacak şekilde ayarlamak için `Disable-AzContextAutoSave` seçeneğini kullanın. Bağlam kaydetme devre dışı bırakıldığında, açtığınız her PowerShell oturumunda Azure oturumu açmanız gerekecektir.

Azure PowerShell’in PowerShell oturumu kapatıldıktan sonra bağlamınızı hatırlamasına izin vermek için `Enable-AzContextAutosave` kullanın. Bağlam ve kimlik bilgileri, kullanıcı dizininizdeki (Windows’da `$env:USERPROFILE\.Azure`, diğer platformlarda `$HOME/.Azure`) özel bir gizli klasöre otomatik olarak kaydedilir. Her yeni PowerShell oturumu son oturumunuzda kullanılan bağlamı hedefler.

Azure bağlamlarını yönetmenizi sağlayan cmdlet’ler, hassas denetime de olanak tanır. Değişikliklerin yalnızca mevcut PowerShell oturumunda (`Process` kapsamı) veya her PowerShell oturumunda (`CurrentUser` kapsamı) geçerli olmasını istiyorsanız. Bu seçenekler [Bağlam Kapsamlarını Kullanma](#Using-Context-Scopes) bölümünde daha ayrıntılı olarak ele alınmıştır.

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a>Azure PowerShell cmdlet'lerini arka plan işleri olarak çalıştırma

**Azure Bağlam Otomatik Kaydı** özelliği ayrıca bağlamınızı PowerShell arka plan işleri ile paylaşmanıza olanak tanır. PowerShell, uzun süre yürütülen görevlerin tamamlanmasını beklemek zorunda kalmadan görevleri arka plan işleri olarak başlatıp izlemenizi sağlar. Kimlik bilgilerini arka plan işleri ile iki farklı şekilde paylaşabilirsiniz:

- Bağlamı bağımsız değişken olarak geçirme

  Birçok AzureRM cmdlet’i, bağlamı cmdlet’e parametre olarak geçirmenize olanak tanır. Bağlamı bir arka plan işine aşağıdaki örnekte gösterildiği gibi geçirebilirsiniz:

  ```powershell-interactive
  PS C:\> $job = Start-Job { param ($ctx) New-AzVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzContext)
  ```

- Otomatik kaydetme etkinken varsayılan bağlamı kullanma

  **Bağlam Otomatik Kaydı**’nı etkinleştirdiyseniz, arka plan işlerinde otomatik olarak kayıtlı varsayılan bağlam kullanılır.

  ```powershell-interactive
  PS C:\> $job = Start-Job { New-AzVm [... Additional parameters ...]}
  ```

Arka plan görevinin sonucunu öğrenmek istediğiniz, `Get-Job` seçeneğini kullanarak iş durumunu denetleyin ve `Wait-Job` ile İşin tamamlanmasını bekleyin. Arka plan işinin çıktısını yakalamak veya görüntülemek için `Receive-Job` seçeneğini kullanın. Daha fazla bilgi için bkz. [İşler hakkında](/powershell/module/microsoft.powershell.core/about/about_jobs).

## <a name="creating-selecting-renaming-and-removing-contexts"></a>Bağlam oluşturma, seçme, yeniden adlandırma ve kaldırma

Bağlam oluşturmak için Azure'da oturum açmanız gerekir. `Connect-AzAccount` cmdlet’i (veya diğer adıyla `Login-AzAccount`), Azure PowerShell cmdlet’leri tarafından kullanılan varsayılan bağlamı ayarlar ve kimlik bilgilerinizin izin verdiği tüm kiracı ya da aboneliklere erişmenize olanak tanır.

Oturum açtıktan sonra yeni bir bağlam eklemek için `Set-AzContext` (veya diğer adıyla `Select-AzSubscription`) cmdlet’ini kullanın.

```azurepowershell-interactive
PS C:\> Set-AzContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

Önceki örnekte, mevcut kimlik bilgileriniz kullanılarak 'Contoso Aboneliği 1'’i hedefleyen yeni bir bağlam eklenmiştir. Yeni bağlam 'Contoso1' olarak adlandırılır. Bağlam için ad belirtmezseniz, hesap kimliği ve abonelik kimliğinin kullanıldığı varsayılan bir ad kullanılır.

Var olan bir bağlamı yeniden adlandırmak için `Rename-AzContext` cmdlet'ini kullanın. Örnek:

```azurepowershell-interactive
PS C:\> Rename-AzContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

Bu örnekte, otomatik adı `[user1@contoso.org; 123456-7890-1234-564321]` olan bağlam 'Contoso2' basit adıyla yeniden adlandırılmaktadır. Bağlamları yöneten cmdlet’ler aynı zamanda sekme tamamlamayı kullanarak bağlamı hızlıca seçmenize olanak tanır.

Son olarak, bir bağlamı kaldırmak için `Remove-AzContext` cmdlet'ini kullanın.  Örnek:

```azurepowershell-interactive
PS C:\> Remove-AzContext Contoso2
```

'Contoso2' adlı bağlamı unutur. Bu bağlamı `Set-AzContext` kullanarak yeniden oluşturabilirsiniz

## <a name="removing-credentials"></a>Kimlik bilgilerini kaldırma

`Disconnect-AzAccount` (aynı zamanda `Logout-AzAccount` olarak bilinir) kullanarak bir kullanıcı ya da hizmet sorumlusuna ait tüm kimlik bilgilerini ve ilişkili bağlamları kaldırabilirsiniz. Parametre olmadan çalıştırıldığında, `Disconnect-AzAccount` cmdlet'i mevcut bağlamda Kullanıcı veya Hizmet Sorumlusu ile ilişkili tüm kimlik bilgilerini ve bağlamları kaldırır. Belirli bir sorumluyu hedeflemek için bir Kullanıcı Adı, Hizmet Asıl Adı ya da bağlam geçirebilirsiniz.

```azurepowershell-interactive
Disconnect-AzAccount user1@contoso.org
```

## <a name="using-context-scopes"></a>Bağlam kapsamlarını kullanma

Bazı durumlarda, diğer oturumları etkilemeden bir PowerShell oturumundaki bağlamı seçmek, değiştirmek ya da kaldırmak isteyebilirsiniz. Bağlam cmdlet'lerinin varsayılan davranışını değiştirmek için `Scope` parametresini kullanın. `Process` kapsamı yalnızca mevcut oturum için geçerli olmasını sağlayarak varsayılan davranışı geçersiz kılar. Buna karşılık `CurrentUser` kapsamı, yalnızca mevcut oturum yerine tüm oturumlardaki bağlamı değiştirir.

Örnek olarak, diğer pencereleri etkilemeden mevcut PowerShell oturumundaki varsayılan bağlamı veya açılan bir sonraki oturumda kullanılan bağlamı değiştirmek için şunu kullanın:

```azurepowershell-interactive
PS C:\> Select-AzContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a>Bağlam otomatik kaydetme ayarını hatırlama

Bağlam Otomatik Kaydetme ayarı, kullanıcının Azure PowerShell dizinine (Windows’da `$env:USERPROFILE\.Azure`, diğer platformlarda `$HOME/.Azure`) kaydedilir. Bilgisayar hesaplarının bazı türleri bu dizine erişemeyebilir. Bu tür senaryolar için ortam değişkenini kullanabilirsiniz

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

Bağlam 'true' olarak ayarlandığında otomatik olarak kaydedilir. Bağlam 'false' olarak ayarlanırsa kaydedilmez.

## <a name="context-management-cmdlets"></a>Bağlam yönetimi cmdlet'leri

- [Enable-AzContextAutosave][enable] - Powershell oturumları arasında bağlamı kaydetmeye olanak tanır.
  Her türlü değişiklik, genel bağlamı değiştirir.
- [Disable-AzContextAutosave][disable] - Bağlamı otomatik kaydetmeyi kapatır. Her yeni PowerShell oturumunda yeniden oturum açmak gerekir.
- [Select-AzContext][select] - Bir bağlamı varsayılan bağlam olarak seçer. Tüm cmdlet'ler kimlik doğrulaması için bu bağlamdaki kimlik bilgilerini kullanır.
- [Disconnect-AzAccount][remove-cred] - Bir hesapla ilişkili tüm kimlik bilgilerini ve bağlamları kaldırır.
- [Remove-AzContext][remove-context] - Adlandırılmış bir bağlamı kaldırır.
- [Rename-AzContext][rename] - Mevcut bir bağlamı yeniden adlandırır.
- [Add-AzAccount][login] - İşlem veya mevcut kullanıcı için oturum açma kapsamının ayarlanmasına izin verir.
  Kimlik doğrulamasından sonra varsayılan bağlamı adlandırmaya olanak tanır.
- [Import-AzContext][import] - İşlem veya mevcut kullanıcı için oturum açma kapsamının ayarlanmasına izin verir.
- [Set-AzContext][set-context] - Mevcut adlandırılmış bağlamların ve işlem ya da mevcut kullanıcı kapsam değişikliklerinin seçilmesine olanak tanır.

<!-- Hyperlinks -->
[enable]: /powershell/module/az.accounts/Enable-AzureRmContextAutosave
[disable]: /powershell/module/az.accounts/Disable-AzContextAutosave
[select]: /powershell/module/az.accounts/Select-AzContext
[remove-cred]: /powershell/module/az.accounts/Disconnect-AzAccount
[remove-context]: /powershell/module/az.accounts/Remove-AzContext
[rename]: /powershell/module/az.accounts/Rename-AzContext

<!-- Updated cmdlets -->
[login]: /powershell/module/az.accounts/Connect-AzAccount
[import]:  /powershell/module/az.accounts/Import-AzContext
[set-context]: /powershell/module/az.accounts/Set-AzContext
