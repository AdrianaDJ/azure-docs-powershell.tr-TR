---
title: Azure bağlamları ve oturum açma bilgileri
description: Farklı PowerShell oturumlarında Azure kimlik bilgilerini ve diğer bilgileri yeniden kullanmayı öğrenin.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.openlocfilehash: 72d1b07bb2c66f80ea6f5d37ef7012d0d0a5bbbc
ms.sourcegitcommit: 05431341858d10eb9c345213275c3ccc24c83c9b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/13/2019
ms.locfileid: "74062505"
---
# <a name="azure-powershell-context-objects"></a>Azure PowerShell bağlam nesneleri

Azure PowerShell abonelik ve kimlik doğrulaması bilgilerini tutmak için _Azure PowerShell bağlam nesneleri_ (Azure bağlamları) kullanır. Birden fazla aboneliğiniz varsa, Azure bağlamları Azure PowerShell cmdlet'lerinin üzerinde çalıştırılacağı aboneliği seçmenizi sağlar. Azure bağlamları birden fazla PowerShell oturumunda oturum açma bilgilerini depolamak ve arka plan görevlerini çalıştırmak için de kullanılır.

Bu makalede aboneliklerin veya hesapların yönetimi değil Azure bağlamlarının yönetimi açıklanır. Kullanıcıları, abonelikleri, kiracıları veya diğer hesap bilgilerini yönetme konusunu arıyorsanız [Azure Active Directory](/azure/active-directory) belgelerine bakın. Bağlamları kullanarak arka plan görevlerini veya paralel görevleri çalıştırmayı öğrenmek için, Azure bağlamlarını anladıktan sonra [PowerShell işlerinde Azure PowerShell cmdlet'lerini kullanma](using-psjobs.md) belgesine bakın.

## <a name="overview-of-azure-context-objects"></a>Azure bağlam nesnelerine genel bakış

Azure bağlamları, üzerinde komutların çalıştırılacağı etkin aboneliğinizi ve Azure bulutuna bağlanmak için gereken kimlik doğrulama bilgilerini temsil eden PowerShell nesneleridir. Azure bağlamlarıyla, Azure PowerShell'in her abonelik değiştirdiğinizde kimliğinizi yeniden doğrulaması gerekmez. Azure bağlamı şunlardan oluşur:

* [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) ile Azure'da oturum açarken kullanılmış olan _hesap_. Azure bağlamları, hesap açısından kullanıcıları, uygulama kimliklerini ve hizmet sorumlularını aynı şekilde değerlendirir.
* _Kiracı_ ile ilişkilendirilmiş Azure kaynaklarını oluşturmak ve çalıştırmak için Microsoft'la yapılan bir hizmet sözleşmesi olan etkin _abonelik_. Belgelerde ve Active Directory ile çalışırken kiracılardan genellikle _kuruluşlar_ olarak söz edilir.
* Azure bulutuna erişmek için depolanan kimlik doğrulama belirteci olan _belirteç önbelleği_ başvurusu. Bu belirtecin nerede depolandığı ve ne kadar süreyle kalıcı olacağı [bağlam otomatik kaydetme ayarları](#save-azure-contexts-across-powershell-sessions) tarafından belirlenir.

Bu terimlerle ilgili daha fazla bilgi için bkz. [Azure Active Directory Terminolojisi](/azure/active-directory/fundamentals/active-directory-whatis#terminology). Azure bağlamları tarafından kullanılan kimlik doğrulama belirteçleri, kalıcı bir oturumun parçası olan diğer depolanmış belirteçlerle aynıdır. 

`Connect-AzAccount` ile oturum açtığınızda varsayılan aboneliğiniz için en az bir Azure bağlamı oluşturulur. `Connect-AzAccount` tarafından döndürülen nesne, PowerShell oturumunun kalanında kullanılan varsayılan Azure bağlamıdır.

## <a name="get-azure-contexts"></a>Azure bağlamlarını alma

Kullanılabilir Azure bağlamları [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet'iyle alınır. Tüm kullanılabilir bağlamları listelemek için `-ListAvailable` kullanın:

```azurepowershell-interactive
Get-AzContext -ListAvailable
```

İsterseniz bağlamı adını belirterek de alabilirsiniz:

```azurepowershell-interactive
$context = Get-Context -Name "mycontext"
```

Bağlam adları, ilişkili aboneliğin adından farklı olabilir.

> [!IMPORTANT]
> Kullanılabilir Azure bağlamları her zaman sizin kullanılabilir abonelikleriniz __olmayabilir__. Azure bağlamları yalnızca yerel olarak depolanmış bilgileri temsil eder. Aboneliklerinizi [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription?view=azps-1.8.0) cmdlet'iyle alabilirsiniz.

## <a name="create-a-new-azure-context-from-subscription-information"></a>Abonelik bilgilerinden yeni Azure bağlamı oluşturma

Hem yeni Azure bağlamlarını oluşturmak hem de bunları etkin bağlam olarak ayarlamak için [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) cmdlet'i kullanılır.
Yeni Azure bağlamı oluşturmanın en kolay yolu mevcut abonelik bilgilerini kullanmaktır. Cmdlet, çıkış nesnesini `Get-AzSubscription` cmdlet'inden yönlendirilmiş değer olarak alacak ve yeni Azure bağlamını yapılandıracak şekilde tasarlanmıştır:

```azurepowershell-interactive
Get-AzSubscription -SubscriptionName 'MySubscriptionName' | Set-AzContext -Name 'MyContextName'
```

Gerekirse abonelik adını veya kimliğini ve kiracı kimliğini de verebilirsiniz:

```azurepowershell-interactive
Set-AzContext -Name 'MyContextName' -Subscription 'MySubscriptionName' -Tenant '.......'
```

`-Name` bağımsız değişkeni atlanırsa, bağlam adı olarak `Subscription Name (subscription-id)` biçiminde aboneliğin adı ve kimliği kullanılır.

## <a name="change-the-active-azure-context"></a>Etkin Azure bağlamını değiştirme

Etkin Azure bağlamını değiştirmek için hem `Set-AzContext` hem de [Select-AzContext](/powershell/module/az.accounts/set-azcontext) kullanılabilir. [Yeni Azure bağlamı oluşturma](#create-a-new-azure-context-from-subscription-information) bölümünde açıklandığı gibi, abonelik için Azure bağlamı yoksa `Set-AzContext` yeni bir Azure bağlamı oluşturur ve ardından etkin bağlam olarak bunu kullanmaya geçer.

`Select-AzContext` cmdlet'inin yalnızca mevcut Azure bağlamlarıyla kullanılması amaçlanmıştır ve `Set-AzContext -Context` kullanımına benzer şekilde çalışır ama yönlendirmeyle kullanılacak şekilde tasarlanmıştır:

```azurepowershell-interactive
Set-AzContext -Context $(Get-AzContext -Name "mycontext") # Set a context with an inline Azure context object
Get-AzContext -Name "mycontext" | Select-AzContext # Set a context with a piped Azure context object
```

Azure PowerShell'deki diğer birçok hesap ve bağlam yönetimi komutu gibi `Set-AzContext` ve `Select-AzContext` de `-Scope` bağımsız değişkenini desteklendiğinden bağlamın ne kadar süreyle etkin olacağını denetleyebilirsiniz. `-Scope`, varsayılanı değiştirmeden tek oturumun etkin bağlamını değiştirmenizi sağlar:

```azurepowershell-interactive
Get-AzContext -Name "mycontext" | Select-AzContext -Scope Process
```

PowerShell oturumunun tamamında bağlamların değiştirilmesini önlemek için, tüm Azure PowerShell komutları `-AzContext` bağımsız değişkeniyle verilen bir bağlamda çalıştırılabilir:

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
New-AzVM -Name ExampleVM -AzContext $context
```

Azure PowerShell cmdlet'lerinde bağlamların diğer önemli kullanım şekli arka plan komutlarını çalıştırmaktır. Azure PowerShell kullanarak PowerShell İşlerini çalıştırma hakkında daha fazla bilgi edinmek için bkz. [PowerShell İşlerinde Azure PowerShell cmdlet'lerini çalıştırma](using-psjobs.md).

## <a name="save-azure-contexts-across-powershell-sessions"></a>PowerShell oturumları arasında Azure bağlamlarını kaydetme

Azure bağlamları varsayılan olarak PowerShell oturumları arasında kullanılmak üzere kaydedilir. Bu davranışı aşağıdaki yollarla değiştirebilirsiniz:

* `Connect-AzAccount` cmdlet'iyle `-Scope Process` kullanarak oturum açın.

  ```azurepowershell
  Connect-AzAccount -Scope Process
  ```

  Bu oturum açma işleminin bir parçası olarak döndürülen Azure bağlamı _yalnızca_ güncel oturumda geçerlidir ve Azure PowerShell bağlam otomatik kaydetme ayarı ne olursa olsun otomatik olarak kaydedilmez.
* Azure PowerShell'in bağlam otomatik kaydetme ayarını [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave) cmdlet'iyle devre dışı bırakın.
  Bağlam otomatik kaydetme ayarı devre dışı bırakıldığında depolanmış olan belirteçler __temizlenmez__. Depolanan Azure bağlam bilgilerini temizlemeyi öğrenmek için bkz. [Azure bağlamlarını ve kimlik bilgilerini kaldırma](#remove-azure-contexts-and-stored-credentials).
* Azure bağlamı otomatik kaydetme ayarını [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave) cmdlet'iyle açıkça etkinleştirin. Otomatik kaydetme etkinleştirildiğinde kullanıcının tüm bağlamları sonraki PowerShell oturumları için yerel olarak depolanır.
* Bağlamları gelecekteki PowerShell oturumlarında kullanılmak üzere [Save-AzContext](/powershell/module/az.accounts/save-azcontext) cmdlet'iyle el ile kaydedin. Bunlar sonraki oturumlarda [Import-AzContext](/powershell/module/az.accounts/import-azcontext) cmdlet'iyle yüklenebilir:

  ```azurepowershell
  Save-AzContext -Path current-context.json # Save the current context
  Save-AzContext -Profile $profileObject -Path other-context.json # Save a context object
  Import-AzContext -Path other-context.json # Load the context from a file and set it to the current context
  ```

> [!WARNING]
> Bağlam otomatik kaydetme ayarı devre dışı bırakıldığında, daha önce kaydedilmiş olan depolanan bağlam bilgileri __temizlenmez__. Depolanan bilgileri kaldırmak için [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext) cmdlet'ini kullanın. Kaydedilmiş bağlamları kaldırma hakkında daha fazla bilgi için bkz. [Bağlamları ve kimlik bilgilerini kaldırma](#remove-azure-contexts-and-stored-credentials).

Bu komutların her biri, yalnızca çalışan işleme uygulamak üzere `Process` değerini alabilen `-Scope` parametresini destekler. Örneğin, yeni oluşturulan bağlamların PowerShell oturumundan çıkarken kaydedilmemesini sağlamak için:

```azurepowershell-interactive
Disable-AzContextAutosave -Scope Process
$context2 = Set-AzContext -Subscription "sub-id" -Tenant "other-tenant"
```

Bağlam bilgileri ve belirteçler Windows'da `$env:USERPROFILE\.Azure` dizininde ve diğer platformlarda `$HOME/.Azure` konumunda depolanır. Abonelik kimlikleri ve kiracı kimlikleri gibi hassas bilgiler yine de günlükler ve kaydedilmiş bağlamlar aracılığıyla depolanan bilgilerde kullanıma sunuluyor olabilir. Depolanan bilgileri temizlemeyi öğrenmek için bkz. [Bağlamları ve kimlik bilgilerini kaldırma](#remove-azure-contexts-and-stored-credentials).

## <a name="remove-azure-contexts-and-stored-credentials"></a>Azure bağlamlarını ve depolanan kimlik bilgilerini kaldırma

Azure bağlamlarını ve kimlik bilgilerini temizlemek için:

* [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount) ile bir hesabın oturumunu kapatın.
  Hesabın oturumunu hesaba veya bağlama göre kapatabilirsiniz:

  ```azurepowershell-interactive
  Disconnect-AzAccount # Disconnect active account 
  Disconnect-AzAccount -Username "user@contoso.com" # Disconnect by account name

  Disconnect-AzAccount -ContextName "subscription2" # Disconnect by context name
  Disconnect-AzAccount -AzureContext $contextObject # Disconnect using context object information
  ```

  Bağlantının kesilmesi her zaman depolanan kimlik doğrulama belirteçlerini kaldırır ve bağlantısı kesilmiş kullanıcıyla veya bağlamla ilişkili kaydedilmiş bağlamları temizler.
* [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext) cmdlet'ini kullanın. Bu cmdlet, her zaman depolanan bağlamlarla kimlik doğrulama belirteçlerinin kaldırılmasını garanti eder, ayrıca oturumunuzu da kapatır.
* Bağlamı [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext) ile kaldırın:
  
  ```azurepowershell-interactive
  Remove-AzContext -Name "mycontext" # Remove by name
  Get-AzContext -Name "mycontext" | Remove-AzContext # Remove by piping Azure context object
  ```

  Etkin bağlamı kaldırırsanız Azure'la bağlantınız kesilir ve `Connect-AzAccount` ile yeniden kimlik doğrulaması yapmanız gerekir.

## <a name="see-also"></a>Ayrıca bkz.

* [PowerShell İşlerinde Azure PowerShell cmdlet'lerini çalıştırma](using-psjobs.md)
* [Azure Active Directory Terminolojisi](/azure/active-directory/fundamentals/active-directory-whatis#terminology)
* [Az.Accounts başvurusu](/powershell/module/az.accounts)
