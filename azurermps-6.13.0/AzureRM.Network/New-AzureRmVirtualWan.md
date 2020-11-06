---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualWan.md
ms.openlocfilehash: 8d514ae4f01709d499c7685958cf13671e9b0c13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594365"
---
# <span data-ttu-id="f07d3-101">New-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="f07d3-101">New-AzureRmVirtualWan</span></span>

## <span data-ttu-id="f07d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f07d3-102">SYNOPSIS</span></span>
<span data-ttu-id="f07d3-103">Azure sanal WAN oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f07d3-103">Creates an Azure Virtual WAN.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f07d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f07d3-104">SYNTAX</span></span>

```
New-AzureRmVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f07d3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f07d3-105">DESCRIPTION</span></span>
<span data-ttu-id="f07d3-106">Yeni bir Azure VirtualWAN kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f07d3-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="f07d3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f07d3-107">EXAMPLES</span></span>

### <span data-ttu-id="f07d3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f07d3-108">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="f07d3-109">Yukarıdaki "Batı ABD" adresindeki "testRG" adlı bir kaynak grubu ve Azure 'daki bu kaynak grubunda şubeye dallanan bir Azure sanal WAN 'si oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="f07d3-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="f07d3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f07d3-110">PARAMETERS</span></span>

### <span data-ttu-id="f07d3-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="f07d3-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="f07d3-112">VirtualWan için dal trafiğine izin verin.</span><span class="sxs-lookup"><span data-stu-id="f07d3-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="f07d3-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="f07d3-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="f07d3-114">VirtualWan için VNET 'den VNET trafiğine izin verin.</span><span class="sxs-lookup"><span data-stu-id="f07d3-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="f07d3-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="f07d3-115">-AsJob</span></span>
<span data-ttu-id="f07d3-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f07d3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f07d3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f07d3-117">-DefaultProfile</span></span>
<span data-ttu-id="f07d3-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f07d3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f07d3-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="f07d3-119">-Location</span></span>
<span data-ttu-id="f07d3-120">VirtualWAN kaynağının konumu.</span><span class="sxs-lookup"><span data-stu-id="f07d3-120">The location of the VirtualWAN resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07d3-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="f07d3-121">-Name</span></span>
<span data-ttu-id="f07d3-122">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="f07d3-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07d3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f07d3-123">-ResourceGroupName</span></span>
<span data-ttu-id="f07d3-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f07d3-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07d3-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f07d3-125">-Tag</span></span>
<span data-ttu-id="f07d3-126">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="f07d3-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07d3-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="f07d3-127">-Confirm</span></span>
<span data-ttu-id="f07d3-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f07d3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f07d3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f07d3-129">-WhatIf</span></span>
<span data-ttu-id="f07d3-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f07d3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f07d3-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f07d3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f07d3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f07d3-132">CommonParameters</span></span>
<span data-ttu-id="f07d3-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f07d3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f07d3-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f07d3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f07d3-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f07d3-135">INPUTS</span></span>

### <span data-ttu-id="f07d3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f07d3-136">System.String</span></span>

### <span data-ttu-id="f07d3-137">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f07d3-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f07d3-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f07d3-138">OUTPUTS</span></span>

### <span data-ttu-id="f07d3-139">Microsoft. Azure. Commands. Network. model. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="f07d3-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="f07d3-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f07d3-140">NOTES</span></span>

## <span data-ttu-id="f07d3-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f07d3-141">RELATED LINKS</span></span>
