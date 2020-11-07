---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 09619247f41acb60180a7d3045afdcd689d5c183
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764201"
---
# <span data-ttu-id="d4f43-101">Update-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4f43-101">Update-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="d4f43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4f43-102">SYNOPSIS</span></span>
<span data-ttu-id="d4f43-103">Depolama hesabının NetworkRule özelliğini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="d4f43-103">Update the NetworkRule property of a Storage Account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4f43-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d4f43-104">SYNTAX</span></span>

```
Update-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4f43-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d4f43-105">DESCRIPTION</span></span>
<span data-ttu-id="d4f43-106">**Update-AzureRmStorageAccountNetworkRuleSet** cmdlet 'i, bir depolama hesabının networkrule özelliğini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="d4f43-106">The **Update-AzureRmStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage Account</span></span>

## <span data-ttu-id="d4f43-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d4f43-107">EXAMPLES</span></span>

### <span data-ttu-id="d4f43-108">Örnek 1: NetworkRule 'un tüm özelliklerini güncelleştir, JSON ile giriş kuralları</span><span class="sxs-lookup"><span data-stu-id="d4f43-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="d4f43-109">Bu komut, tüm NetworkRule özelliklerini, JSON ile giriş kurallarını güncelleştir.</span><span class="sxs-lookup"><span data-stu-id="d4f43-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="d4f43-110">Örnek 2: NetworkRule 'un güncelleştirme atlama özelliği</span><span class="sxs-lookup"><span data-stu-id="d4f43-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="d4f43-111">Bu komut, NetworkRule 'un bypass özelliğini güncelleyin (diğer özellikler değişmez).</span><span class="sxs-lookup"><span data-stu-id="d4f43-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="d4f43-112">Örnek 3: depolama hesabının NetworkRule kurallarını Temizleme</span><span class="sxs-lookup"><span data-stu-id="d4f43-112">Example 3: Clean up rules of NetworkRule of a Storage Account</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="d4f43-113">Bu komut depolama hesabının NetworkRule kurallarını temizler (diğer özellikler değişmez).</span><span class="sxs-lookup"><span data-stu-id="d4f43-113">This command clean up rules of NetworkRule of a Storage Account (other properties not change).</span></span>

## <span data-ttu-id="d4f43-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d4f43-114">PARAMETERS</span></span>

### <span data-ttu-id="d4f43-115">-Bypass</span><span class="sxs-lookup"><span data-stu-id="d4f43-115">-Bypass</span></span>
<span data-ttu-id="d4f43-116">Depolama hesabının NetworkRule özelliğine güncelleştirilecek atlama değeri.</span><span class="sxs-lookup"><span data-stu-id="d4f43-116">The Bypass value to update to the NetworkRule property of a Storage Account.</span></span>
<span data-ttu-id="d4f43-117">İzin verilen değer none veya herhangi bir birleşimi: ¢ Logging</span><span class="sxs-lookup"><span data-stu-id="d4f43-117">The allowed value are none or any combination of: â€¢ Logging â€¢ Metrics â€¢ Azureservices</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleBypassEnum
Parameter Sets: (All)
Aliases: 
Accepted values: None, Logging, Metrics, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4f43-118">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="d4f43-118">-DefaultAction</span></span>
<span data-ttu-id="d4f43-119">Depolama hesabının NetworkRule özelliğine güncelleştirilecek DefaultAction değeri.</span><span class="sxs-lookup"><span data-stu-id="d4f43-119">The DefaultAction value to update to the NetworkRule property of a Storage Account.</span></span>
<span data-ttu-id="d4f43-120">İzin verilen seçenekler: â € ¢</span><span class="sxs-lookup"><span data-stu-id="d4f43-120">The allowed Options: â€¢ Allow â€¢ Deny</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Deny, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4f43-121">-Iprule</span><span class="sxs-lookup"><span data-stu-id="d4f43-121">-IPRule</span></span>
<span data-ttu-id="d4f43-122">Bir depolama hesabının NetworkRule özelliğine güncelleştirilecek ıprule nesneleri dizisi.</span><span class="sxs-lookup"><span data-stu-id="d4f43-122">The Array of IpRule objects to update to the NetworkRule Property of a Storage Account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f43-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="d4f43-123">-Name</span></span>
<span data-ttu-id="d4f43-124">Depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4f43-124">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="d4f43-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4f43-125">-ResourceGroupName</span></span>
<span data-ttu-id="d4f43-126">Depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4f43-126">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="d4f43-127">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d4f43-127">-VirtualNetworkRule</span></span>
<span data-ttu-id="d4f43-128">Depolama hesabının NetworkRule özelliğine güncelleştirilecek VirtualNetworkRule nesnelerinin dizisi.</span><span class="sxs-lookup"><span data-stu-id="d4f43-128">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage Account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f43-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="d4f43-129">-Confirm</span></span>
<span data-ttu-id="d4f43-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d4f43-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4f43-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4f43-131">-WhatIf</span></span>
<span data-ttu-id="d4f43-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d4f43-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4f43-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d4f43-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4f43-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4f43-134">-DefaultProfile</span></span>
<span data-ttu-id="d4f43-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d4f43-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4f43-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4f43-136">CommonParameters</span></span>
<span data-ttu-id="d4f43-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d4f43-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4f43-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4f43-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4f43-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d4f43-139">INPUTS</span></span>

### <span data-ttu-id="d4f43-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d4f43-140">System.String</span></span>
<span data-ttu-id="d4f43-141">Microsoft. Azure. Commands. Management. Storage. modeller. PSIpRule [] Microsoft. Azure. Commands. Management. Storage. model. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="d4f43-141">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="d4f43-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d4f43-142">OUTPUTS</span></span>

### <span data-ttu-id="d4f43-143">Microsoft. Azure. Commands. Management. Storage. model. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4f43-143">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="d4f43-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d4f43-144">NOTES</span></span>

## <span data-ttu-id="d4f43-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d4f43-145">RELATED LINKS</span></span>

