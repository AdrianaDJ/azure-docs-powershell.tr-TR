---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: 7dccf9410ff4d03503763354aabbe6b02d0c0c6d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752814"
---
# <span data-ttu-id="2dfcd-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2dfcd-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="2dfcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dfcd-102">SYNOPSIS</span></span>
<span data-ttu-id="2dfcd-103">Azure 'dan bir kullanılabilirlik kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2dfcd-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="2dfcd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2dfcd-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dfcd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2dfcd-105">DESCRIPTION</span></span>
<span data-ttu-id="2dfcd-106">**Remove-AzAvailabilitySet** cmdlet 'i Azure 'dan bir kullanılabilirlik kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2dfcd-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="2dfcd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2dfcd-107">EXAMPLES</span></span>

### <span data-ttu-id="2dfcd-108">Örnek 1: kullanılabilirlik kümesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="2dfcd-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="2dfcd-109">Bu komut, ResourceGroup11 adındaki kaynak grubundaki AvailabilitySet03 adındaki bir kullanılabilirlik kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2dfcd-109">This command removes an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="2dfcd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2dfcd-110">PARAMETERS</span></span>

### <span data-ttu-id="2dfcd-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="2dfcd-111">-AsJob</span></span>
<span data-ttu-id="2dfcd-112">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="2dfcd-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2dfcd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dfcd-113">-DefaultProfile</span></span>
<span data-ttu-id="2dfcd-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2dfcd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2dfcd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2dfcd-115">-Force</span></span>
<span data-ttu-id="2dfcd-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="2dfcd-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dfcd-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="2dfcd-117">-Name</span></span>
<span data-ttu-id="2dfcd-118">Kullanılabilirlik kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="2dfcd-118">The availability set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dfcd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dfcd-119">-ResourceGroupName</span></span>
<span data-ttu-id="2dfcd-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2dfcd-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2dfcd-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="2dfcd-121">-Confirm</span></span>
<span data-ttu-id="2dfcd-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2dfcd-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dfcd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dfcd-123">-WhatIf</span></span>
<span data-ttu-id="2dfcd-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2dfcd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dfcd-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2dfcd-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dfcd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dfcd-126">CommonParameters</span></span>
<span data-ttu-id="2dfcd-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2dfcd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dfcd-128">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2dfcd-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dfcd-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2dfcd-129">INPUTS</span></span>

### <span data-ttu-id="2dfcd-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2dfcd-130">System.String</span></span>

## <span data-ttu-id="2dfcd-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2dfcd-131">OUTPUTS</span></span>

### <span data-ttu-id="2dfcd-132">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2dfcd-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2dfcd-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2dfcd-133">NOTES</span></span>

## <span data-ttu-id="2dfcd-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2dfcd-134">RELATED LINKS</span></span>

[<span data-ttu-id="2dfcd-135">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2dfcd-135">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="2dfcd-136">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2dfcd-136">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)


