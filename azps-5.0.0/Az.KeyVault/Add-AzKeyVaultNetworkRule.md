---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
ms.openlocfilehash: c437611603bab6b2c4b9fff5cd0696e306182afa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319921"
---
# <span data-ttu-id="1aa28-101">Add-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1aa28-101">Add-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="1aa28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1aa28-102">SYNOPSIS</span></span>
<span data-ttu-id="1aa28-103">İstemcinin internet adresi temelinde bir anahtar kasasına erişimi kısıtlamak amacıyla bir kural ekler.</span><span class="sxs-lookup"><span data-stu-id="1aa28-103">Adds a rule meant to restrict access to a key vault based on the client's internet address.</span></span>

## <span data-ttu-id="1aa28-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1aa28-104">SYNTAX</span></span>

### <span data-ttu-id="1aa28-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1aa28-105">ByVaultName (Default)</span></span>
```
Add-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1aa28-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1aa28-106">ByInputObject</span></span>
```
Add-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1aa28-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="1aa28-107">ByResourceId</span></span>
```
Add-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1aa28-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1aa28-108">DESCRIPTION</span></span>
<span data-ttu-id="1aa28-109">**Add-Azanahtarvaultnetworkrule** cmdlet 'ı, IP adresleriyle veya ait oldukları sanal ağla belirlenen bir arayan kümesi için Anahtar Kasası erişimine izin verir veya erişimi kısıtlar.</span><span class="sxs-lookup"><span data-stu-id="1aa28-109">The **Add-AzKeyVaultNetworkRule** cmdlet grants or restricts access to a key vault to a set of caller designated by their IP addresses or the virtual network to which they belong.</span></span> <span data-ttu-id="1aa28-110">Kuralın erişim ilkesi aracılığıyla izin verilen diğer kullanıcılar, uygulamalar veya güvenlik grupları için erişimi kısıtlama olasılığı vardır.</span><span class="sxs-lookup"><span data-stu-id="1aa28-110">The rule has the potential to restrict access for other users, applications, or security groups which have been granted permissions via the access policy.</span></span>

<span data-ttu-id="1aa28-111">Lütfen içindeki tüm IP aralığının `10.0.0.0-10.255.255.255` (özel IP adresleri) ağ kuralları eklemek için kullanılamayacağını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="1aa28-111">Please note that any IP range inside `10.0.0.0-10.255.255.255` (private IP addresses) cannot be used to add network rules.</span></span>

## <span data-ttu-id="1aa28-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1aa28-112">EXAMPLES</span></span>

### <span data-ttu-id="1aa28-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1aa28-113">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Add-AzKeyVaultNetworkRule -VaultName myvault -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myvault
Resource Group Name              : myRG
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myRG/providers
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


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   : 10.0.1.0/24
                                   Virtual Network Rules                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-
                                   xxxxxxxxxxxxx/resourcegroups/myRG/providers/microsoft.network/virtualnetworks/myvn
                                   et/subnets/frontendsubnet

Tags                             :
```

<span data-ttu-id="1aa28-114">Bu komut, $myNetworkResId ile belirtilen sanal ağdan belirtilen IP adresine erişim izni vererek belirtilen kasaya bir ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="1aa28-114">This command adds a network rule to the specified vault, allowing access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="1aa28-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1aa28-115">PARAMETERS</span></span>

### <span data-ttu-id="1aa28-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aa28-116">-DefaultProfile</span></span>
<span data-ttu-id="1aa28-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1aa28-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1aa28-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1aa28-118">-InputObject</span></span>
<span data-ttu-id="1aa28-119">Tuş Kasası nesnesi</span><span class="sxs-lookup"><span data-stu-id="1aa28-119">KeyVault object</span></span>

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

### <span data-ttu-id="1aa28-120">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="1aa28-120">-IpAddressRange</span></span>
<span data-ttu-id="1aa28-121">Ağ kuralının ağ adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1aa28-121">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="1aa28-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1aa28-122">-PassThru</span></span>
<span data-ttu-id="1aa28-123">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="1aa28-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1aa28-124">Bu anahtar belirtilmişse, güncelleştirilmiş anahtar kasa nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="1aa28-124">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="1aa28-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aa28-125">-ResourceGroupName</span></span>
<span data-ttu-id="1aa28-126">Ağ kuralı değiştirildiği Anahtar Kasası ile ilişkili kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1aa28-126">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="1aa28-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1aa28-127">-ResourceId</span></span>
<span data-ttu-id="1aa28-128">Tuş Kasası kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="1aa28-128">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="1aa28-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1aa28-129">-VaultName</span></span>
<span data-ttu-id="1aa28-130">Ağ kuralı değiştirilecek bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1aa28-130">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="1aa28-131">-Virtualnetworkresourceıd</span><span class="sxs-lookup"><span data-stu-id="1aa28-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="1aa28-132">Ağ kuralının sanal ağ kaynağı tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1aa28-132">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="1aa28-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="1aa28-133">-Confirm</span></span>
<span data-ttu-id="1aa28-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1aa28-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1aa28-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1aa28-135">-WhatIf</span></span>
<span data-ttu-id="1aa28-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1aa28-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1aa28-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1aa28-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1aa28-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aa28-138">CommonParameters</span></span>
<span data-ttu-id="1aa28-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1aa28-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aa28-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1aa28-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aa28-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1aa28-141">INPUTS</span></span>

### <span data-ttu-id="1aa28-142">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="1aa28-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="1aa28-143">System. String</span><span class="sxs-lookup"><span data-stu-id="1aa28-143">System.String</span></span>

## <span data-ttu-id="1aa28-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1aa28-144">OUTPUTS</span></span>

### <span data-ttu-id="1aa28-145">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="1aa28-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="1aa28-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1aa28-146">NOTES</span></span>

## <span data-ttu-id="1aa28-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1aa28-147">RELATED LINKS</span></span>
