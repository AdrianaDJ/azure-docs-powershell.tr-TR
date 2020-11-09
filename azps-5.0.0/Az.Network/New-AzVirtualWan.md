---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 9969ee8009e1a0cd3cf5e071f01bd03035455bde
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323260"
---
# <span data-ttu-id="e94f0-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e94f0-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="e94f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e94f0-102">SYNOPSIS</span></span>
<span data-ttu-id="e94f0-103">Azure sanal WAN oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e94f0-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="e94f0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e94f0-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-VirtualWANType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e94f0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e94f0-105">DESCRIPTION</span></span>
<span data-ttu-id="e94f0-106">Yeni bir Azure VirtualWAN kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e94f0-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="e94f0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e94f0-107">EXAMPLES</span></span>

### <span data-ttu-id="e94f0-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e94f0-108">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="e94f0-109">Yukarıdaki "Batı ABD" adresindeki "testRG" adlı bir kaynak grubu ve Azure 'daki bu kaynak grubunda şubeye dallanan bir Azure sanal WAN 'si oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e94f0-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="e94f0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e94f0-110">PARAMETERS</span></span>

### <span data-ttu-id="e94f0-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="e94f0-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="e94f0-112">VirtualWan için dal trafiğine izin verin.</span><span class="sxs-lookup"><span data-stu-id="e94f0-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="e94f0-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="e94f0-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="e94f0-114">VirtualWan için VNET 'den VNET trafiğine izin verin.</span><span class="sxs-lookup"><span data-stu-id="e94f0-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="e94f0-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="e94f0-115">-AsJob</span></span>
<span data-ttu-id="e94f0-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e94f0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e94f0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e94f0-117">-DefaultProfile</span></span>
<span data-ttu-id="e94f0-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e94f0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e94f0-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="e94f0-119">-Location</span></span>
<span data-ttu-id="e94f0-120">VirtualWAN kaynağının konumu.</span><span class="sxs-lookup"><span data-stu-id="e94f0-120">The location of the VirtualWAN resource.</span></span>

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

### <span data-ttu-id="e94f0-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="e94f0-121">-Name</span></span>
<span data-ttu-id="e94f0-122">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="e94f0-122">The resource name.</span></span>

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

### <span data-ttu-id="e94f0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e94f0-123">-ResourceGroupName</span></span>
<span data-ttu-id="e94f0-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e94f0-124">The resource group name.</span></span>

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

### <span data-ttu-id="e94f0-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e94f0-125">-Tag</span></span>
<span data-ttu-id="e94f0-126">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="e94f0-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e94f0-127">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="e94f0-127">-VirtualWANType</span></span>
<span data-ttu-id="e94f0-128">Sanal WAN 'ın türü.</span><span class="sxs-lookup"><span data-stu-id="e94f0-128">The type of the Virtual Wan.</span></span>

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

### <span data-ttu-id="e94f0-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="e94f0-129">-Confirm</span></span>
<span data-ttu-id="e94f0-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e94f0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e94f0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e94f0-131">-WhatIf</span></span>
<span data-ttu-id="e94f0-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e94f0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e94f0-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e94f0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e94f0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e94f0-134">CommonParameters</span></span>
<span data-ttu-id="e94f0-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e94f0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e94f0-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e94f0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e94f0-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e94f0-137">INPUTS</span></span>

### <span data-ttu-id="e94f0-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e94f0-138">None</span></span>

## <span data-ttu-id="e94f0-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e94f0-139">OUTPUTS</span></span>

### <span data-ttu-id="e94f0-140">Microsoft. Azure. Commands. Network. model. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e94f0-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="e94f0-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e94f0-141">NOTES</span></span>

## <span data-ttu-id="e94f0-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e94f0-142">RELATED LINKS</span></span>

[<span data-ttu-id="e94f0-143">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e94f0-143">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="e94f0-144">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e94f0-144">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="e94f0-145">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e94f0-145">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
