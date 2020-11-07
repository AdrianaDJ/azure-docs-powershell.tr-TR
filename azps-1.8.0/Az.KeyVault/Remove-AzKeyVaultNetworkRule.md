---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
ms.openlocfilehash: d7b5f3a7a5a4c2f28724214fb026768979fa9028
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916255"
---
# <span data-ttu-id="21aeb-101">Remove-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="21aeb-101">Remove-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="21aeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21aeb-102">SYNOPSIS</span></span>
<span data-ttu-id="21aeb-103">Bir anahtar kasasından ağ kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="21aeb-103">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="21aeb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="21aeb-104">SYNTAX</span></span>

### <span data-ttu-id="21aeb-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="21aeb-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21aeb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="21aeb-106">ByInputObject</span></span>
```
Remove-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21aeb-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="21aeb-107">ByResourceId</span></span>
```
Remove-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21aeb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="21aeb-108">DESCRIPTION</span></span>
<span data-ttu-id="21aeb-109">Bir anahtar kasasından ağ kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="21aeb-109">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="21aeb-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="21aeb-110">EXAMPLES</span></span>

### <span data-ttu-id="21aeb-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="21aeb-111">Example 1</span></span>
```powershell
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNetName -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Remove-AzKeyVaultNetworkRule -VaultName myVault -IpAddressRange "10.0.0.1/26" -VirtualNetworkResourceId $myNetworkResId -PassThru

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

<span data-ttu-id="21aeb-112">Bu komut belirtilen kasadan, belirtilen IP adresiyle sanal ağ kaynak tanımlayıcısıyla eşleşen bir kural bulunduğunda bir ağ kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="21aeb-112">This command removes a network rule from the specified vault, provided a rule is found matching the specified IP address and the virtual network resource identifier.</span></span>

## <span data-ttu-id="21aeb-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="21aeb-113">PARAMETERS</span></span>

### <span data-ttu-id="21aeb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21aeb-114">-DefaultProfile</span></span>
<span data-ttu-id="21aeb-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="21aeb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21aeb-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21aeb-116">-InputObject</span></span>
<span data-ttu-id="21aeb-117">Tuş Kasası nesnesi</span><span class="sxs-lookup"><span data-stu-id="21aeb-117">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21aeb-118">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="21aeb-118">-IpAddressRange</span></span>
<span data-ttu-id="21aeb-119">Ağ kuralının ağ adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="21aeb-119">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21aeb-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="21aeb-120">-PassThru</span></span>
<span data-ttu-id="21aeb-121">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="21aeb-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="21aeb-122">Bu anahtar belirtilmişse, güncelleştirilmiş anahtar kasa nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="21aeb-122">If this switch is specified, it returns the updated key vault object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21aeb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21aeb-123">-ResourceGroupName</span></span>
<span data-ttu-id="21aeb-124">Ağ kuralı değiştirildiği Anahtar Kasası ile ilişkili kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="21aeb-124">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21aeb-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="21aeb-125">-ResourceId</span></span>
<span data-ttu-id="21aeb-126">Tuş Kasası kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="21aeb-126">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21aeb-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="21aeb-127">-VaultName</span></span>
<span data-ttu-id="21aeb-128">Ağ kuralı değiştirilecek bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="21aeb-128">Specifies the name of a key vault whose network rule is being modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21aeb-129">-Virtualnetworkresourceıd</span><span class="sxs-lookup"><span data-stu-id="21aeb-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="21aeb-130">Ağ kuralının sanal ağ kaynağı tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="21aeb-130">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21aeb-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="21aeb-131">-Confirm</span></span>
<span data-ttu-id="21aeb-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="21aeb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21aeb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21aeb-133">-WhatIf</span></span>
<span data-ttu-id="21aeb-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="21aeb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21aeb-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="21aeb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21aeb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21aeb-136">CommonParameters</span></span>
<span data-ttu-id="21aeb-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="21aeb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21aeb-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21aeb-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21aeb-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="21aeb-139">INPUTS</span></span>

### <span data-ttu-id="21aeb-140">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="21aeb-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="21aeb-141">System. String</span><span class="sxs-lookup"><span data-stu-id="21aeb-141">System.String</span></span>

## <span data-ttu-id="21aeb-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="21aeb-142">OUTPUTS</span></span>

### <span data-ttu-id="21aeb-143">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="21aeb-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="21aeb-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="21aeb-144">NOTES</span></span>

## <span data-ttu-id="21aeb-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="21aeb-145">RELATED LINKS</span></span>