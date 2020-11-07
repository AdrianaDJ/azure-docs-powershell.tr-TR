---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: 107881e8d9ac1f631b9a90dbf68ba096a59cefb7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752798"
---
# <span data-ttu-id="4ecbb-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="4ecbb-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="4ecbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ecbb-102">SYNOPSIS</span></span>
<span data-ttu-id="4ecbb-103">Konak grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4ecbb-103">Removes a host group.</span></span>

## <span data-ttu-id="4ecbb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4ecbb-104">SYNTAX</span></span>

### <span data-ttu-id="4ecbb-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4ecbb-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ecbb-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="4ecbb-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ecbb-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="4ecbb-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ecbb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4ecbb-108">DESCRIPTION</span></span>
<span data-ttu-id="4ecbb-109">Bu cmdlet bir konak grubunu Silecek</span><span class="sxs-lookup"><span data-stu-id="4ecbb-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="4ecbb-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4ecbb-110">EXAMPLES</span></span>

### <span data-ttu-id="4ecbb-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4ecbb-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="4ecbb-112">Bu komut, verilen konak grubunu alır ve kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4ecbb-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="4ecbb-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4ecbb-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="4ecbb-114">Bu komut, verilen konak grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4ecbb-114">This command removes the given host group.</span></span>

## <span data-ttu-id="4ecbb-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4ecbb-115">PARAMETERS</span></span>

### <span data-ttu-id="4ecbb-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="4ecbb-116">-AsJob</span></span>
<span data-ttu-id="4ecbb-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4ecbb-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ecbb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ecbb-118">-DefaultProfile</span></span>
<span data-ttu-id="4ecbb-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4ecbb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ecbb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ecbb-120">-InputObject</span></span>
<span data-ttu-id="4ecbb-121">Konak grubunun yerel nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4ecbb-121">The local object of the host group.</span></span>

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

### <span data-ttu-id="4ecbb-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="4ecbb-122">-Name</span></span>
<span data-ttu-id="4ecbb-123">Konak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4ecbb-123">The name of the host group.</span></span>

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

### <span data-ttu-id="4ecbb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ecbb-124">-ResourceGroupName</span></span>
<span data-ttu-id="4ecbb-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4ecbb-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="4ecbb-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4ecbb-126">-ResourceId</span></span>
<span data-ttu-id="4ecbb-127">Kaynağın KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4ecbb-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="4ecbb-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="4ecbb-128">-Confirm</span></span>
<span data-ttu-id="4ecbb-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4ecbb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ecbb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ecbb-130">-WhatIf</span></span>
<span data-ttu-id="4ecbb-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4ecbb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ecbb-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4ecbb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ecbb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ecbb-133">CommonParameters</span></span>
<span data-ttu-id="4ecbb-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4ecbb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ecbb-135">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4ecbb-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ecbb-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4ecbb-136">INPUTS</span></span>

### <span data-ttu-id="4ecbb-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4ecbb-137">System.String</span></span>

### <span data-ttu-id="4ecbb-138">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="4ecbb-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="4ecbb-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4ecbb-139">OUTPUTS</span></span>

### <span data-ttu-id="4ecbb-140">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="4ecbb-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4ecbb-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4ecbb-141">NOTES</span></span>

## <span data-ttu-id="4ecbb-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4ecbb-142">RELATED LINKS</span></span>
