---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 10141D75-B58D-42B0-B0A6-92FF630E534C
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 16fea9de0415fe13986633120b4db60777e24906
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759864"
---
# <span data-ttu-id="3d172-101">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="3d172-101">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="3d172-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d172-102">SYNOPSIS</span></span>
<span data-ttu-id="3d172-103">Linux bilgisayarlarından performans sayaçları toplamayı başlatır.</span><span class="sxs-lookup"><span data-stu-id="3d172-103">Starts collection of performance counters from Linux computers.</span></span>

## <span data-ttu-id="3d172-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d172-104">SYNTAX</span></span>

### <span data-ttu-id="3d172-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3d172-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d172-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="3d172-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d172-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d172-107">DESCRIPTION</span></span>
<span data-ttu-id="3d172-108">**Enable-Azoperationalınsightslinuxperformancecbir** cmdlet, bir çalışma alanındaki bağlı Linux bilgisayarlarından performans sayaçlarının toplanmasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="3d172-108">The **Enable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet starts collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="3d172-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d172-109">EXAMPLES</span></span>

## <span data-ttu-id="3d172-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d172-110">PARAMETERS</span></span>

### <span data-ttu-id="3d172-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d172-111">-DefaultProfile</span></span>
<span data-ttu-id="3d172-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3d172-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d172-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d172-113">-ResourceGroupName</span></span>
<span data-ttu-id="3d172-114">Linux bilgisayarlarını içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d172-114">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d172-115">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="3d172-115">-Workspace</span></span>
<span data-ttu-id="3d172-116">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d172-116">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d172-117">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="3d172-117">-WorkspaceName</span></span>
<span data-ttu-id="3d172-118">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d172-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d172-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="3d172-119">-Confirm</span></span>
<span data-ttu-id="3d172-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3d172-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d172-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d172-121">-WhatIf</span></span>
<span data-ttu-id="3d172-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d172-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d172-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3d172-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d172-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d172-124">CommonParameters</span></span>
<span data-ttu-id="3d172-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d172-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d172-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d172-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d172-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d172-127">INPUTS</span></span>

### <span data-ttu-id="3d172-128">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="3d172-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="3d172-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3d172-129">System.String</span></span>

## <span data-ttu-id="3d172-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d172-130">OUTPUTS</span></span>

### <span data-ttu-id="3d172-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="3d172-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="3d172-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d172-132">NOTES</span></span>
* <span data-ttu-id="3d172-133">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, işletim, Öngörüler</span><span class="sxs-lookup"><span data-stu-id="3d172-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="3d172-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d172-134">RELATED LINKS</span></span>

[<span data-ttu-id="3d172-135">Disable-Azoperationalınsightslinuxperformancecollection</span><span class="sxs-lookup"><span data-stu-id="3d172-135">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)


