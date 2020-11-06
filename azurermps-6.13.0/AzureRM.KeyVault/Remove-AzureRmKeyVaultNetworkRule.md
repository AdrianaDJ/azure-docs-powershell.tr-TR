---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurermkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultNetworkRule.md
ms.openlocfilehash: f1ff73a753c794ce7528c9af2b480f75d1460815
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590220"
---
# <span data-ttu-id="99526-101">Remove-AzureRmKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="99526-101">Remove-AzureRmKeyVaultNetworkRule</span></span>

## <span data-ttu-id="99526-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99526-102">SYNOPSIS</span></span>
<span data-ttu-id="99526-103">Bir anahtar kasasından ağ kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="99526-103">Removes a network rule from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99526-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99526-104">SYNTAX</span></span>

### <span data-ttu-id="99526-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="99526-105">ByVaultName (Default)</span></span>
```
Remove-AzureRmKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99526-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="99526-106">ByInputObject</span></span>
```
Remove-AzureRmKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99526-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="99526-107">ByResourceId</span></span>
```
Remove-AzureRmKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99526-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="99526-108">DESCRIPTION</span></span>
<span data-ttu-id="99526-109">Bir anahtar kasasından ağ kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="99526-109">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="99526-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99526-110">EXAMPLES</span></span>

### <span data-ttu-id="99526-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="99526-111">Example 1</span></span>
```powershell
PS C:\> $myNetworkResId = (Get-AzureRmVirtualNetwork -Name myVNetName -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Remove-AzureRmKeyVaultNetworkRule -VaultName myVault -IpAddressRange "10.0.0.1/26" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myVault
Resource Group Name              : myrg
Location                         : West US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/myvault
Vault URI                        : https://myvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
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
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   : 
                                   Virtual Network Rules                      :

Tags                             :
```

<span data-ttu-id="99526-112">Bu komut belirtilen kasadan, belirtilen IP adresiyle sanal ağ kaynak tanımlayıcısıyla eşleşen bir kural bulunduğunda bir ağ kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="99526-112">This command removes a network rule from the specified vault, provided a rule is found matching the specified IP address and the virtual network resource identifier.</span></span>

## <span data-ttu-id="99526-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99526-113">PARAMETERS</span></span>

### <span data-ttu-id="99526-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99526-114">-DefaultProfile</span></span>
<span data-ttu-id="99526-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="99526-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99526-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99526-116">-InputObject</span></span>
<span data-ttu-id="99526-117">Tuş Kasası nesnesi</span><span class="sxs-lookup"><span data-stu-id="99526-117">KeyVault object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99526-118">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="99526-118">-IpAddressRange</span></span>
<span data-ttu-id="99526-119">Ağ kuralının ağ adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99526-119">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99526-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="99526-120">-PassThru</span></span>
<span data-ttu-id="99526-121">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="99526-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="99526-122">Bu anahtar belirtilmişse, güncelleştirilmiş anahtar kasa nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="99526-122">If this switch is specified, it returns the updated key vault object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99526-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99526-123">-ResourceGroupName</span></span>
<span data-ttu-id="99526-124">Ağ kuralı değiştirildiği Anahtar Kasası ile ilişkili kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99526-124">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99526-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="99526-125">-ResourceId</span></span>
<span data-ttu-id="99526-126">Tuş Kasası kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="99526-126">KeyVault Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99526-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="99526-127">-VaultName</span></span>
<span data-ttu-id="99526-128">Ağ kuralı değiştirilecek bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99526-128">Specifies the name of a key vault whose network rule is being modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99526-129">-Virtualnetworkresourceıd</span><span class="sxs-lookup"><span data-stu-id="99526-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="99526-130">Ağ kuralının sanal ağ kaynağı tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99526-130">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99526-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="99526-131">-Confirm</span></span>
<span data-ttu-id="99526-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="99526-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99526-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99526-133">-WhatIf</span></span>
<span data-ttu-id="99526-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="99526-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99526-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="99526-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99526-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99526-136">CommonParameters</span></span>
<span data-ttu-id="99526-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="99526-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99526-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99526-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99526-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99526-139">INPUTS</span></span>

### <span data-ttu-id="99526-140">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="99526-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="99526-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99526-141">OUTPUTS</span></span>

### <span data-ttu-id="99526-142">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="99526-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="99526-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99526-143">NOTES</span></span>

## <span data-ttu-id="99526-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99526-144">RELATED LINKS</span></span>
