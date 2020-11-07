---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: bcf15e36ae428277293c174df6b7a3cd55c36252
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917343"
---
# <span data-ttu-id="fb6ae-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fb6ae-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="fb6ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb6ae-102">SYNOPSIS</span></span>
<span data-ttu-id="fb6ae-103">Azure 'dan bir kullanılabilirlik kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fb6ae-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="fb6ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb6ae-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb6ae-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb6ae-105">DESCRIPTION</span></span>
<span data-ttu-id="fb6ae-106">**Remove-AzAvailabilitySet** cmdlet 'i Azure 'dan bir kullanılabilirlik kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fb6ae-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="fb6ae-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb6ae-107">EXAMPLES</span></span>

### <span data-ttu-id="fb6ae-108">Örnek 1: kullanılabilirlik kümesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="fb6ae-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="fb6ae-109">Bu komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet03 adındaki bir kullanılabilirlik kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fb6ae-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="fb6ae-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb6ae-110">PARAMETERS</span></span>

### <span data-ttu-id="fb6ae-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="fb6ae-111">-AsJob</span></span>
<span data-ttu-id="fb6ae-112">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="fb6ae-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="fb6ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb6ae-113">-DefaultProfile</span></span>
<span data-ttu-id="fb6ae-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fb6ae-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb6ae-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fb6ae-115">-Force</span></span>
<span data-ttu-id="fb6ae-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="fb6ae-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fb6ae-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="fb6ae-117">-Name</span></span>
<span data-ttu-id="fb6ae-118">Kullanılabilirlik kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="fb6ae-118">The availability set name.</span></span>

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

### <span data-ttu-id="fb6ae-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb6ae-119">-ResourceGroupName</span></span>
<span data-ttu-id="fb6ae-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb6ae-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fb6ae-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="fb6ae-121">-Confirm</span></span>
<span data-ttu-id="fb6ae-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fb6ae-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb6ae-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb6ae-123">-WhatIf</span></span>
<span data-ttu-id="fb6ae-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb6ae-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb6ae-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fb6ae-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb6ae-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb6ae-126">CommonParameters</span></span>
<span data-ttu-id="fb6ae-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb6ae-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb6ae-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb6ae-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb6ae-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb6ae-129">INPUTS</span></span>

### <span data-ttu-id="fb6ae-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fb6ae-130">System.String</span></span>

## <span data-ttu-id="fb6ae-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb6ae-131">OUTPUTS</span></span>

### <span data-ttu-id="fb6ae-132">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="fb6ae-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="fb6ae-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb6ae-133">NOTES</span></span>

## <span data-ttu-id="fb6ae-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb6ae-134">RELATED LINKS</span></span>

[<span data-ttu-id="fb6ae-135">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fb6ae-135">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="fb6ae-136">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fb6ae-136">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)


