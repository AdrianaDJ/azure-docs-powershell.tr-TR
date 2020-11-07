---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: 17397d2bd1056b6e4280d560b2640abcacb1250a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938544"
---
# <span data-ttu-id="d6229-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="d6229-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="d6229-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6229-102">SYNOPSIS</span></span>
<span data-ttu-id="d6229-103">Konak grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d6229-103">Removes a host group.</span></span>

## <span data-ttu-id="d6229-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d6229-104">SYNTAX</span></span>

### <span data-ttu-id="d6229-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d6229-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6229-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="d6229-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6229-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="d6229-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6229-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d6229-108">DESCRIPTION</span></span>
<span data-ttu-id="d6229-109">Bu cmdlet bir konak grubunu Silecek</span><span class="sxs-lookup"><span data-stu-id="d6229-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="d6229-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d6229-110">EXAMPLES</span></span>

### <span data-ttu-id="d6229-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d6229-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="d6229-112">Bu komut, verilen konak grubunu alır ve kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d6229-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="d6229-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d6229-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="d6229-114">Bu komut, verilen konak grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d6229-114">This command removes the given host group.</span></span>

## <span data-ttu-id="d6229-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d6229-115">PARAMETERS</span></span>

### <span data-ttu-id="d6229-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="d6229-116">-AsJob</span></span>
<span data-ttu-id="d6229-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d6229-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6229-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6229-118">-DefaultProfile</span></span>
<span data-ttu-id="d6229-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d6229-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6229-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6229-120">-InputObject</span></span>
<span data-ttu-id="d6229-121">Konak grubunun yerel nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d6229-121">The local object of the host group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup
Parameter Sets: ObjectParameter
Aliases: HostGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6229-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="d6229-122">-Name</span></span>
<span data-ttu-id="d6229-123">Konak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d6229-123">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6229-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6229-124">-ResourceGroupName</span></span>
<span data-ttu-id="d6229-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d6229-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6229-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d6229-126">-ResourceId</span></span>
<span data-ttu-id="d6229-127">Kaynağın KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d6229-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6229-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="d6229-128">-Confirm</span></span>
<span data-ttu-id="d6229-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d6229-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6229-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6229-130">-WhatIf</span></span>
<span data-ttu-id="d6229-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d6229-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6229-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d6229-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6229-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6229-133">CommonParameters</span></span>
<span data-ttu-id="d6229-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d6229-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6229-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d6229-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6229-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d6229-136">INPUTS</span></span>

### <span data-ttu-id="d6229-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d6229-137">System.String</span></span>

### <span data-ttu-id="d6229-138">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="d6229-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="d6229-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d6229-139">OUTPUTS</span></span>

### <span data-ttu-id="d6229-140">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="d6229-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="d6229-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d6229-141">NOTES</span></span>

## <span data-ttu-id="d6229-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d6229-142">RELATED LINKS</span></span>
