---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 47AFBAC7-8818-4788-B685-7AB4DCD6C2DE
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 0a39dae7ebdc6cc2c1fcc1b77ceb9b5d8e330d66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932904"
---
# <span data-ttu-id="ff953-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="ff953-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="ff953-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff953-102">SYNOPSIS</span></span>
<span data-ttu-id="ff953-103">Linux bilgisayarlarından performans sayaçlarının toplanmasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="ff953-103">Stops collection of performance counters from Linux computers.</span></span>

## <span data-ttu-id="ff953-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ff953-104">SYNTAX</span></span>

### <span data-ttu-id="ff953-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ff953-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff953-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="ff953-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff953-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ff953-107">DESCRIPTION</span></span>
<span data-ttu-id="ff953-108">**Disable-Azoperationalınsightslinuxperformancecbir** cmdlet, bir çalışma alanındaki bağlı Linux bilgisayarlarından performans sayaçlarının toplanmasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="ff953-108">The **Disable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet stops collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="ff953-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ff953-109">EXAMPLES</span></span>

## <span data-ttu-id="ff953-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ff953-110">PARAMETERS</span></span>

### <span data-ttu-id="ff953-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff953-111">-DefaultProfile</span></span>
<span data-ttu-id="ff953-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ff953-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff953-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff953-113">-ResourceGroupName</span></span>
<span data-ttu-id="ff953-114">Linux bilgisayarlarını içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ff953-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="ff953-115">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="ff953-115">-Workspace</span></span>
<span data-ttu-id="ff953-116">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ff953-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ff953-117">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="ff953-117">-WorkspaceName</span></span>
<span data-ttu-id="ff953-118">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ff953-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ff953-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="ff953-119">-Confirm</span></span>
<span data-ttu-id="ff953-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ff953-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff953-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff953-121">-WhatIf</span></span>
<span data-ttu-id="ff953-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ff953-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff953-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ff953-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff953-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff953-124">CommonParameters</span></span>
<span data-ttu-id="ff953-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ff953-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff953-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff953-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff953-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ff953-127">INPUTS</span></span>

### <span data-ttu-id="ff953-128">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ff953-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="ff953-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ff953-129">System.String</span></span>

## <span data-ttu-id="ff953-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ff953-130">OUTPUTS</span></span>

### <span data-ttu-id="ff953-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="ff953-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="ff953-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ff953-132">NOTES</span></span>
* <span data-ttu-id="ff953-133">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, işletim, Öngörüler</span><span class="sxs-lookup"><span data-stu-id="ff953-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="ff953-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ff953-134">RELATED LINKS</span></span>

[<span data-ttu-id="ff953-135">Enable-Azoperationalınsightslinuxperformancecollection</span><span class="sxs-lookup"><span data-stu-id="ff953-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="ff953-136">New-Azoperationalınsightslinuxsyslogdatasource</span><span class="sxs-lookup"><span data-stu-id="ff953-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


