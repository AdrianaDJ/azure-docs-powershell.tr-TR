---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/update-azurermstorageaccountnetworkruleset
schema: 2.0.0
ms.openlocfilehash: beeaf374a261a30ad842aa9c0570ff544ec8ab68
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939210"
---
# <span data-ttu-id="9a759-101">Update-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9a759-101">Update-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="9a759-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a759-102">SYNOPSIS</span></span>
<span data-ttu-id="9a759-103">Depolama hesabının NetworkRule özelliğini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="9a759-103">Update the NetworkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a759-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9a759-104">SYNTAX</span></span>

```
Update-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a759-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9a759-105">DESCRIPTION</span></span>
<span data-ttu-id="9a759-106">**Update-AzureRmStorageAccountNetworkRuleSet** cmdlet 'i, bir depolama hesabının networkrule özelliğini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="9a759-106">The **Update-AzureRmStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="9a759-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9a759-107">EXAMPLES</span></span>

### <span data-ttu-id="9a759-108">Örnek 1: NetworkRule 'un tüm özelliklerini güncelleştir, JSON ile giriş kuralları</span><span class="sxs-lookup"><span data-stu-id="9a759-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="9a759-109">Bu komut, tüm NetworkRule özelliklerini, JSON ile giriş kurallarını güncelleştir.</span><span class="sxs-lookup"><span data-stu-id="9a759-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="9a759-110">Örnek 2: NetworkRule 'un güncelleştirme atlama özelliği</span><span class="sxs-lookup"><span data-stu-id="9a759-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="9a759-111">Bu komut, NetworkRule 'un bypass özelliğini güncelleyin (diğer özellikler değişmez).</span><span class="sxs-lookup"><span data-stu-id="9a759-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="9a759-112">Örnek 3: depolama hesabının NetworkRule kurallarını Temizleme</span><span class="sxs-lookup"><span data-stu-id="9a759-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="9a759-113">Bu komut depolama hesabının NetworkRule kurallarını temizler (diğer özellikler değişmez).</span><span class="sxs-lookup"><span data-stu-id="9a759-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="9a759-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9a759-114">PARAMETERS</span></span>

### <span data-ttu-id="9a759-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="9a759-115">-AsJob</span></span>
<span data-ttu-id="9a759-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9a759-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a759-117">-Bypass</span><span class="sxs-lookup"><span data-stu-id="9a759-117">-Bypass</span></span>
<span data-ttu-id="9a759-118">Depolama hesabının NetworkRule özelliğine güncelleştirilecek atlama değeri.</span><span class="sxs-lookup"><span data-stu-id="9a759-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="9a759-119">İzin verilen değer yok veya herhangi bir bileşimidir: • günlükleme • ölçüler • Azureservices</span><span class="sxs-lookup"><span data-stu-id="9a759-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

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

### <span data-ttu-id="9a759-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="9a759-120">-DefaultAction</span></span>
<span data-ttu-id="9a759-121">Depolama hesabının NetworkRule özelliğine güncelleştirilecek DefaultAction değeri.</span><span class="sxs-lookup"><span data-stu-id="9a759-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="9a759-122">İzin verilen seçenekler: • Izin ver • Reddet</span><span class="sxs-lookup"><span data-stu-id="9a759-122">The allowed Options: • Allow • Deny</span></span>

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

### <span data-ttu-id="9a759-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a759-123">-DefaultProfile</span></span>
<span data-ttu-id="9a759-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9a759-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a759-125">-Iprule</span><span class="sxs-lookup"><span data-stu-id="9a759-125">-IPRule</span></span>
<span data-ttu-id="9a759-126">Bir depolama hesabının NetworkRule özelliğine güncelleştirilecek ıprule nesneleri dizisi.</span><span class="sxs-lookup"><span data-stu-id="9a759-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="9a759-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="9a759-127">-Name</span></span>
<span data-ttu-id="9a759-128">Depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a759-128">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="9a759-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a759-129">-ResourceGroupName</span></span>
<span data-ttu-id="9a759-130">Depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a759-130">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="9a759-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9a759-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="9a759-132">Depolama hesabının NetworkRule özelliğine güncelleştirilecek VirtualNetworkRule nesnelerinin dizisi.</span><span class="sxs-lookup"><span data-stu-id="9a759-132">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="9a759-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="9a759-133">-Confirm</span></span>
<span data-ttu-id="9a759-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9a759-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a759-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a759-135">-WhatIf</span></span>
<span data-ttu-id="9a759-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9a759-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a759-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9a759-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a759-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a759-138">CommonParameters</span></span>
<span data-ttu-id="9a759-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9a759-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a759-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a759-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a759-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9a759-141">INPUTS</span></span>

### <span data-ttu-id="9a759-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9a759-142">System.String</span></span>

### <span data-ttu-id="9a759-143">Microsoft. Azure. Commands. Management. Storage. model. Psıprule []</span><span class="sxs-lookup"><span data-stu-id="9a759-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>
<span data-ttu-id="9a759-144">Parametreler: ıprule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9a759-144">Parameters: IPRule (ByValue)</span></span>

### <span data-ttu-id="9a759-145">Microsoft. Azure. Commands. Management. Storage. model. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="9a759-145">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>
<span data-ttu-id="9a759-146">Parametreler: VirtualNetworkRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9a759-146">Parameters: VirtualNetworkRule (ByValue)</span></span>

## <span data-ttu-id="9a759-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9a759-147">OUTPUTS</span></span>

### <span data-ttu-id="9a759-148">Microsoft. Azure. Commands. Management. Storage. model. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9a759-148">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="9a759-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9a759-149">NOTES</span></span>

## <span data-ttu-id="9a759-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9a759-150">RELATED LINKS</span></span>
