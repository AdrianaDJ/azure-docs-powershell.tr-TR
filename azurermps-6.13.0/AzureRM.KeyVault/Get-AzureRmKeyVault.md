---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: d79c28b09c9f6ca36ae163566574555bb3c50459
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763844"
---
# <span data-ttu-id="1f71f-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="1f71f-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="1f71f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f71f-102">SYNOPSIS</span></span>
<span data-ttu-id="1f71f-103">Tuş</span><span class="sxs-lookup"><span data-stu-id="1f71f-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f71f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f71f-104">SYNTAX</span></span>

### <span data-ttu-id="1f71f-105">Listallvaultsınsubscription (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1f71f-105">ListAllVaultsInSubscription (Default)</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f71f-106">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="1f71f-106">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f71f-107">Bydeletedkasası</span><span class="sxs-lookup"><span data-stu-id="1f71f-107">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f71f-108">Listalldeletedvaultsınsubscription</span><span class="sxs-lookup"><span data-stu-id="1f71f-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f71f-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f71f-109">DESCRIPTION</span></span>
<span data-ttu-id="1f71f-110">**Get-Azurermkeykasa** cmdlet 'i, bir abonelikteki Anahtar Kasası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="1f71f-110">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="1f71f-111">Bir abonelikteki tüm önemli kasa örneklerini görüntüleyebilir ya da sonuçlarınızı bir kaynak grubuna veya belirli bir anahtar kasaya göre filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f71f-111">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>
<span data-ttu-id="1f71f-112">Tek bir Anahtar Kasası aldığınızda bu cmdlet için kaynak grubu 'nun isteğe bağlı olduğunu belirten unutmayın, daha iyi performans için bunu yapmalısınız.</span><span class="sxs-lookup"><span data-stu-id="1f71f-112">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="1f71f-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f71f-113">EXAMPLES</span></span>

### <span data-ttu-id="1f71f-114">Örnek 1: geçerli aboneliğinizdeki tüm tuş örneklerini alın</span><span class="sxs-lookup"><span data-stu-id="1f71f-114">Example 1: Get all key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzureRMKeyVault

Vault Name          : myvault1
Resource Group Name : myrg
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.Ke
                      yVault/vaults/myvault1
Tags                :


Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="1f71f-115">Bu komut geçerli aboneliğinizdeki tüm anahtarı getirir.</span><span class="sxs-lookup"><span data-stu-id="1f71f-115">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="1f71f-116">Örnek 2: belirli bir Anahtar Kasası alma</span><span class="sxs-lookup"><span data-stu-id="1f71f-116">Example 2: Get a specific key vault</span></span>
```powershell
PS C:\> Get-AzureRMKeyVault -VaultName 'myvault'

Vault Name                       : myvault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/myvault
Vault URI                        : https://myvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : True
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update

Tags                             :
```

<span data-ttu-id="1f71f-117">Bu komut, geçerli aboneliğinizde mykasası adındaki anahtar kasayı alır.</span><span class="sxs-lookup"><span data-stu-id="1f71f-117">This command gets the key vault named myvault in your current subscription.</span></span>

### <span data-ttu-id="1f71f-118">Örnek 3: kaynak grubundaki tuş örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="1f71f-118">Example 3: Get key vaults in a resource group</span></span>
```powershell
PS C:\> Get-AzureRmKeyVault -ResourceGroupName 'myrg1'

Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="1f71f-119">Bu komut, ContosoPayRollResourceGroup adlı kaynak grubundaki tüm anahtarı getirir.</span><span class="sxs-lookup"><span data-stu-id="1f71f-119">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="1f71f-120">Örnek 4: geçerli aboneliğinizde tüm silinmiş anahtar örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="1f71f-120">Example 4: Get all deleted key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzureRmKeyVault -InRemovedState

Vault Name           : myvault4
Location             : westus
Id                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/providers/Microsoft.KeyVault/locations/westu
                       s/deletedVaults/myvault4
Resource ID          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.K
                       eyVault/vaults/myvault4
Deletion Date        : 5/24/2018 9:33:24 PM
Scheduled Purge Date : 8/22/2018 9:33:24 PM
Tags                 :
```

<span data-ttu-id="1f71f-121">Bu komut geçerli aboneliğinizde tüm silinmiş anahtar yerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="1f71f-121">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="1f71f-122">Örnek 5: silinen bir Anahtar Kasası alma</span><span class="sxs-lookup"><span data-stu-id="1f71f-122">Example 5: Get a deleted key vault</span></span>
```powershell
PS C:\> Get-AzureRMKeyVault -VaultName 'myvault4'  -Location 'westus' -InRemovedState

Vault Name           : myvault4
Location             : westus
Id                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/providers/Microsoft.KeyVault/locations/westu
                       s/deletedVaults/myvault4
Resource ID          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.K
                       eyVault/vaults/myvault4
Deletion Date        : 5/24/2018 9:33:24 PM
Scheduled Purge Date : 8/22/2018 9:33:24 PM
Tags                 :
```

<span data-ttu-id="1f71f-123">Bu komut, geçerli aboneliğinizde ve westus bölgesinde myvault4 adlı silinmiş Anahtar Kasası bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="1f71f-123">This command gets the deleted key vault information named myvault4 in your current subscription and in westus region.</span></span>

## <span data-ttu-id="1f71f-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f71f-124">PARAMETERS</span></span>

### <span data-ttu-id="1f71f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f71f-125">-DefaultProfile</span></span>
<span data-ttu-id="1f71f-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1f71f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f71f-127">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="1f71f-127">-InRemovedState</span></span>
<span data-ttu-id="1f71f-128">Çıktıda önceden silinmiş olan kasa gösterilip gösterilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f71f-128">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f71f-129">-Konum</span><span class="sxs-lookup"><span data-stu-id="1f71f-129">-Location</span></span>
<span data-ttu-id="1f71f-130">Silinmiş kasanın konumu.</span><span class="sxs-lookup"><span data-stu-id="1f71f-130">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f71f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f71f-131">-ResourceGroupName</span></span>
<span data-ttu-id="1f71f-132">Sorgulanan Anahtar Kasası veya anahtar kasası ile ilişkili kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f71f-132">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f71f-133">Etiketli</span><span class="sxs-lookup"><span data-stu-id="1f71f-133">-Tag</span></span>
<span data-ttu-id="1f71f-134">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="1f71f-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1f71f-135">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="1f71f-135">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f71f-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1f71f-136">-VaultName</span></span>
<span data-ttu-id="1f71f-137">Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f71f-137">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f71f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f71f-138">CommonParameters</span></span>
<span data-ttu-id="1f71f-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f71f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f71f-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f71f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f71f-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f71f-141">INPUTS</span></span>

### <span data-ttu-id="1f71f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1f71f-142">System.String</span></span>

### <span data-ttu-id="1f71f-143">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1f71f-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1f71f-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f71f-144">OUTPUTS</span></span>

### <span data-ttu-id="1f71f-145">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="1f71f-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="1f71f-146">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultidentityıtem</span><span class="sxs-lookup"><span data-stu-id="1f71f-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="1f71f-147">Microsoft.Azure.Commands.KeyVault.Models.PSDEleditedtuş Kasası</span><span class="sxs-lookup"><span data-stu-id="1f71f-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="1f71f-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f71f-148">NOTES</span></span>

## <span data-ttu-id="1f71f-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f71f-149">RELATED LINKS</span></span>

[<span data-ttu-id="1f71f-150">Yeni-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="1f71f-150">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="1f71f-151">Remove-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="1f71f-151">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
