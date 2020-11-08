---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 1eeaf3a7c9d0c4b5715bc5b75e42e53a8fa98c5e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279323"
---
# <span data-ttu-id="4b8b9-101">Remove-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4b8b9-101">Remove-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="4b8b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b8b9-102">SYNOPSIS</span></span>
<span data-ttu-id="4b8b9-103">Depolama hesabının NetWorkRule özelliğinden ıprules veya VirtualNetworkRules öğesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="4b8b9-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="4b8b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b8b9-104">SYNTAX</span></span>

### <span data-ttu-id="4b8b9-105">NetWorkRuleString (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4b8b9-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4b8b9-106">Ipruleobject</span><span class="sxs-lookup"><span data-stu-id="4b8b9-106">IpRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b8b9-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="4b8b9-107">NetworkRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b8b9-108">Iprulestring</span><span class="sxs-lookup"><span data-stu-id="4b8b9-108">IpRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b8b9-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b8b9-109">DESCRIPTION</span></span>
<span data-ttu-id="4b8b9-110">**Remove-AzStorageAccountNetworkRule** cmdlet 'i, bir depolama hesabının networkrule özelliğinden ıprules veya virtualnetworkrules öğesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="4b8b9-110">The **Remove-AzStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="4b8b9-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b8b9-111">EXAMPLES</span></span>

### <span data-ttu-id="4b8b9-112">Örnek 1: ıpaddressorrange ile birkaç Ipkuralı kaldırın</span><span class="sxs-lookup"><span data-stu-id="4b8b9-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="4b8b9-113">Bu komut, ıpaddressorrange ile birkaç Ipkuralı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4b8b9-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="4b8b9-114">Örnek 2: JSON ile VirtualNetworkRule nesne girişiyle VirtualNetworkRule öğesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="4b8b9-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="4b8b9-115">Bu komut, JSON ile VirtualNetworkRule nesne girişiyle VirtualNetworkRule öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4b8b9-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="4b8b9-116">Örnek 3: birinci ıprule 'i ardışık düzene çıkarma</span><span class="sxs-lookup"><span data-stu-id="4b8b9-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="4b8b9-117">Bu komut ilk ıprule 'i ardışık düzene çıkarın.</span><span class="sxs-lookup"><span data-stu-id="4b8b9-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="4b8b9-118">Örnek 4: Virtualnetworkresourceıd ile birkaç VirtualNetworkRules 'ı kaldırma</span><span class="sxs-lookup"><span data-stu-id="4b8b9-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="4b8b9-119">Bu komut Virtualnetworkresourceıd ile birkaç VirtualNetworkRules 'ı kaldırın.</span><span class="sxs-lookup"><span data-stu-id="4b8b9-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

## <span data-ttu-id="4b8b9-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b8b9-120">PARAMETERS</span></span>

### <span data-ttu-id="4b8b9-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="4b8b9-121">-AsJob</span></span>
<span data-ttu-id="4b8b9-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4b8b9-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b8b9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b8b9-123">-DefaultProfile</span></span>
<span data-ttu-id="4b8b9-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4b8b9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b8b9-125">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="4b8b9-125">-IPAddressOrRange</span></span>
<span data-ttu-id="4b8b9-126">Ipaddressorrange dizisi, ıprule 'i NetWorkRule özelliğinden aynı ıpaddressorrange ile kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4b8b9-126">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IpRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b8b9-127">-Iprule</span><span class="sxs-lookup"><span data-stu-id="4b8b9-127">-IPRule</span></span>
<span data-ttu-id="4b8b9-128">NetWorkRule özelliğinden kaldırılacak ıprule nesneleri dizisi.</span><span class="sxs-lookup"><span data-stu-id="4b8b9-128">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]
Parameter Sets: IpRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b8b9-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="4b8b9-129">-Name</span></span>
<span data-ttu-id="4b8b9-130">Depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b8b9-130">Specifies the name of the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b8b9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b8b9-131">-ResourceGroupName</span></span>
<span data-ttu-id="4b8b9-132">Depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b8b9-132">Specifies the name of the resource group contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b8b9-133">-Virtualnetworkresourceıd</span><span class="sxs-lookup"><span data-stu-id="4b8b9-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="4b8b9-134">Virtualnetworkresourceıd dizisi, NetWorkRule özelliğinden aynı Virtualnetworkresourceıd ile VirtualNetworkRule öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4b8b9-134">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: NetWorkRuleString
Aliases: SubnetId, VirtualNetworkId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b8b9-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4b8b9-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="4b8b9-136">NetWorkRule özelliğinden kaldırılacak VirtualNetworkRule nesnelerinin dizisi.</span><span class="sxs-lookup"><span data-stu-id="4b8b9-136">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b8b9-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="4b8b9-137">-Confirm</span></span>
<span data-ttu-id="4b8b9-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4b8b9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b8b9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b8b9-139">-WhatIf</span></span>
<span data-ttu-id="4b8b9-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b8b9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b8b9-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4b8b9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b8b9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b8b9-142">CommonParameters</span></span>
<span data-ttu-id="4b8b9-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b8b9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b8b9-144">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b8b9-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b8b9-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b8b9-145">INPUTS</span></span>

### <span data-ttu-id="4b8b9-146">System. String</span><span class="sxs-lookup"><span data-stu-id="4b8b9-146">System.String</span></span>

### <span data-ttu-id="4b8b9-147">Microsoft. Azure. Commands. Management. Storage. model. Psıprule []</span><span class="sxs-lookup"><span data-stu-id="4b8b9-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="4b8b9-148">Microsoft. Azure. Commands. Management. Storage. model. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="4b8b9-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="4b8b9-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b8b9-149">OUTPUTS</span></span>

### <span data-ttu-id="4b8b9-150">Microsoft. Azure. Commands. Management. Storage. model. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4b8b9-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="4b8b9-151">Microsoft. Azure. Commands. Management. Storage. model. Psıprule</span><span class="sxs-lookup"><span data-stu-id="4b8b9-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="4b8b9-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b8b9-152">NOTES</span></span>

## <span data-ttu-id="4b8b9-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b8b9-153">RELATED LINKS</span></span>
