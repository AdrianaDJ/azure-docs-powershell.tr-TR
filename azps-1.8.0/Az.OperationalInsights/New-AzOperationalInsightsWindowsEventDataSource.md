---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 4230eadc005ca53600feb2e6bc7ee2e001d7b209
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759842"
---
# <span data-ttu-id="a96ab-101">New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="a96ab-101">New-AzOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="a96ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a96ab-102">SYNOPSIS</span></span>
<span data-ttu-id="a96ab-103">Windows işletim sistemini çalıştıran bilgisayarlardan olay günlükleri toplar.</span><span class="sxs-lookup"><span data-stu-id="a96ab-103">Collects event logs from computers that run the Windows operating system.</span></span>

## <span data-ttu-id="a96ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a96ab-104">SYNTAX</span></span>

### <span data-ttu-id="a96ab-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a96ab-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a96ab-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="a96ab-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a96ab-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a96ab-107">DESCRIPTION</span></span>
<span data-ttu-id="a96ab-108">**New-Azoperationalınsightswindowseventdatasource** cmdlet 'ı, Azure Operasyonel Öngörüler 'de Windows işletim sistemini çalıştıran bağlı bilgisayarlardan Windows olay günlüklerini toplayan bir veri kaynağı ekler.</span><span class="sxs-lookup"><span data-stu-id="a96ab-108">The **New-AzOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="a96ab-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a96ab-109">EXAMPLES</span></span>

## <span data-ttu-id="a96ab-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a96ab-110">PARAMETERS</span></span>

### <span data-ttu-id="a96ab-111">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="a96ab-111">-CollectErrors</span></span>
<span data-ttu-id="a96ab-112">Işlemsel öngörülerle hata iletilerini topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="a96ab-112">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="a96ab-113">-Collectınformation</span><span class="sxs-lookup"><span data-stu-id="a96ab-113">-CollectInformation</span></span>
<span data-ttu-id="a96ab-114">Işlemsel Öngörüler 'in bilgi iletilerini topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="a96ab-114">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="a96ab-115">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="a96ab-115">-CollectWarnings</span></span>
<span data-ttu-id="a96ab-116">Işlemsel öngörülerle uyarı mesajları topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="a96ab-116">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="a96ab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a96ab-117">-DefaultProfile</span></span>
<span data-ttu-id="a96ab-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a96ab-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a96ab-119">-EventLogName</span><span class="sxs-lookup"><span data-stu-id="a96ab-119">-EventLogName</span></span>
<span data-ttu-id="a96ab-120">Olay günlüğünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a96ab-120">Specifies the name of the event log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a96ab-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a96ab-121">-Force</span></span>
<span data-ttu-id="a96ab-122">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="a96ab-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a96ab-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="a96ab-123">-Name</span></span>
<span data-ttu-id="a96ab-124">Veri kaynağı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="a96ab-124">Specifies a name for the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a96ab-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a96ab-125">-ResourceGroupName</span></span>
<span data-ttu-id="a96ab-126">Bilgisayarları içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a96ab-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="a96ab-127">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="a96ab-127">-Workspace</span></span>
<span data-ttu-id="a96ab-128">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a96ab-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="a96ab-129">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="a96ab-129">-WorkspaceName</span></span>
<span data-ttu-id="a96ab-130">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a96ab-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="a96ab-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="a96ab-131">-Confirm</span></span>
<span data-ttu-id="a96ab-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a96ab-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a96ab-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a96ab-133">-WhatIf</span></span>
<span data-ttu-id="a96ab-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a96ab-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a96ab-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a96ab-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a96ab-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a96ab-136">CommonParameters</span></span>
<span data-ttu-id="a96ab-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a96ab-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a96ab-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a96ab-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a96ab-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a96ab-139">INPUTS</span></span>

### <span data-ttu-id="a96ab-140">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a96ab-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="a96ab-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a96ab-141">System.String</span></span>

## <span data-ttu-id="a96ab-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a96ab-142">OUTPUTS</span></span>

### <span data-ttu-id="a96ab-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="a96ab-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="a96ab-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a96ab-144">NOTES</span></span>

## <span data-ttu-id="a96ab-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a96ab-145">RELATED LINKS</span></span>
