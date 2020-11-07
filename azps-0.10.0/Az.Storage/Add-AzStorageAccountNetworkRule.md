---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: fb8df6e3444a650cc5f3c249545a43b4033689bd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936292"
---
# <span data-ttu-id="f892f-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f892f-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="f892f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f892f-102">SYNOPSIS</span></span>
 <span data-ttu-id="f892f-103">Depolama hesabının NetworkRule özelliğine ıprules veya VirtualNetworkRules ekleme</span><span class="sxs-lookup"><span data-stu-id="f892f-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="f892f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f892f-104">SYNTAX</span></span>

### <span data-ttu-id="f892f-105">NetWorkRuleString (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f892f-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f892f-106">Ipruleobject</span><span class="sxs-lookup"><span data-stu-id="f892f-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f892f-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="f892f-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f892f-108">Iprulestring</span><span class="sxs-lookup"><span data-stu-id="f892f-108">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f892f-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="f892f-109">DESCRIPTION</span></span>
<span data-ttu-id="f892f-110">**Add-AzStorageAccountNetworkRule** cmdlet 'i, bir depolama hesabının networkrule özelliğine ıprules veya virtualnetworkrules ekler</span><span class="sxs-lookup"><span data-stu-id="f892f-110">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="f892f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f892f-111">EXAMPLES</span></span>

### <span data-ttu-id="f892f-112">Örnek 1: ıpaddressorrange ile birkaç IpRules ekleme</span><span class="sxs-lookup"><span data-stu-id="f892f-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="f892f-113">Bu komut, ıpaddressorrange ile birkaç ıprules ekler.</span><span class="sxs-lookup"><span data-stu-id="f892f-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="f892f-114">Örnek 2: Virtualnetworkresourceıd ile VirtualNetworkRule ekleme</span><span class="sxs-lookup"><span data-stu-id="f892f-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="f892f-115">Bu komut Virtualnetworkresourceıd ile VirtualNetworkRule öğesini ekler.</span><span class="sxs-lookup"><span data-stu-id="f892f-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="f892f-116">Örnek 3: başka bir hesaptan VirtualNetworkRule nesneleriyle VirtualNetworkRules ekleme</span><span class="sxs-lookup"><span data-stu-id="f892f-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="f892f-117">Bu komut, başka bir hesaptan VirtualNetworkRule nesneleriyle VirtualNetworkRules öğesini ekler.</span><span class="sxs-lookup"><span data-stu-id="f892f-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="f892f-118">Örnek 4: ıprule nesneleri olan birkaç ıprule ekleme, JSON ile giriş</span><span class="sxs-lookup"><span data-stu-id="f892f-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="f892f-119">Bu komut, ıprule nesneleri</span><span class="sxs-lookup"><span data-stu-id="f892f-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="f892f-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f892f-120">PARAMETERS</span></span>

### <span data-ttu-id="f892f-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="f892f-121">-AsJob</span></span>
<span data-ttu-id="f892f-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f892f-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f892f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f892f-123">-DefaultProfile</span></span>
<span data-ttu-id="f892f-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f892f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f892f-125">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="f892f-125">-IPAddressOrRange</span></span>
<span data-ttu-id="f892f-126">Ipaddressorrange dizisi, giriş ıpaddressorrange ve varsayılan eylem to NetworkRule özelliğine sahip olan ıprules ekleyin.</span><span class="sxs-lookup"><span data-stu-id="f892f-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="f892f-127">-Iprule</span><span class="sxs-lookup"><span data-stu-id="f892f-127">-IPRule</span></span>
<span data-ttu-id="f892f-128">Iprule nesnelerinin, NetworkRule özelliğine eklenecek dizisi.</span><span class="sxs-lookup"><span data-stu-id="f892f-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="f892f-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="f892f-129">-Name</span></span>
<span data-ttu-id="f892f-130">Depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f892f-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="f892f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f892f-131">-ResourceGroupName</span></span>
<span data-ttu-id="f892f-132">Depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f892f-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="f892f-133">-Virtualnetworkresourceıd</span><span class="sxs-lookup"><span data-stu-id="f892f-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="f892f-134">Virtualnetworkresourceıd dizisi, giriş Virtualnetworkresourceıd ile VirtualNetworkRule öğesini ve varsayılan eylemi NetworkRule özelliğine Izin verir.</span><span class="sxs-lookup"><span data-stu-id="f892f-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="f892f-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f892f-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="f892f-136">NetworkRule özelliğine eklenecek VirtualNetworkRule nesnelerinin dizisi.</span><span class="sxs-lookup"><span data-stu-id="f892f-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="f892f-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="f892f-137">-Confirm</span></span>
<span data-ttu-id="f892f-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f892f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f892f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f892f-139">-WhatIf</span></span>
<span data-ttu-id="f892f-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f892f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f892f-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f892f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f892f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f892f-142">CommonParameters</span></span>
<span data-ttu-id="f892f-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f892f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f892f-144">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f892f-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f892f-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f892f-145">INPUTS</span></span>

### <span data-ttu-id="f892f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f892f-146">System.String</span></span>

### <span data-ttu-id="f892f-147">Microsoft. Azure. Commands. Management. Storage. model. Psıprule []</span><span class="sxs-lookup"><span data-stu-id="f892f-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>
<span data-ttu-id="f892f-148">Parametreler: ıprule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f892f-148">Parameters: IPRule (ByValue)</span></span>

### <span data-ttu-id="f892f-149">Microsoft. Azure. Commands. Management. Storage. model. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="f892f-149">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>
<span data-ttu-id="f892f-150">Parametreler: VirtualNetworkRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f892f-150">Parameters: VirtualNetworkRule (ByValue)</span></span>

## <span data-ttu-id="f892f-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f892f-151">OUTPUTS</span></span>

### <span data-ttu-id="f892f-152">Microsoft. Azure. Commands. Management. Storage. model. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f892f-152">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="f892f-153">Microsoft. Azure. Commands. Management. Storage. model. Psıprule</span><span class="sxs-lookup"><span data-stu-id="f892f-153">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="f892f-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f892f-154">NOTES</span></span>

## <span data-ttu-id="f892f-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f892f-155">RELATED LINKS</span></span>
