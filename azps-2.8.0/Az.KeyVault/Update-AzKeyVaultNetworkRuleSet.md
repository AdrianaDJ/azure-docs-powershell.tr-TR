---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
ms.openlocfilehash: f20099fbd9dd2aa7a9fd6774892d29fbde7ce34b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751599"
---
# <span data-ttu-id="2447f-101">Update-AzKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2447f-101">Update-AzKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="2447f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2447f-102">SYNOPSIS</span></span>
<span data-ttu-id="2447f-103">Bir anahtar kasasındaki ağ kuralı 'nı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2447f-103">Updates the network rule set on a key vault.</span></span>

## <span data-ttu-id="2447f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2447f-104">SYNTAX</span></span>

### <span data-ttu-id="2447f-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2447f-105">ByVaultName (Default)</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2447f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2447f-106">ByInputObject</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-InputObject] <PSKeyVault>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2447f-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="2447f-107">ByResourceId</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-ResourceId] <String>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2447f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2447f-108">DESCRIPTION</span></span>
<span data-ttu-id="2447f-109">**Update-Azanahtarvaultnetworkruleset** komutu, belirtilen anahtar kasası 'ndaki ağ kurallarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2447f-109">The **Update-AzKeyVaultNetworkRuleSet** command updates the network rules in effect on the specified key vault.</span></span> 

## <span data-ttu-id="2447f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2447f-110">EXAMPLES</span></span>

### <span data-ttu-id="2447f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2447f-111">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Update-AzKeyVaultNetworkRuleSet -VaultName 'myVault' -ResourceGroupName myRG -Bypass AzureServices -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myVault
Resource Group Name              : myRG
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
                                   IP Rules                                   : 10.0.1.0/24
                                   Virtual Network Rules                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-
                                   xxxxxxxxxxxxx/resourcegroups/myrg/providers/microsoft.network/virtualnetworks/myvn
                                   et/subnets/frontendsubnet

Tags                             :
```

<span data-ttu-id="2447f-112">Bu komut, belirtilen IP aralığı ve sanal ağ için ' Mykasa ' adlı kasada ağ RuleSet 'i güncelleştirir ve Azure hizmetleri için ağ kuralının atlanmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="2447f-112">This command updates the network ruleset on the vault named 'myVault' for the specified IP range and the virtual network, allowing bypassing of the network rule for Azure services.</span></span>

## <span data-ttu-id="2447f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2447f-113">PARAMETERS</span></span>

### <span data-ttu-id="2447f-114">-Bypass</span><span class="sxs-lookup"><span data-stu-id="2447f-114">-Bypass</span></span>
<span data-ttu-id="2447f-115">Ağ kuralının atlanmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2447f-115">Specifies bypass of network rule.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum]
Parameter Sets: (All)
Aliases:
Accepted values: None, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2447f-116">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="2447f-116">-DefaultAction</span></span>
<span data-ttu-id="2447f-117">Ağ kuralının varsayılan eylemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2447f-117">Specifies default action of network rule.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum]
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2447f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2447f-118">-DefaultProfile</span></span>
<span data-ttu-id="2447f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2447f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2447f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2447f-120">-InputObject</span></span>
<span data-ttu-id="2447f-121">Tuş Kasası nesnesi</span><span class="sxs-lookup"><span data-stu-id="2447f-121">KeyVault object</span></span>

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

### <span data-ttu-id="2447f-122">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="2447f-122">-IpAddressRange</span></span>
<span data-ttu-id="2447f-123">Ağ kuralının ağ adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2447f-123">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="2447f-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2447f-124">-PassThru</span></span>
<span data-ttu-id="2447f-125">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="2447f-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="2447f-126">Bu anahtar belirtilmişse, güncelleştirilmiş anahtar kasa nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2447f-126">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="2447f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2447f-127">-ResourceGroupName</span></span>
<span data-ttu-id="2447f-128">Ağ kuralı değiştirildiği Anahtar Kasası ile ilişkili kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2447f-128">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="2447f-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2447f-129">-ResourceId</span></span>
<span data-ttu-id="2447f-130">Tuş Kasası kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="2447f-130">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="2447f-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2447f-131">-VaultName</span></span>
<span data-ttu-id="2447f-132">Ağ kuralı değiştirilecek bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2447f-132">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="2447f-133">-Virtualnetworkresourceıd</span><span class="sxs-lookup"><span data-stu-id="2447f-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="2447f-134">Ağ kuralının sanal ağ kaynağı tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2447f-134">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="2447f-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="2447f-135">-Confirm</span></span>
<span data-ttu-id="2447f-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2447f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2447f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2447f-137">-WhatIf</span></span>
<span data-ttu-id="2447f-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2447f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2447f-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2447f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2447f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2447f-140">CommonParameters</span></span>
<span data-ttu-id="2447f-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2447f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2447f-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2447f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2447f-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2447f-143">INPUTS</span></span>

### <span data-ttu-id="2447f-144">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="2447f-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="2447f-145">System. String</span><span class="sxs-lookup"><span data-stu-id="2447f-145">System.String</span></span>

### <span data-ttu-id="2447f-146">System. Nullable ' 1 [[Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultNetworkRuleDefaultActionEnum, Microsoft. Azure. PowerShell. cmdlet. Keykasası, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2447f-146">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="2447f-147">System. Nullable ' 1 [[Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultNetworkRuleBypassEnum, Microsoft. Azure. PowerShell. cmdlet. Keykasası, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2447f-147">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2447f-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2447f-148">OUTPUTS</span></span>

### <span data-ttu-id="2447f-149">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="2447f-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="2447f-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2447f-150">NOTES</span></span>

## <span data-ttu-id="2447f-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2447f-151">RELATED LINKS</span></span>
