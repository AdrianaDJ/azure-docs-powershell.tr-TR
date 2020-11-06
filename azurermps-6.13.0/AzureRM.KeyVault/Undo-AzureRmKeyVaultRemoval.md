---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurermkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
ms.openlocfilehash: af6ed0e4db688cdc9ad6da598c0bc240e9b3c958
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590216"
---
# <span data-ttu-id="2e873-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="2e873-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="2e873-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e873-102">SYNOPSIS</span></span>
<span data-ttu-id="2e873-103">Silinmiş Anahtar Kasası 'nı etkin bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="2e873-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e873-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e873-104">SYNTAX</span></span>

### <span data-ttu-id="2e873-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2e873-105">Default (Default)</span></span>
```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e873-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2e873-106">InputObject</span></span>
```
Undo-AzureRmKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e873-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e873-107">DESCRIPTION</span></span>
<span data-ttu-id="2e873-108">**Undo-Azurermkeyvaultkaldırmada** cmdlet 'i önceden silinmiş bir Anahtar Kasası kurtarır.</span><span class="sxs-lookup"><span data-stu-id="2e873-108">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="2e873-109">Kurtarılan kasa kurtarma sonrasında etkin olur</span><span class="sxs-lookup"><span data-stu-id="2e873-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="2e873-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e873-110">EXAMPLES</span></span>

### <span data-ttu-id="2e873-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2e873-111">Example 1</span></span>
```powershell
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}

Vault Name                       : MyKeyVault
Resource Group Name              : MyResourceGroup
Location                         : eastus2
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers
                                   /Microsoft.KeyVault/vaults/mykeyvault
Vault URI                        : https://mykeyvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : True
Enabled For Disk Encryption?     : True
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
                                   Name  Value
                                   ====  =====
                                   x     y
```

<span data-ttu-id="2e873-112">Bu komut, daha önce eastus2 bölgesinden ve ' MyResourceGroup ' kaynak grubundan silinen Anahtar Kasası 'nı etkin ve kullanılabilir bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="2e873-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="2e873-113">Ayrıca etiketleri yeni etiketle değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2e873-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="2e873-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e873-114">PARAMETERS</span></span>

### <span data-ttu-id="2e873-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e873-115">-DefaultProfile</span></span>
<span data-ttu-id="2e873-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2e873-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e873-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e873-117">-InputObject</span></span>
<span data-ttu-id="2e873-118">Silinmiş kasa nesnesi</span><span class="sxs-lookup"><span data-stu-id="2e873-118">Deleted vault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e873-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="2e873-119">-Location</span></span>
<span data-ttu-id="2e873-120">Silinmiş kasa özgün Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e873-120">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e873-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e873-121">-ResourceGroupName</span></span>
<span data-ttu-id="2e873-122">Anahtar Kasası oluşturulacak varolan bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e873-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e873-123">Etiketli</span><span class="sxs-lookup"><span data-stu-id="2e873-123">-Tag</span></span>
<span data-ttu-id="2e873-124">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="2e873-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2e873-125">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="2e873-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e873-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2e873-126">-VaultName</span></span>
<span data-ttu-id="2e873-127">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="2e873-127">Vault name.</span></span>
<span data-ttu-id="2e873-128">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2e873-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e873-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="2e873-129">-Confirm</span></span>
<span data-ttu-id="2e873-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2e873-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e873-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e873-131">-WhatIf</span></span>
<span data-ttu-id="2e873-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2e873-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e873-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2e873-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e873-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e873-134">CommonParameters</span></span>
<span data-ttu-id="2e873-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e873-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e873-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e873-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e873-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e873-137">INPUTS</span></span>

### <span data-ttu-id="2e873-138">Microsoft.Azure.Commands.KeyVault.Models.PSDEleditedtuş Kasası</span><span class="sxs-lookup"><span data-stu-id="2e873-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>
<span data-ttu-id="2e873-139">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2e873-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="2e873-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e873-140">OUTPUTS</span></span>

### <span data-ttu-id="2e873-141">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="2e873-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="2e873-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e873-142">NOTES</span></span>

## <span data-ttu-id="2e873-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e873-143">RELATED LINKS</span></span>

[<span data-ttu-id="2e873-144">Remove-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="2e873-144">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="2e873-145">Yeni-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="2e873-145">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="2e873-146">Get-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="2e873-146">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)
