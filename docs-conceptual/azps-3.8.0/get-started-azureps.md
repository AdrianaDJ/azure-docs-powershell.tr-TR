---
title: Azure PowerShell’i kullanmaya başlama
description: ''
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 04/24/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 6281ac5f6ec8941e0d5c1755f90f99552db9aa92
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89240769"
---
# <a name="get-started-with-azure-powershell"></a>Azure PowerShell’i kullanmaya başlama

Azure PowerShell, Azure kaynaklarını komut satırından yönetmek için tasarlanmıştır.
Azure Resource Manager modelini kullanan otomatik araçlar oluşturmak istediğinizde Azure PowerShell'i kullanın. Tarayıcınızda [Azure Cloud Shell](/azure/cloud-shell/overview) ile kullanmayı deneyin veya yerel makinenize yükleyin.

Bu makale Azure PowerShell'i kullanmaya başlamanıza yardımcı olur ve bu ürünün ardındaki temel kavramları öğretir.

## <a name="install-or-run-in-azure-cloud-shell"></a>Azure Cloud Shell'i yükleme veya çalıştırma

Azure PowerShell'i kullanmaya başlamanın en kolay yolu onu Azure Cloud Shell ortamında denemektir. Cloud Shell'i kullanmaya başlamak için bkz. [Azure Cloud Shell'de PowerShell için hızlı başlangıç](/azure/cloud-shell/quickstart-powershell). Cloud Shell, PowerShell’i bir Linux kapsayıcısında çalıştırır, dolayısıyla Windows’a özel işlevler kullanılamaz.

Yerel makinenize Azure PowerShell'i yüklemeye hazır olduğunuzda, [Azure PowerShell modülünü yükleme](install-az-ps.md) makalesindeki yönergeleri izleyin.

## <a name="sign-in-to-azure"></a>Azure'da oturum açma

[Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet’iyle etkileşimli olarak oturum açın. Cloud Shell kullanıyorsanız bu adımı atlayın. Azure Cloud Shell oturumunuz, Cloud Shell oturumunu başlatan ortam, abonelik ve kiracı için zaten kimlik doğrulaması yapmıştır.

```azurepowershell-interactive
Connect-AzAccount
```

Azure bulut hizmetleri, bölgesel veri işlemeyle ilgili yasalara uygun ortamlar sunar. Bölgesel buluttaki hesaplar için, oturum açmak amacıyla **Ortam** parametresini kullanın. [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet'ini kullanarak bölgeniz için ortamın adını alın.
Örneğin, Azure Çin 21Vianet'te oturum açmak için:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

Windows PowerShell 5.1 ortamlarında Azure hesabınızın kullanıcı adını ve parolasını sağlamak için bir oturum açma iletişim kutusu görüntülenir. PowerShell’in diğer tüm sürümlerinde [microsoft.com/devicelogin](https://microsoft.com/devicelogin) üzerinde kullanmak üzere bir belirteç alırsınız. Tarayıcınızda bu sayfayı açıp belirteci girin, ardından Azure hesabı kimlik bilgilerinizle oturum açın ve Azure PowerShell’i yetkilendirin.

Oturum açtıktan sonra, hangi Azure aboneliğinizin etkin olduğunu gösteren bilgiler göreceksiniz. Hesabınızda birden fazla Azure aboneliği bulunuyorsa ve farklı bir abonelik seçmek istiyorsanız, [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) ile kullanılabilir aboneliklerinizi alabilir ve abonelik kimliğiniz ile [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet’ini kullanabilirsiniz. Azure PowerShell’de Azure aboneliklerinizi yönetme hakkında daha fazla bilgi almak için bkz. [Birden fazla Azure aboneliği kullanma](manage-subscriptions-azureps.md).

Oturum açtıktan sonra, Azure PowerShell cmdlet'lerini kullanarak aboneliğinizdeki kaynaklara erişin ve bunları yönetin. Oturum açma işlemi ve kimlik doğrulama yöntemleri hakkında daha fazla bilgi edinmek için bkz. [Azure PowerShell ile oturum açma](authenticate-azureps.md).

## <a name="find-commands"></a>Komutları bulma

Azure PowerShell cmdlet'lerinde PowerShell için standart `Verb-Noun` adlandırma kuralına uyulur. Burada VERB (fiil) eylemi (örneğin `New`, `Get`, `Set`, `Remove`) ve NOUN (ad) da kaynak türünü (örneğin`AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`) belirtir. Azure PowerShell'de adlar her zaman `Az` ön ekiyle başlar. Standart fiillerin tam listesi için bkz. [PowerShell Komutları için onaylanmış fiiller](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands).

Kullanılabilir adları, fiilleri ve Azure PowerShell modüllerini bilmek, [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet'iyle komutları bulmanıza yardımcı olur. Örneğin, `Get` fiilinin kullanıldığı VM ile ilgili tüm komutları bulmak için:

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

Yaygın komutları bulmanıza yardımcı olmak için, bu tabloda `Get-Command` ile kullanılacak kaynak türü, ilgili Azure PowerShell modülü ve ad ön eki listelenir:

|                              Kaynak türü                              |                   Azure PowerShell modülü                    |    Ad ön eki     |
| ----------------------------------------------------------------------- | ------------------------------------------------------------ | ------------------ |
| [Kaynak grubu](/azure/azure-resource-manager/resource-group-overview) | [Az.Resources](/powershell/module/az.resources#resources)    | `AzResourceGroup`  |
| [Sanal makineler](/azure/virtual-machines)                             | [Az.Compute](/powershell/module/az.compute#virtual_machines) | `AzVM`             |
| [Depolama hesapları](/azure/storage/common/storage-introduction)          | [Az.Storage](/powershell/module/az.storage/)                 | `AzStorageAccount` |
| [Anahtar Kasası](/azure/key-vault/key-vault-whatis)                          | [Az.KeyVault](/powershell/module/az.keyvault)                | `AzKeyVault`       |
| [Web uygulamaları](/azure/app-service)                                  | [Az.Websites](/powershell/module/az.websites)                | `AzWebApp`         |
| [SQL veritabanları](/azure/sql-database)                                    | [Az.Sql](/powershell/module/az.sql)                          | `AzSqlDatabase`    |

Azure PowerShell'deki modüllerin tam listesi için, GitHub'da barındırılan [Azure PowerShell modül listesine](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) bakın.

## <a name="telemetry"></a>Telemetri

Azure PowerShell varsayılan olarak telemetri verilerini otomatik olarak toplar. Microsoft, kullanım desenlerini belirlemek, yaygın sorunları belirlemek ve Azure PowerShell deneyimini geliştirmek için toplanan verileri kümeler. Microsoft Azure PowerShell özel veya kişisel verileri toplamaz. Veri toplamayı devre dışı bırakmak için [Disable-AzDataCollection](/powershell/module/az.accounts/disable-azdatacollection) cmdlet’ini yürüterek açıkça devre dışı bırakmanız gerekir.

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a>Hızlı başlangıçlar ve öğreticiler ile Azure PowerShell'in temellerini öğrenme

Azure PowerShell'i kullanmaya başlamak için, sanal makineleri ayarlamaya ve bunların nasıl sorgulanacağını öğrenmeye yönelik ayrıntılı bir öğreticiyi deneyin.

> [!div class="nextstepaction"]
> [Azure PowerShell ile sanal makine oluşturma](azureps-vm-tutorial.yml)

Ayrıca diğer popüler Azure hizmetleri için de Azure PowerShell hızlı başlangıçları vardır:

* [Depolama hesabı oluşturma](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [Nesneleri Azure Blob depolamanın içine/dışına aktarma](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [Azure Key Vault'tan gizli anahtarlar oluşturma ve bunları alma](/azure/key-vault/quick-create-powershell)
* [Azure SQL veritabanı ve güvenlik duvarı oluşturma](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [Azure Container Instances’ta kapsayıcı çalıştırma](/azure/container-instances/container-instances-quickstart-powershell)
* [Sanal Makine Ölçek Kümesi oluşturma](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [Standart yük dengeleyici oluşturma](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a>Sonraki adımlar

* [Azure PowerShell ile oturum açma](authenticate-azureps.md)
* [Azure PowerShell ile Azure aboneliklerini yönetme](manage-subscriptions-azureps.md)
* [Azure PowerShell ile hizmet sorumluları oluşturma](create-azure-service-principal-azureps.md)
* Topluluktan yardım alın:
  * [MSDN'deki Azure forumu](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [Stack Overflow](https://go.microsoft.com/fwlink/?LinkId=320213)
