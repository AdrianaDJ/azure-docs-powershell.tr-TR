---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: 9ac7717769cef1ad147ea122ddedde3efd1e389f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936351"
---
# <span data-ttu-id="85ea6-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="85ea6-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="85ea6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85ea6-102">SYNOPSIS</span></span>
<span data-ttu-id="85ea6-103">Yönetim grubunu kaldırır</span><span class="sxs-lookup"><span data-stu-id="85ea6-103">Removes a Management Group</span></span>

## <span data-ttu-id="85ea6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="85ea6-104">SYNTAX</span></span>

### <span data-ttu-id="85ea6-105">GroupOperations (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="85ea6-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85ea6-106">Yönetim</span><span class="sxs-lookup"><span data-stu-id="85ea6-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85ea6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="85ea6-107">DESCRIPTION</span></span>
<span data-ttu-id="85ea6-108">**Remove-AzManagementGroup** cmdlet 'ı bir yönetim grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="85ea6-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="85ea6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="85ea6-109">EXAMPLES</span></span>

### <span data-ttu-id="85ea6-110">Örnek 1-yönetim grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="85ea6-110">Example 1 - Remove a Management Group</span></span>
```
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="85ea6-111">Örnek 2-bir yönetim grubunu, PSManagementGroup nesnesiyle ayırarak kaldırma</span><span class="sxs-lookup"><span data-stu-id="85ea6-111">Example 2 - Remove a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-Remove-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="85ea6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="85ea6-112">PARAMETERS</span></span>

### <span data-ttu-id="85ea6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85ea6-113">-DefaultProfile</span></span>
<span data-ttu-id="85ea6-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="85ea6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85ea6-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="85ea6-115">-GroupName</span></span>
<span data-ttu-id="85ea6-116">Yönetim grubu kimliği</span><span class="sxs-lookup"><span data-stu-id="85ea6-116">Management Group Id</span></span>

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

### <span data-ttu-id="85ea6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85ea6-117">-InputObject</span></span>
<span data-ttu-id="85ea6-118">Arama al 'dan giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="85ea6-118">Input Object from the Get call</span></span>

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

### <span data-ttu-id="85ea6-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="85ea6-119">-PassThru</span></span>
<span data-ttu-id="85ea6-120">`true`Başarılı yürütmeye dönme</span><span class="sxs-lookup"><span data-stu-id="85ea6-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="85ea6-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="85ea6-121">-Confirm</span></span>
<span data-ttu-id="85ea6-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="85ea6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85ea6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85ea6-123">-WhatIf</span></span>
<span data-ttu-id="85ea6-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="85ea6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85ea6-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="85ea6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85ea6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85ea6-126">CommonParameters</span></span>
<span data-ttu-id="85ea6-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="85ea6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85ea6-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85ea6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85ea6-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="85ea6-129">INPUTS</span></span>

### <span data-ttu-id="85ea6-130">Microsoft. Azure. Commands. resources. modeller. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="85ea6-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>
<span data-ttu-id="85ea6-131">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="85ea6-131">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="85ea6-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="85ea6-132">OUTPUTS</span></span>

### <span data-ttu-id="85ea6-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="85ea6-133">System.Boolean</span></span>

## <span data-ttu-id="85ea6-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="85ea6-134">NOTES</span></span>

## <span data-ttu-id="85ea6-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="85ea6-135">RELATED LINKS</span></span>
