---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: f83a52281cbe244e91b22300b7f10582d6ca6349
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096937"
---
# <span data-ttu-id="f4d96-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="f4d96-101">New-AzHostGroup</span></span>

## <span data-ttu-id="f4d96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4d96-102">SYNOPSIS</span></span>
<span data-ttu-id="f4d96-103">Konak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f4d96-103">Creates a host group.</span></span>

## <span data-ttu-id="f4d96-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f4d96-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4d96-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f4d96-105">DESCRIPTION</span></span>
<span data-ttu-id="f4d96-106">Bu cmdlet bir konak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f4d96-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="f4d96-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f4d96-107">EXAMPLES</span></span>

### <span data-ttu-id="f4d96-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f4d96-108">Example 1</span></span>
```
PS C:\> New-AzHostGroup -ResourceGroupName $resourceGroupName -Name $hostGroupName -Location $location -Zone $zone

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="f4d96-109">Bu komut, verilen konum ve bölgede bir konak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f4d96-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="f4d96-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f4d96-110">PARAMETERS</span></span>

### <span data-ttu-id="f4d96-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="f4d96-111">-AsJob</span></span>
<span data-ttu-id="f4d96-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f4d96-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4d96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4d96-113">-DefaultProfile</span></span>
<span data-ttu-id="f4d96-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f4d96-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4d96-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="f4d96-115">-Location</span></span>
<span data-ttu-id="f4d96-116">Konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4d96-116">Specifies location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4d96-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="f4d96-117">-Name</span></span>
<span data-ttu-id="f4d96-118">Konak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4d96-118">Specifies the name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4d96-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="f4d96-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="f4d96-120">Konak grubunun yayılacağı hata etki alanlarının sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4d96-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="f4d96-121">En küçük değer 1 ve en yüksek değer 3 ' dir.</span><span class="sxs-lookup"><span data-stu-id="f4d96-121">The minimum value is 1 and the maximum value is 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4d96-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4d96-122">-ResourceGroupName</span></span>
<span data-ttu-id="f4d96-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f4d96-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="f4d96-124">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f4d96-124">-Tag</span></span>
<span data-ttu-id="f4d96-125">Etiketleri belirtir</span><span class="sxs-lookup"><span data-stu-id="f4d96-125">Specifies Tags</span></span>

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

### <span data-ttu-id="f4d96-126">-Bölge</span><span class="sxs-lookup"><span data-stu-id="f4d96-126">-Zone</span></span>
<span data-ttu-id="f4d96-127">Konak grubunun bölgelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4d96-127">Specifies Zones of the host group.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4d96-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="f4d96-128">-Confirm</span></span>
<span data-ttu-id="f4d96-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f4d96-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4d96-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4d96-130">-WhatIf</span></span>
<span data-ttu-id="f4d96-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f4d96-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4d96-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f4d96-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4d96-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d96-133">CommonParameters</span></span>
<span data-ttu-id="f4d96-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f4d96-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d96-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f4d96-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d96-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f4d96-136">INPUTS</span></span>

### <span data-ttu-id="f4d96-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f4d96-137">System.String</span></span>

## <span data-ttu-id="f4d96-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f4d96-138">OUTPUTS</span></span>

### <span data-ttu-id="f4d96-139">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="f4d96-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="f4d96-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f4d96-140">NOTES</span></span>

## <span data-ttu-id="f4d96-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f4d96-141">RELATED LINKS</span></span>
