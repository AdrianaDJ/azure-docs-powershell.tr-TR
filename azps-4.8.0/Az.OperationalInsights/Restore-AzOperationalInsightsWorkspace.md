---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/restore-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 01354106e3d6ad9fbe33c97f6bcd774c62be7ccf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109412"
---
# <span data-ttu-id="49880-101">Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="49880-101">Restore-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="49880-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49880-102">SYNOPSIS</span></span>
<span data-ttu-id="49880-103">Silinmiş çalışma alanını geri yükleme.</span><span class="sxs-lookup"><span data-stu-id="49880-103">Restore a deleted workspace.</span></span>

## <span data-ttu-id="49880-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="49880-104">SYNTAX</span></span>

```
Restore-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49880-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="49880-105">DESCRIPTION</span></span>
<span data-ttu-id="49880-106">Silinmiş çalışma alanını geri yükleme.</span><span class="sxs-lookup"><span data-stu-id="49880-106">Restore a deleted workspace.</span></span>

## <span data-ttu-id="49880-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="49880-107">EXAMPLES</span></span>

### <span data-ttu-id="49880-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="49880-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> $workspace = Restore-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
```

<span data-ttu-id="49880-109">Silinen çalışma alanını geri yükleme.</span><span class="sxs-lookup"><span data-stu-id="49880-109">Restore deleted workspace.</span></span>

## <span data-ttu-id="49880-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="49880-110">PARAMETERS</span></span>

### <span data-ttu-id="49880-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49880-111">-DefaultProfile</span></span>
<span data-ttu-id="49880-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="49880-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49880-113">-Force</span><span class="sxs-lookup"><span data-stu-id="49880-113">-Force</span></span>
<span data-ttu-id="49880-114">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="49880-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="49880-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="49880-115">-Location</span></span>
<span data-ttu-id="49880-116">Çalışma alanının içinde oluşturulduğu coğrafi bölge.</span><span class="sxs-lookup"><span data-stu-id="49880-116">The geographic region that the workspace will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49880-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="49880-117">-Name</span></span>
<span data-ttu-id="49880-118">Çalışma alanı adı.</span><span class="sxs-lookup"><span data-stu-id="49880-118">The workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49880-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49880-119">-ResourceGroupName</span></span>
<span data-ttu-id="49880-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="49880-120">The resource group name.</span></span>

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

### <span data-ttu-id="49880-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="49880-121">-Confirm</span></span>
<span data-ttu-id="49880-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="49880-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49880-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49880-123">-WhatIf</span></span>
<span data-ttu-id="49880-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="49880-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49880-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="49880-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49880-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49880-126">CommonParameters</span></span>
<span data-ttu-id="49880-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="49880-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49880-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="49880-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49880-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="49880-129">INPUTS</span></span>

### <span data-ttu-id="49880-130">System. String</span><span class="sxs-lookup"><span data-stu-id="49880-130">System.String</span></span>

## <span data-ttu-id="49880-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="49880-131">OUTPUTS</span></span>

### <span data-ttu-id="49880-132">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="49880-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="49880-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="49880-133">NOTES</span></span>

## <span data-ttu-id="49880-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="49880-134">RELATED LINKS</span></span>
