---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azsmartgroupstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
ms.openlocfilehash: 6c0b67bb70a364de45a88f80ca99bdec5e1d7188
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108024"
---
# <span data-ttu-id="2b236-101">Update-AzSmartGroupState</span><span class="sxs-lookup"><span data-stu-id="2b236-101">Update-AzSmartGroupState</span></span>

## <span data-ttu-id="2b236-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b236-102">SYNOPSIS</span></span>
<span data-ttu-id="2b236-103">Akıllı grup durumunu güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="2b236-103">Updates smart group state</span></span>

## <span data-ttu-id="2b236-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2b236-104">SYNTAX</span></span>

### <span data-ttu-id="2b236-105">Bysmartgroupıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2b236-105">BySmartGroupId (Default)</span></span>
```
Update-AzSmartGroupState -SmartGroupId <String> -State <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b236-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2b236-106">ByInputObject</span></span>
```
Update-AzSmartGroupState -State <String> -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b236-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b236-107">DESCRIPTION</span></span>
<span data-ttu-id="2b236-108">**Update-AzSmartGroupState** cmdlet 'i akıllı grup durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2b236-108">**Update-AzSmartGroupState** cmdlet updates smart group state.</span></span>

## <span data-ttu-id="2b236-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2b236-109">EXAMPLES</span></span>

### <span data-ttu-id="2b236-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2b236-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSmartGroupState -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Acknowledged"
```

<span data-ttu-id="2b236-111">Bu cmdlet, akıllı grup durumunu Acknowolarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2b236-111">This cmdlet updates the smart group state to Acknowleged.</span></span>

## <span data-ttu-id="2b236-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2b236-112">PARAMETERS</span></span>

### <span data-ttu-id="2b236-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b236-113">-DefaultProfile</span></span>
<span data-ttu-id="2b236-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2b236-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b236-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b236-115">-InputObject</span></span>
<span data-ttu-id="2b236-116">Ardışık düzenin giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2b236-116">Input object from pipeline.</span></span>

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

### <span data-ttu-id="2b236-117">-Smartgroupıd</span><span class="sxs-lookup"><span data-stu-id="2b236-117">-SmartGroupId</span></span>
<span data-ttu-id="2b236-118">Akıllı grup ve ResourceId için benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="2b236-118">Unique Identifier of Smart Group / ResourceId of smart group.</span></span>

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

### <span data-ttu-id="2b236-119">Durumlu</span><span class="sxs-lookup"><span data-stu-id="2b236-119">-State</span></span>
<span data-ttu-id="2b236-120">Güncelleştirilmiş akıllı Grup durumu</span><span class="sxs-lookup"><span data-stu-id="2b236-120">Updated Smart group State</span></span>

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

### <span data-ttu-id="2b236-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="2b236-121">-Confirm</span></span>
<span data-ttu-id="2b236-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2b236-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b236-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b236-123">-WhatIf</span></span>
<span data-ttu-id="2b236-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b236-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b236-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2b236-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b236-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b236-126">CommonParameters</span></span>
<span data-ttu-id="2b236-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2b236-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b236-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2b236-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b236-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2b236-129">INPUTS</span></span>

### <span data-ttu-id="2b236-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2b236-130">None</span></span>

## <span data-ttu-id="2b236-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2b236-131">OUTPUTS</span></span>

### <span data-ttu-id="2b236-132">Microsoft. Azure. Commands. AlertsManagement. Outputmodel. PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="2b236-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="2b236-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2b236-133">NOTES</span></span>

## <span data-ttu-id="2b236-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2b236-134">RELATED LINKS</span></span>
