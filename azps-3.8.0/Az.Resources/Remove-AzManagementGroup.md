---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: ddbc088ec14ed09ca879ba1134292921f255784a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097333"
---
# <span data-ttu-id="84cbf-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="84cbf-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="84cbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84cbf-102">SYNOPSIS</span></span>
<span data-ttu-id="84cbf-103">Yönetim grubunu kaldırır</span><span class="sxs-lookup"><span data-stu-id="84cbf-103">Removes a Management Group</span></span>

## <span data-ttu-id="84cbf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="84cbf-104">SYNTAX</span></span>

### <span data-ttu-id="84cbf-105">GroupOperations (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="84cbf-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84cbf-106">Yönetim</span><span class="sxs-lookup"><span data-stu-id="84cbf-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84cbf-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="84cbf-107">DESCRIPTION</span></span>
<span data-ttu-id="84cbf-108">**Remove-AzManagementGroup** cmdlet 'ı bir yönetim grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="84cbf-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="84cbf-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="84cbf-109">EXAMPLES</span></span>

### <span data-ttu-id="84cbf-110">Örnek 1-yönetim grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="84cbf-110">Example 1 - Remove a Management Group</span></span>
```
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="84cbf-111">Örnek 2-bir yönetim grubunu, PSManagementGroup nesnesiyle ayırarak kaldırma</span><span class="sxs-lookup"><span data-stu-id="84cbf-111">Example 2 - Remove a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-Remove-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="84cbf-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="84cbf-112">PARAMETERS</span></span>

### <span data-ttu-id="84cbf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84cbf-113">-DefaultProfile</span></span>
<span data-ttu-id="84cbf-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="84cbf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84cbf-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="84cbf-115">-GroupName</span></span>
<span data-ttu-id="84cbf-116">Yönetim grubu kimliği</span><span class="sxs-lookup"><span data-stu-id="84cbf-116">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84cbf-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84cbf-117">-InputObject</span></span>
<span data-ttu-id="84cbf-118">Arama al 'dan giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="84cbf-118">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84cbf-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="84cbf-119">-PassThru</span></span>
<span data-ttu-id="84cbf-120">`true`Başarılı yürütmeye dönme</span><span class="sxs-lookup"><span data-stu-id="84cbf-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="84cbf-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="84cbf-121">-Confirm</span></span>
<span data-ttu-id="84cbf-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="84cbf-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84cbf-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84cbf-123">-WhatIf</span></span>
<span data-ttu-id="84cbf-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="84cbf-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84cbf-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="84cbf-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84cbf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84cbf-126">CommonParameters</span></span>
<span data-ttu-id="84cbf-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="84cbf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84cbf-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="84cbf-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84cbf-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="84cbf-129">INPUTS</span></span>

### <span data-ttu-id="84cbf-130">Microsoft. Azure. Commands. resources. modeller. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="84cbf-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="84cbf-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="84cbf-131">OUTPUTS</span></span>

### <span data-ttu-id="84cbf-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="84cbf-132">System.Boolean</span></span>

## <span data-ttu-id="84cbf-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="84cbf-133">NOTES</span></span>

## <span data-ttu-id="84cbf-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="84cbf-134">RELATED LINKS</span></span>
