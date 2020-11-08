---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 75b729437599f66be567229a1899028e628079fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098698"
---
# <span data-ttu-id="1e297-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="1e297-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="1e297-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e297-102">SYNOPSIS</span></span>
<span data-ttu-id="1e297-103">Azure sanal WAN oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1e297-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="1e297-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e297-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-VirtualWANType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e297-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e297-105">DESCRIPTION</span></span>
<span data-ttu-id="1e297-106">Yeni bir Azure VirtualWAN kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1e297-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="1e297-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e297-107">EXAMPLES</span></span>

### <span data-ttu-id="1e297-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1e297-108">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="1e297-109">Yukarıdaki "Batı ABD" adresindeki "testRG" adlı bir kaynak grubu ve Azure 'daki bu kaynak grubunda şubeye dallanan bir Azure sanal WAN 'si oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1e297-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="1e297-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e297-110">PARAMETERS</span></span>

### <span data-ttu-id="1e297-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="1e297-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="1e297-112">VirtualWan için dal trafiğine izin verin.</span><span class="sxs-lookup"><span data-stu-id="1e297-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="1e297-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="1e297-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="1e297-114">VirtualWan için VNET 'den VNET trafiğine izin verin.</span><span class="sxs-lookup"><span data-stu-id="1e297-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="1e297-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="1e297-115">-AsJob</span></span>
<span data-ttu-id="1e297-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1e297-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e297-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e297-117">-DefaultProfile</span></span>
<span data-ttu-id="1e297-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1e297-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e297-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="1e297-119">-Location</span></span>
<span data-ttu-id="1e297-120">VirtualWAN kaynağının konumu.</span><span class="sxs-lookup"><span data-stu-id="1e297-120">The location of the VirtualWAN resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e297-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="1e297-121">-Name</span></span>
<span data-ttu-id="1e297-122">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="1e297-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e297-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e297-123">-ResourceGroupName</span></span>
<span data-ttu-id="1e297-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1e297-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e297-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="1e297-125">-Tag</span></span>
<span data-ttu-id="1e297-126">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="1e297-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e297-127">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="1e297-127">-VirtualWANType</span></span>
<span data-ttu-id="1e297-128">Sanal WAN 'ın türü.</span><span class="sxs-lookup"><span data-stu-id="1e297-128">The type of the Virtual Wan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e297-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="1e297-129">-Confirm</span></span>
<span data-ttu-id="1e297-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1e297-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e297-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e297-131">-WhatIf</span></span>
<span data-ttu-id="1e297-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1e297-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e297-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1e297-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e297-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e297-134">CommonParameters</span></span>
<span data-ttu-id="1e297-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e297-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e297-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1e297-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e297-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e297-137">INPUTS</span></span>

### <span data-ttu-id="1e297-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1e297-138">None</span></span>

## <span data-ttu-id="1e297-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e297-139">OUTPUTS</span></span>

### <span data-ttu-id="1e297-140">Microsoft. Azure. Commands. Network. model. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="1e297-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="1e297-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e297-141">NOTES</span></span>

## <span data-ttu-id="1e297-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e297-142">RELATED LINKS</span></span>

[<span data-ttu-id="1e297-143">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="1e297-143">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="1e297-144">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="1e297-144">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="1e297-145">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="1e297-145">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
