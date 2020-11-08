---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
ms.openlocfilehash: cb1c4f901c598ec20af13e87707966704b285c64
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108226"
---
# <span data-ttu-id="f1c50-101">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="f1c50-101">Get-AzKeyVault</span></span>

## <span data-ttu-id="f1c50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1c50-102">SYNOPSIS</span></span>
<span data-ttu-id="f1c50-103">Tuş</span><span class="sxs-lookup"><span data-stu-id="f1c50-103">Gets key vaults.</span></span>

## <span data-ttu-id="f1c50-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1c50-104">SYNTAX</span></span>

### <span data-ttu-id="f1c50-105">GetVaultByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f1c50-105">GetVaultByName (Default)</span></span>
```
Get-AzKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1c50-106">Bydeletedkasası</span><span class="sxs-lookup"><span data-stu-id="f1c50-106">ByDeletedVault</span></span>
```
Get-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1c50-107">Listalldeletedvaultsınsubscription</span><span class="sxs-lookup"><span data-stu-id="f1c50-107">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1c50-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1c50-108">DESCRIPTION</span></span>
<span data-ttu-id="f1c50-109">**Get-Azanahtarkasası** cmdlet 'i, bir abonelikteki Anahtar Kasası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="f1c50-109">The **Get-AzKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="f1c50-110">Bir abonelikteki tüm önemli kasa örneklerini görüntüleyebilir ya da sonuçlarınızı bir kaynak grubuna veya belirli bir anahtar kasaya göre filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f1c50-110">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>
<span data-ttu-id="f1c50-111">Tek bir Anahtar Kasası aldığınızda bu cmdlet için kaynak grubu 'nun isteğe bağlı olduğunu belirten unutmayın, daha iyi performans için bunu yapmalısınız.</span><span class="sxs-lookup"><span data-stu-id="f1c50-111">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="f1c50-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1c50-112">EXAMPLES</span></span>

### <span data-ttu-id="f1c50-113">Örnek 1: geçerli aboneliğinizdeki tüm tuş örneklerini alın</span><span class="sxs-lookup"><span data-stu-id="f1c50-113">Example 1: Get all key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVault

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

<span data-ttu-id="f1c50-114">Bu komut geçerli aboneliğinizdeki tüm anahtarı getirir.</span><span class="sxs-lookup"><span data-stu-id="f1c50-114">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="f1c50-115">Örnek 2: belirli bir Anahtar Kasası alma</span><span class="sxs-lookup"><span data-stu-id="f1c50-115">Example 2: Get a specific key vault</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault'

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

<span data-ttu-id="f1c50-116">Bu komut, geçerli aboneliğinizde mykasası adındaki anahtar kasayı alır.</span><span class="sxs-lookup"><span data-stu-id="f1c50-116">This command gets the key vault named myvault in your current subscription.</span></span>

### <span data-ttu-id="f1c50-117">Örnek 3: kaynak grubundaki tuş örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="f1c50-117">Example 3: Get key vaults in a resource group</span></span>
```powershell
PS C:\> Get-AzKeyVault -ResourceGroupName 'myrg1'

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

<span data-ttu-id="f1c50-118">Bu komut, ContosoPayRollResourceGroup adlı kaynak grubundaki tüm anahtarı getirir.</span><span class="sxs-lookup"><span data-stu-id="f1c50-118">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="f1c50-119">Örnek 4: geçerli aboneliğinizde tüm silinmiş anahtar örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="f1c50-119">Example 4: Get all deleted key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVault -InRemovedState

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

<span data-ttu-id="f1c50-120">Bu komut geçerli aboneliğinizde tüm silinmiş anahtar yerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="f1c50-120">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="f1c50-121">Örnek 5: silinen bir Anahtar Kasası alma</span><span class="sxs-lookup"><span data-stu-id="f1c50-121">Example 5: Get a deleted key vault</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault4'  -Location 'westus' -InRemovedState

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

<span data-ttu-id="f1c50-122">Bu komut, geçerli aboneliğinizde ve westus bölgesinde myvault4 adlı silinmiş Anahtar Kasası bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="f1c50-122">This command gets the deleted key vault information named myvault4 in your current subscription and in westus region.</span></span>

### <span data-ttu-id="f1c50-123">Örnek 6: filtreleme kullanarak tuş örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="f1c50-123">Example 6: Get key vaults using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault*'

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

<span data-ttu-id="f1c50-124">Bu komut, abonelikteki "mykasa" ile başlayan tüm tuş yerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="f1c50-124">This command gets all the key vaults in the subscription that start with "myvault".</span></span>

## <span data-ttu-id="f1c50-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1c50-125">PARAMETERS</span></span>

### <span data-ttu-id="f1c50-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1c50-126">-DefaultProfile</span></span>
<span data-ttu-id="f1c50-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f1c50-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1c50-128">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="f1c50-128">-InRemovedState</span></span>
<span data-ttu-id="f1c50-129">Çıktıda önceden silinmiş olan kasa gösterilip gösterilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1c50-129">Specifies whether to show the previously deleted vaults in the output.</span></span>

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

### <span data-ttu-id="f1c50-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="f1c50-130">-Location</span></span>
<span data-ttu-id="f1c50-131">Silinmiş kasanın konumu.</span><span class="sxs-lookup"><span data-stu-id="f1c50-131">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="f1c50-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1c50-132">-ResourceGroupName</span></span>
<span data-ttu-id="f1c50-133">Sorgulanan Anahtar Kasası veya anahtar kasası ile ilişkili kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1c50-133">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

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

### <span data-ttu-id="f1c50-134">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f1c50-134">-Tag</span></span>
<span data-ttu-id="f1c50-135">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="f1c50-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f1c50-136">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="f1c50-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1c50-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f1c50-137">-VaultName</span></span>
<span data-ttu-id="f1c50-138">Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1c50-138">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="f1c50-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1c50-139">CommonParameters</span></span>
<span data-ttu-id="f1c50-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1c50-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1c50-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f1c50-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1c50-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1c50-142">INPUTS</span></span>

### <span data-ttu-id="f1c50-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f1c50-143">System.String</span></span>

### <span data-ttu-id="f1c50-144">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f1c50-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f1c50-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1c50-145">OUTPUTS</span></span>

### <span data-ttu-id="f1c50-146">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="f1c50-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="f1c50-147">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultidentityıtem</span><span class="sxs-lookup"><span data-stu-id="f1c50-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="f1c50-148">Microsoft.Azure.Commands.KeyVault.Models.PSDEleditedtuş Kasası</span><span class="sxs-lookup"><span data-stu-id="f1c50-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="f1c50-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1c50-149">NOTES</span></span>

## <span data-ttu-id="f1c50-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1c50-150">RELATED LINKS</span></span>

[<span data-ttu-id="f1c50-151">Yeni-Aztuş Kasası</span><span class="sxs-lookup"><span data-stu-id="f1c50-151">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="f1c50-152">Remove-Aztuş Kasası</span><span class="sxs-lookup"><span data-stu-id="f1c50-152">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
