---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
ms.openlocfilehash: fd93a933b394fc8729186c7ea78c737123149bf2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916367"
---
# <span data-ttu-id="fb143-101">Add-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fb143-101">Add-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="fb143-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb143-102">SYNOPSIS</span></span>
<span data-ttu-id="fb143-103">İstemcinin internet adresi temelinde bir anahtar kasasına erişimi kısıtlamak amacıyla bir kural ekler.</span><span class="sxs-lookup"><span data-stu-id="fb143-103">Adds a rule meant to restrict access to a key vault based on the client's internet address.</span></span>

## <span data-ttu-id="fb143-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb143-104">SYNTAX</span></span>

### <span data-ttu-id="fb143-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fb143-105">ByVaultName (Default)</span></span>
```
Add-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb143-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fb143-106">ByInputObject</span></span>
```
Add-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb143-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="fb143-107">ByResourceId</span></span>
```
Add-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb143-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb143-108">DESCRIPTION</span></span>
<span data-ttu-id="fb143-109">**Add-Azanahtarvaultnetworkrule** cmdlet 'ı, IP adresleriyle veya ait oldukları sanal ağla belirlenen bir arayan kümesi için Anahtar Kasası erişimine izin verir veya erişimi kısıtlar.</span><span class="sxs-lookup"><span data-stu-id="fb143-109">The **Add-AzKeyVaultNetworkRule** cmdlet grants or restricts access to a key vault to a set of caller designated by their IP addresses or the virtual network to which they belong.</span></span> <span data-ttu-id="fb143-110">Kuralın erişim ilkesi aracılığıyla izin verilen diğer kullanıcılar, uygulamalar veya güvenlik grupları için erişimi kısıtlama olasılığı vardır.</span><span class="sxs-lookup"><span data-stu-id="fb143-110">The rule has the potential to restrict access for other users, applications, or security groups which have been granted permissions via the access policy.</span></span>

## <span data-ttu-id="fb143-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb143-111">EXAMPLES</span></span>

### <span data-ttu-id="fb143-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fb143-112">Example 1</span></span>
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

<span data-ttu-id="fb143-113">Bu komut, $myNetworkResId ile belirtilen sanal ağdan belirtilen IP adresine erişim izni vererek belirtilen kasaya bir ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="fb143-113">This command adds a network rule to the specified vault, allowing access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="fb143-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb143-114">PARAMETERS</span></span>

### <span data-ttu-id="fb143-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb143-115">-DefaultProfile</span></span>
<span data-ttu-id="fb143-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fb143-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb143-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb143-117">-InputObject</span></span>
<span data-ttu-id="fb143-118">Tuş Kasası nesnesi</span><span class="sxs-lookup"><span data-stu-id="fb143-118">KeyVault object</span></span>

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

### <span data-ttu-id="fb143-119">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="fb143-119">-IpAddressRange</span></span>
<span data-ttu-id="fb143-120">Ağ kuralının ağ adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb143-120">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="fb143-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fb143-121">-PassThru</span></span>
<span data-ttu-id="fb143-122">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="fb143-122">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="fb143-123">Bu anahtar belirtilmişse, güncelleştirilmiş anahtar kasa nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="fb143-123">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="fb143-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb143-124">-ResourceGroupName</span></span>
<span data-ttu-id="fb143-125">Ağ kuralı değiştirildiği Anahtar Kasası ile ilişkili kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb143-125">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="fb143-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fb143-126">-ResourceId</span></span>
<span data-ttu-id="fb143-127">Tuş Kasası kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="fb143-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="fb143-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fb143-128">-VaultName</span></span>
<span data-ttu-id="fb143-129">Ağ kuralı değiştirilecek bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb143-129">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="fb143-130">-Virtualnetworkresourceıd</span><span class="sxs-lookup"><span data-stu-id="fb143-130">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="fb143-131">Ağ kuralının sanal ağ kaynağı tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb143-131">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="fb143-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="fb143-132">-Confirm</span></span>
<span data-ttu-id="fb143-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fb143-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb143-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb143-134">-WhatIf</span></span>
<span data-ttu-id="fb143-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb143-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb143-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fb143-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb143-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb143-137">CommonParameters</span></span>
<span data-ttu-id="fb143-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb143-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb143-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb143-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb143-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb143-140">INPUTS</span></span>

### <span data-ttu-id="fb143-141">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="fb143-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="fb143-142">System. String</span><span class="sxs-lookup"><span data-stu-id="fb143-142">System.String</span></span>

## <span data-ttu-id="fb143-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb143-143">OUTPUTS</span></span>

### <span data-ttu-id="fb143-144">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="fb143-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="fb143-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb143-145">NOTES</span></span>

## <span data-ttu-id="fb143-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb143-146">RELATED LINKS</span></span>
