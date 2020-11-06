---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurermkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureRmKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureRmKeyVaultNetworkRule.md
ms.openlocfilehash: c99b621a39df1be595ceb873d85f5a3d848abc88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588111"
---
# <span data-ttu-id="c5b48-101">Add-AzureRmKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c5b48-101">Add-AzureRmKeyVaultNetworkRule</span></span>

## <span data-ttu-id="c5b48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5b48-102">SYNOPSIS</span></span>
<span data-ttu-id="c5b48-103">İstemcinin internet adresi temelinde bir anahtar kasasına erişimi kısıtlamak amacıyla bir kural ekler.</span><span class="sxs-lookup"><span data-stu-id="c5b48-103">Adds a rule meant to restrict access to a key vault based on the client's internet address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5b48-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c5b48-104">SYNTAX</span></span>

### <span data-ttu-id="c5b48-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c5b48-105">ByVaultName (Default)</span></span>
```
Add-AzureRmKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5b48-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c5b48-106">ByInputObject</span></span>
```
Add-AzureRmKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5b48-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="c5b48-107">ByResourceId</span></span>
```
Add-AzureRmKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5b48-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c5b48-108">DESCRIPTION</span></span>
<span data-ttu-id="c5b48-109">**Add-AzureRmKeyVaultNetworkRule** cmdlet 'ı, IP adresleriyle veya ait oldukları sanal ağla belirlenen bir arayan kümesi için Anahtar Kasası erişimine izin verir veya erişimi kısıtlar.</span><span class="sxs-lookup"><span data-stu-id="c5b48-109">The **Add-AzureRmKeyVaultNetworkRule** cmdlet grants or restricts access to a key vault to a set of caller designated by their IP addresses or the virtual network to which they belong.</span></span> <span data-ttu-id="c5b48-110">Kuralın erişim ilkesi aracılığıyla izin verilen diğer kullanıcılar, uygulamalar veya güvenlik grupları için erişimi kısıtlama olasılığı vardır.</span><span class="sxs-lookup"><span data-stu-id="c5b48-110">The rule has the potential to restrict access for other users, applications, or security groups which have been granted permissions via the access policy.</span></span>

## <span data-ttu-id="c5b48-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c5b48-111">EXAMPLES</span></span>

### <span data-ttu-id="c5b48-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c5b48-112">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzureRmVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzureRmVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Add-AzureRmKeyVaultNetworkRule -VaultName myvault -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

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

<span data-ttu-id="c5b48-113">Bu komut, $myNetworkResId ile belirtilen sanal ağdan belirtilen IP adresine erişim izni vererek belirtilen kasaya bir ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="c5b48-113">This command adds a network rule to the specified vault, allowing access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="c5b48-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c5b48-114">PARAMETERS</span></span>

### <span data-ttu-id="c5b48-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5b48-115">-DefaultProfile</span></span>
<span data-ttu-id="c5b48-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c5b48-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5b48-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5b48-117">-InputObject</span></span>
<span data-ttu-id="c5b48-118">Tuş Kasası nesnesi</span><span class="sxs-lookup"><span data-stu-id="c5b48-118">KeyVault object</span></span>

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

### <span data-ttu-id="c5b48-119">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="c5b48-119">-IpAddressRange</span></span>
<span data-ttu-id="c5b48-120">Ağ kuralının ağ adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5b48-120">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="c5b48-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c5b48-121">-PassThru</span></span>
<span data-ttu-id="c5b48-122">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="c5b48-122">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="c5b48-123">Bu anahtar belirtilmişse, güncelleştirilmiş anahtar kasa nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c5b48-123">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="c5b48-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5b48-124">-ResourceGroupName</span></span>
<span data-ttu-id="c5b48-125">Ağ kuralı değiştirildiği Anahtar Kasası ile ilişkili kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5b48-125">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="c5b48-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c5b48-126">-ResourceId</span></span>
<span data-ttu-id="c5b48-127">Tuş Kasası kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="c5b48-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="c5b48-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c5b48-128">-VaultName</span></span>
<span data-ttu-id="c5b48-129">Ağ kuralı değiştirilecek bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5b48-129">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="c5b48-130">-Virtualnetworkresourceıd</span><span class="sxs-lookup"><span data-stu-id="c5b48-130">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="c5b48-131">Ağ kuralının sanal ağ kaynağı tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5b48-131">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="c5b48-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="c5b48-132">-Confirm</span></span>
<span data-ttu-id="c5b48-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c5b48-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5b48-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5b48-134">-WhatIf</span></span>
<span data-ttu-id="c5b48-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c5b48-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5b48-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c5b48-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5b48-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5b48-137">CommonParameters</span></span>
<span data-ttu-id="c5b48-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c5b48-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5b48-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5b48-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5b48-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c5b48-140">INPUTS</span></span>

### <span data-ttu-id="c5b48-141">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="c5b48-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="c5b48-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c5b48-142">OUTPUTS</span></span>

### <span data-ttu-id="c5b48-143">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="c5b48-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="c5b48-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c5b48-144">NOTES</span></span>

## <span data-ttu-id="c5b48-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c5b48-145">RELATED LINKS</span></span>
