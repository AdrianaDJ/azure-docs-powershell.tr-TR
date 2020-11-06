---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/update-azurermstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 8851f7e2820e1c9a0a63b475544c49fe5c0c8ee7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592861"
---
# <span data-ttu-id="2efb5-101">Update-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2efb5-101">Update-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="2efb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2efb5-102">SYNOPSIS</span></span>
<span data-ttu-id="2efb5-103">Depolama hesabının NetworkRule özelliğini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="2efb5-103">Update the NetworkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2efb5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2efb5-104">SYNTAX</span></span>

```
Update-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2efb5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2efb5-105">DESCRIPTION</span></span>
<span data-ttu-id="2efb5-106">**Update-AzureRmStorageAccountNetworkRuleSet** cmdlet 'i, bir depolama hesabının networkrule özelliğini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="2efb5-106">The **Update-AzureRmStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="2efb5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2efb5-107">EXAMPLES</span></span>

### <span data-ttu-id="2efb5-108">Örnek 1: NetworkRule 'un tüm özelliklerini güncelleştir, JSON ile giriş kuralları</span><span class="sxs-lookup"><span data-stu-id="2efb5-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="2efb5-109">Bu komut, tüm NetworkRule özelliklerini, JSON ile giriş kurallarını güncelleştir.</span><span class="sxs-lookup"><span data-stu-id="2efb5-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="2efb5-110">Örnek 2: NetworkRule 'un güncelleştirme atlama özelliği</span><span class="sxs-lookup"><span data-stu-id="2efb5-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="2efb5-111">Bu komut, NetworkRule 'un bypass özelliğini güncelleyin (diğer özellikler değişmez).</span><span class="sxs-lookup"><span data-stu-id="2efb5-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="2efb5-112">Örnek 3: depolama hesabının NetworkRule kurallarını Temizleme</span><span class="sxs-lookup"><span data-stu-id="2efb5-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="2efb5-113">Bu komut depolama hesabının NetworkRule kurallarını temizler (diğer özellikler değişmez).</span><span class="sxs-lookup"><span data-stu-id="2efb5-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="2efb5-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2efb5-114">PARAMETERS</span></span>

### <span data-ttu-id="2efb5-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="2efb5-115">-AsJob</span></span>
<span data-ttu-id="2efb5-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2efb5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2efb5-117">-Bypass</span><span class="sxs-lookup"><span data-stu-id="2efb5-117">-Bypass</span></span>
<span data-ttu-id="2efb5-118">Depolama hesabının NetworkRule özelliğine güncelleştirilecek atlama değeri.</span><span class="sxs-lookup"><span data-stu-id="2efb5-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="2efb5-119">İzin verilen değer yok veya herhangi bir bileşimidir: • günlükleme • ölçüler • Azureservices</span><span class="sxs-lookup"><span data-stu-id="2efb5-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

```yaml
Type: PSNetWorkRuleBypassEnum
Parameter Sets: (All)
Aliases: 
Accepted values: None, Logging, Metrics, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2efb5-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="2efb5-120">-DefaultAction</span></span>
<span data-ttu-id="2efb5-121">Depolama hesabının NetworkRule özelliğine güncelleştirilecek DefaultAction değeri.</span><span class="sxs-lookup"><span data-stu-id="2efb5-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="2efb5-122">İzin verilen seçenekler: • Izin ver • Reddet</span><span class="sxs-lookup"><span data-stu-id="2efb5-122">The allowed Options: • Allow • Deny</span></span>

```yaml
Type: PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Deny, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2efb5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2efb5-123">-DefaultProfile</span></span>
<span data-ttu-id="2efb5-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2efb5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2efb5-125">-Iprule</span><span class="sxs-lookup"><span data-stu-id="2efb5-125">-IPRule</span></span>
<span data-ttu-id="2efb5-126">Bir depolama hesabının NetworkRule özelliğine güncelleştirilecek ıprule nesneleri dizisi.</span><span class="sxs-lookup"><span data-stu-id="2efb5-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: PSIpRule[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2efb5-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="2efb5-127">-Name</span></span>
<span data-ttu-id="2efb5-128">Depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2efb5-128">Specifies the name of the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2efb5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2efb5-129">-ResourceGroupName</span></span>
<span data-ttu-id="2efb5-130">Depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2efb5-130">Specifies the name of the resource group contains the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2efb5-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2efb5-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="2efb5-132">Depolama hesabının NetworkRule özelliğine güncelleştirilecek VirtualNetworkRule nesnelerinin dizisi.</span><span class="sxs-lookup"><span data-stu-id="2efb5-132">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2efb5-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="2efb5-133">-Confirm</span></span>
<span data-ttu-id="2efb5-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2efb5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2efb5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2efb5-135">-WhatIf</span></span>
<span data-ttu-id="2efb5-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2efb5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2efb5-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2efb5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2efb5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2efb5-138">CommonParameters</span></span>
<span data-ttu-id="2efb5-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2efb5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2efb5-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2efb5-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2efb5-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2efb5-141">INPUTS</span></span>

### <span data-ttu-id="2efb5-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2efb5-142">System.String</span></span>
<span data-ttu-id="2efb5-143">Microsoft. Azure. Commands. Management. Storage. modeller. PSIpRule [] Microsoft. Azure. Commands. Management. Storage. model. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="2efb5-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="2efb5-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2efb5-144">OUTPUTS</span></span>

### <span data-ttu-id="2efb5-145">Microsoft. Azure. Commands. Management. Storage. model. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2efb5-145">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="2efb5-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2efb5-146">NOTES</span></span>

## <span data-ttu-id="2efb5-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2efb5-147">RELATED LINKS</span></span>

