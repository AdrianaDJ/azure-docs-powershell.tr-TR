---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstorageaccountnetworkrule
schema: 2.0.0
ms.openlocfilehash: 6fd79e458c4ac288c6bc8f26add140e8f0a695ca
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938908"
---
# <span data-ttu-id="57ff8-101">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="57ff8-101">Remove-AzureRmStorageAccountNetworkRule</span></span>

## <span data-ttu-id="57ff8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="57ff8-103">Depolama hesabının NetWorkRule özelliğinden ıprules veya VirtualNetworkRules öğesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="57ff8-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57ff8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57ff8-104">SYNTAX</span></span>

### <span data-ttu-id="57ff8-105">NetWorkRuleString (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="57ff8-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57ff8-106">Ipruleobject</span><span class="sxs-lookup"><span data-stu-id="57ff8-106">IpRuleObject</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57ff8-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="57ff8-107">NetworkRuleObject</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57ff8-108">Iprulestring</span><span class="sxs-lookup"><span data-stu-id="57ff8-108">IpRuleString</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57ff8-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="57ff8-109">DESCRIPTION</span></span>
<span data-ttu-id="57ff8-110">**Remove-AzureRmStorageAccountNetworkRule** cmdlet 'i, bir depolama hesabının networkrule özelliğinden ıprules veya virtualnetworkrules öğesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="57ff8-110">The **Remove-AzureRmStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="57ff8-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57ff8-111">EXAMPLES</span></span>

### <span data-ttu-id="57ff8-112">Örnek 1: ıpaddressorrange ile birkaç Ipkuralı kaldırın</span><span class="sxs-lookup"><span data-stu-id="57ff8-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="57ff8-113">Bu komut, ıpaddressorrange ile birkaç Ipkuralı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="57ff8-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="57ff8-114">Örnek 2: JSON ile VirtualNetworkRule nesne girişiyle VirtualNetworkRule öğesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="57ff8-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="57ff8-115">Bu komut, JSON ile VirtualNetworkRule nesne girişiyle VirtualNetworkRule öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="57ff8-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="57ff8-116">Örnek 3: birinci ıprule 'i ardışık düzene çıkarma</span><span class="sxs-lookup"><span data-stu-id="57ff8-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="57ff8-117">Bu komut ilk ıprule 'i ardışık düzene çıkarın.</span><span class="sxs-lookup"><span data-stu-id="57ff8-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="57ff8-118">Örnek 4: Virtualnetworkresourceıd ile birkaç VirtualNetworkRules 'ı kaldırma</span><span class="sxs-lookup"><span data-stu-id="57ff8-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="57ff8-119">Bu komut Virtualnetworkresourceıd ile birkaç VirtualNetworkRules 'ı kaldırın.</span><span class="sxs-lookup"><span data-stu-id="57ff8-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

## <span data-ttu-id="57ff8-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57ff8-120">PARAMETERS</span></span>

### <span data-ttu-id="57ff8-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="57ff8-121">-AsJob</span></span>
<span data-ttu-id="57ff8-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="57ff8-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57ff8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57ff8-123">-DefaultProfile</span></span>
<span data-ttu-id="57ff8-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="57ff8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57ff8-125">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="57ff8-125">-IPAddressOrRange</span></span>
<span data-ttu-id="57ff8-126">Ipaddressorrange dizisi, ıprule 'i NetWorkRule özelliğinden aynı ıpaddressorrange ile kaldırır.</span><span class="sxs-lookup"><span data-stu-id="57ff8-126">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="57ff8-127">-Iprule</span><span class="sxs-lookup"><span data-stu-id="57ff8-127">-IPRule</span></span>
<span data-ttu-id="57ff8-128">NetWorkRule özelliğinden kaldırılacak ıprule nesneleri dizisi.</span><span class="sxs-lookup"><span data-stu-id="57ff8-128">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="57ff8-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="57ff8-129">-Name</span></span>
<span data-ttu-id="57ff8-130">Depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57ff8-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="57ff8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57ff8-131">-ResourceGroupName</span></span>
<span data-ttu-id="57ff8-132">Depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57ff8-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="57ff8-133">-Virtualnetworkresourceıd</span><span class="sxs-lookup"><span data-stu-id="57ff8-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="57ff8-134">Virtualnetworkresourceıd dizisi, NetWorkRule özelliğinden aynı Virtualnetworkresourceıd ile VirtualNetworkRule öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="57ff8-134">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="57ff8-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="57ff8-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="57ff8-136">NetWorkRule özelliğinden kaldırılacak VirtualNetworkRule nesnelerinin dizisi.</span><span class="sxs-lookup"><span data-stu-id="57ff8-136">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="57ff8-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="57ff8-137">-Confirm</span></span>
<span data-ttu-id="57ff8-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="57ff8-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57ff8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57ff8-139">-WhatIf</span></span>
<span data-ttu-id="57ff8-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="57ff8-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57ff8-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="57ff8-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57ff8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57ff8-142">CommonParameters</span></span>
<span data-ttu-id="57ff8-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57ff8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57ff8-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57ff8-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57ff8-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57ff8-145">INPUTS</span></span>

### <span data-ttu-id="57ff8-146">System. String</span><span class="sxs-lookup"><span data-stu-id="57ff8-146">System.String</span></span>

### <span data-ttu-id="57ff8-147">Microsoft. Azure. Commands. Management. Storage. model. Psıprule []</span><span class="sxs-lookup"><span data-stu-id="57ff8-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>
<span data-ttu-id="57ff8-148">Parametreler: ıprule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="57ff8-148">Parameters: IPRule (ByValue)</span></span>

### <span data-ttu-id="57ff8-149">Microsoft. Azure. Commands. Management. Storage. model. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="57ff8-149">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>
<span data-ttu-id="57ff8-150">Parametreler: VirtualNetworkRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="57ff8-150">Parameters: VirtualNetworkRule (ByValue)</span></span>

## <span data-ttu-id="57ff8-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57ff8-151">OUTPUTS</span></span>

### <span data-ttu-id="57ff8-152">Microsoft. Azure. Commands. Management. Storage. model. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="57ff8-152">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="57ff8-153">Microsoft. Azure. Commands. Management. Storage. model. Psıprule</span><span class="sxs-lookup"><span data-stu-id="57ff8-153">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="57ff8-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57ff8-154">NOTES</span></span>

## <span data-ttu-id="57ff8-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57ff8-155">RELATED LINKS</span></span>
