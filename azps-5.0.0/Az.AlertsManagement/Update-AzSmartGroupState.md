---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azsmartgroupstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
ms.openlocfilehash: 6c0b67bb70a364de45a88f80ca99bdec5e1d7188
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279136"
---
# <span data-ttu-id="e793b-101">Update-AzSmartGroupState</span><span class="sxs-lookup"><span data-stu-id="e793b-101">Update-AzSmartGroupState</span></span>

## <span data-ttu-id="e793b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e793b-102">SYNOPSIS</span></span>
<span data-ttu-id="e793b-103">Akıllı grup durumunu güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="e793b-103">Updates smart group state</span></span>

## <span data-ttu-id="e793b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e793b-104">SYNTAX</span></span>

### <span data-ttu-id="e793b-105">Bysmartgroupıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e793b-105">BySmartGroupId (Default)</span></span>
```
Update-AzSmartGroupState -SmartGroupId <String> -State <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e793b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e793b-106">ByInputObject</span></span>
```
Update-AzSmartGroupState -State <String> -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e793b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e793b-107">DESCRIPTION</span></span>
<span data-ttu-id="e793b-108">**Update-AzSmartGroupState** cmdlet 'i akıllı grup durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e793b-108">**Update-AzSmartGroupState** cmdlet updates smart group state.</span></span>

## <span data-ttu-id="e793b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e793b-109">EXAMPLES</span></span>

### <span data-ttu-id="e793b-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e793b-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSmartGroupState -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Acknowledged"
```

<span data-ttu-id="e793b-111">Bu cmdlet, akıllı grup durumunu Acknowolarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e793b-111">This cmdlet updates the smart group state to Acknowleged.</span></span>

## <span data-ttu-id="e793b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e793b-112">PARAMETERS</span></span>

### <span data-ttu-id="e793b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e793b-113">-DefaultProfile</span></span>
<span data-ttu-id="e793b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e793b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e793b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e793b-115">-InputObject</span></span>
<span data-ttu-id="e793b-116">Ardışık düzenin giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e793b-116">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e793b-117">-Smartgroupıd</span><span class="sxs-lookup"><span data-stu-id="e793b-117">-SmartGroupId</span></span>
<span data-ttu-id="e793b-118">Akıllı grup ve ResourceId için benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="e793b-118">Unique Identifier of Smart Group / ResourceId of smart group.</span></span>

```yaml
Type: System.String
Parameter Sets: BySmartGroupId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e793b-119">Durumlu</span><span class="sxs-lookup"><span data-stu-id="e793b-119">-State</span></span>
<span data-ttu-id="e793b-120">Güncelleştirilmiş akıllı Grup durumu</span><span class="sxs-lookup"><span data-stu-id="e793b-120">Updated Smart group State</span></span>

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

### <span data-ttu-id="e793b-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="e793b-121">-Confirm</span></span>
<span data-ttu-id="e793b-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e793b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e793b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e793b-123">-WhatIf</span></span>
<span data-ttu-id="e793b-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e793b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e793b-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e793b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e793b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e793b-126">CommonParameters</span></span>
<span data-ttu-id="e793b-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e793b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e793b-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e793b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e793b-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e793b-129">INPUTS</span></span>

### <span data-ttu-id="e793b-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e793b-130">None</span></span>

## <span data-ttu-id="e793b-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e793b-131">OUTPUTS</span></span>

### <span data-ttu-id="e793b-132">Microsoft. Azure. Commands. AlertsManagement. Outputmodel. PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="e793b-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="e793b-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e793b-133">NOTES</span></span>

## <span data-ttu-id="e793b-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e793b-134">RELATED LINKS</span></span>
