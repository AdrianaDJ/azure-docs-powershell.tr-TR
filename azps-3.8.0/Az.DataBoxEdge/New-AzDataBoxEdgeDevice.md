---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 66c91c7a486638c01902f6091993143bb2e1a535
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098877"
---
# <span data-ttu-id="04964-101">New-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="04964-101">New-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="04964-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04964-102">SYNOPSIS</span></span>
<span data-ttu-id="04964-103">Yeni veri kutusu uç cihazı yapılandırır</span><span class="sxs-lookup"><span data-stu-id="04964-103">Configures a new Data Box Edge device</span></span>

## <span data-ttu-id="04964-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="04964-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04964-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="04964-105">DESCRIPTION</span></span>
<span data-ttu-id="04964-106">**New-AzDataBoxEdgeDevice** cmdlet 'i yeni bir veri kutusu uç cihazı yapılandırır</span><span class="sxs-lookup"><span data-stu-id="04964-106">The **New-AzDataBoxEdgeDevice** cmdlet configures a new Data Box Edge device</span></span>

## <span data-ttu-id="04964-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="04964-107">EXAMPLES</span></span>

### <span data-ttu-id="04964-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="04964-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="04964-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="04964-109">PARAMETERS</span></span>

### <span data-ttu-id="04964-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="04964-110">-AsJob</span></span>
<span data-ttu-id="04964-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="04964-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04964-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04964-112">-DefaultProfile</span></span>
<span data-ttu-id="04964-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="04964-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04964-114">-Konum</span><span class="sxs-lookup"><span data-stu-id="04964-114">-Location</span></span>
<span data-ttu-id="04964-115">Cihazın konumu</span><span class="sxs-lookup"><span data-stu-id="04964-115">Location of the device</span></span>

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

### <span data-ttu-id="04964-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="04964-116">-Name</span></span>
<span data-ttu-id="04964-117">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="04964-117">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04964-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04964-118">-ResourceGroupName</span></span>
<span data-ttu-id="04964-119">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="04964-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04964-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="04964-120">-Sku</span></span>
<span data-ttu-id="04964-121">Kullanılabilir SKU 'Lar Edge, ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="04964-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="04964-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="04964-122">-Confirm</span></span>
<span data-ttu-id="04964-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="04964-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04964-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04964-124">-WhatIf</span></span>
<span data-ttu-id="04964-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="04964-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04964-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="04964-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04964-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04964-127">CommonParameters</span></span>
<span data-ttu-id="04964-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="04964-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04964-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="04964-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04964-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="04964-130">INPUTS</span></span>

### <span data-ttu-id="04964-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="04964-131">None</span></span>

## <span data-ttu-id="04964-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="04964-132">OUTPUTS</span></span>

### <span data-ttu-id="04964-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="04964-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="04964-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="04964-134">NOTES</span></span>

## <span data-ttu-id="04964-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="04964-135">RELATED LINKS</span></span>
