---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroup.md
ms.openlocfilehash: 7f19e45f96dbeac1470fbcc67a7db319589ad390
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593187"
---
# <span data-ttu-id="673ed-101">Remove-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="673ed-101">Remove-AzureRmManagementGroup</span></span>

## <span data-ttu-id="673ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="673ed-102">SYNOPSIS</span></span>
<span data-ttu-id="673ed-103">Yönetim grubunu kaldırır</span><span class="sxs-lookup"><span data-stu-id="673ed-103">Removes a Management Group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="673ed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="673ed-104">SYNTAX</span></span>

### <span data-ttu-id="673ed-105">GroupOperations (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="673ed-105">GroupOperations (Default)</span></span>
```
Remove-AzureRmManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="673ed-106">Yönetim</span><span class="sxs-lookup"><span data-stu-id="673ed-106">ManagementGroupObject</span></span>
```
Remove-AzureRmManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="673ed-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="673ed-107">DESCRIPTION</span></span>
<span data-ttu-id="673ed-108">**Remove-AzureRmManagementGroup** cmdlet 'ı bir yönetim grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="673ed-108">The **Remove-AzureRmManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="673ed-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="673ed-109">EXAMPLES</span></span>

### <span data-ttu-id="673ed-110">Örnek 1-yönetim grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="673ed-110">Example 1 - Remove a Management Group</span></span>
```
PS C:\> Remove-AzureRmManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="673ed-111">Örnek 2-bir yönetim grubunu, PSManagementGroup nesnesiyle ayırarak kaldırma</span><span class="sxs-lookup"><span data-stu-id="673ed-111">Example 2 - Remove a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-Remove-AzureRmManagementGroup -GroupName "TestGroup" | Remove-AzureRmManagementGroup
```

## <span data-ttu-id="673ed-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="673ed-112">PARAMETERS</span></span>

### <span data-ttu-id="673ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="673ed-113">-DefaultProfile</span></span>
<span data-ttu-id="673ed-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="673ed-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="673ed-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="673ed-115">-GroupName</span></span>
<span data-ttu-id="673ed-116">Yönetim grubu kimliği</span><span class="sxs-lookup"><span data-stu-id="673ed-116">Management Group Id</span></span>

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

### <span data-ttu-id="673ed-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="673ed-117">-InputObject</span></span>
<span data-ttu-id="673ed-118">Arama al 'dan giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="673ed-118">Input Object from the Get call</span></span>

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

### <span data-ttu-id="673ed-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="673ed-119">-PassThru</span></span>
<span data-ttu-id="673ed-120">`true`Başarılı yürütmeye dönme</span><span class="sxs-lookup"><span data-stu-id="673ed-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="673ed-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="673ed-121">-Confirm</span></span>
<span data-ttu-id="673ed-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="673ed-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="673ed-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="673ed-123">-WhatIf</span></span>
<span data-ttu-id="673ed-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="673ed-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="673ed-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="673ed-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="673ed-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="673ed-126">CommonParameters</span></span>
<span data-ttu-id="673ed-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="673ed-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="673ed-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="673ed-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="673ed-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="673ed-129">INPUTS</span></span>

### <span data-ttu-id="673ed-130">Microsoft. Azure. Commands. resources. modeller. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="673ed-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>
<span data-ttu-id="673ed-131">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="673ed-131">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="673ed-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="673ed-132">OUTPUTS</span></span>

### <span data-ttu-id="673ed-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="673ed-133">System.Boolean</span></span>

## <span data-ttu-id="673ed-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="673ed-134">NOTES</span></span>

## <span data-ttu-id="673ed-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="673ed-135">RELATED LINKS</span></span>
