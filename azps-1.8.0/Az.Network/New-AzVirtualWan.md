---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 17ace5a209a34fc65d79efaac0bfb477e00b2472
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760252"
---
# <span data-ttu-id="9bd27-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="9bd27-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="9bd27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bd27-102">SYNOPSIS</span></span>
<span data-ttu-id="9bd27-103">Azure sanal WAN oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9bd27-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="9bd27-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9bd27-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bd27-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9bd27-105">DESCRIPTION</span></span>
<span data-ttu-id="9bd27-106">Yeni bir Azure VirtualWAN kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9bd27-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="9bd27-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9bd27-107">EXAMPLES</span></span>

### <span data-ttu-id="9bd27-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9bd27-108">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="9bd27-109">Yukarıdaki "Batı ABD" adresindeki "testRG" adlı bir kaynak grubu ve Azure 'daki bu kaynak grubunda şubeye dallanan bir Azure sanal WAN 'si oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9bd27-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="9bd27-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9bd27-110">PARAMETERS</span></span>

### <span data-ttu-id="9bd27-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="9bd27-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="9bd27-112">VirtualWan için dal trafiğine izin verin.</span><span class="sxs-lookup"><span data-stu-id="9bd27-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="9bd27-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="9bd27-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="9bd27-114">VirtualWan için VNET 'den VNET trafiğine izin verin.</span><span class="sxs-lookup"><span data-stu-id="9bd27-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="9bd27-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="9bd27-115">-AsJob</span></span>
<span data-ttu-id="9bd27-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9bd27-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9bd27-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bd27-117">-DefaultProfile</span></span>
<span data-ttu-id="9bd27-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9bd27-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bd27-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="9bd27-119">-Location</span></span>
<span data-ttu-id="9bd27-120">VirtualWAN kaynağının konumu.</span><span class="sxs-lookup"><span data-stu-id="9bd27-120">The location of the VirtualWAN resource.</span></span>

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

### <span data-ttu-id="9bd27-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="9bd27-121">-Name</span></span>
<span data-ttu-id="9bd27-122">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="9bd27-122">The resource name.</span></span>

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

### <span data-ttu-id="9bd27-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bd27-123">-ResourceGroupName</span></span>
<span data-ttu-id="9bd27-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9bd27-124">The resource group name.</span></span>

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

### <span data-ttu-id="9bd27-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="9bd27-125">-Tag</span></span>
<span data-ttu-id="9bd27-126">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="9bd27-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="9bd27-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="9bd27-127">-Confirm</span></span>
<span data-ttu-id="9bd27-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9bd27-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bd27-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bd27-129">-WhatIf</span></span>
<span data-ttu-id="9bd27-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9bd27-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bd27-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9bd27-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bd27-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bd27-132">CommonParameters</span></span>
<span data-ttu-id="9bd27-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9bd27-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bd27-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bd27-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bd27-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9bd27-135">INPUTS</span></span>

### <span data-ttu-id="9bd27-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9bd27-136">None</span></span>

## <span data-ttu-id="9bd27-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9bd27-137">OUTPUTS</span></span>

### <span data-ttu-id="9bd27-138">Microsoft. Azure. Commands. Network. model. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="9bd27-138">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="9bd27-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9bd27-139">NOTES</span></span>

## <span data-ttu-id="9bd27-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9bd27-140">RELATED LINKS</span></span>

[<span data-ttu-id="9bd27-141">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="9bd27-141">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="9bd27-142">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="9bd27-142">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="9bd27-143">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="9bd27-143">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
