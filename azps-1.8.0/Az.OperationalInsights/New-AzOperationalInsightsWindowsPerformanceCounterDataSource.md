---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowsperformancecounterdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: e775f07249b9ec8a8987986d4e614e9fc66a25f8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759841"
---
# <span data-ttu-id="7d17b-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="7d17b-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="7d17b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d17b-102">SYNOPSIS</span></span>
<span data-ttu-id="7d17b-103">Windows işletim sistemini çalıştıran bağlı bilgisayarlara Windows performans sayacı veri kaynağı ekler.</span><span class="sxs-lookup"><span data-stu-id="7d17b-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="7d17b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7d17b-104">SYNTAX</span></span>

### <span data-ttu-id="7d17b-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7d17b-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d17b-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="7d17b-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d17b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7d17b-107">DESCRIPTION</span></span>
<span data-ttu-id="7d17b-108">**New-AzOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet 'ı, Windows işletim sistemini çalıştıran bağlı bilgisayarlara Windows performans sayacı veri kaynağı ekler.</span><span class="sxs-lookup"><span data-stu-id="7d17b-108">The **New-AzOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="7d17b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7d17b-109">EXAMPLES</span></span>

## <span data-ttu-id="7d17b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7d17b-110">PARAMETERS</span></span>

### <span data-ttu-id="7d17b-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="7d17b-111">-CounterName</span></span>
<span data-ttu-id="7d17b-112">Bir sayacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d17b-112">Specifies the name of a counter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d17b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d17b-113">-DefaultProfile</span></span>
<span data-ttu-id="7d17b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7d17b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d17b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7d17b-115">-Force</span></span>
<span data-ttu-id="7d17b-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="7d17b-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7d17b-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="7d17b-117">-InstanceName</span></span>
<span data-ttu-id="7d17b-118">Bir örnek adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d17b-118">Specifies an instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d17b-119">-Intervalsaniye</span><span class="sxs-lookup"><span data-stu-id="7d17b-119">-IntervalSeconds</span></span>
<span data-ttu-id="7d17b-120">Koleksiyon aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d17b-120">Specifies the interval of collection.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d17b-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="7d17b-121">-Name</span></span>
<span data-ttu-id="7d17b-122">Veri kaynağı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d17b-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="7d17b-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="7d17b-123">-ObjectName</span></span>
<span data-ttu-id="7d17b-124">Nesnenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d17b-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="7d17b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d17b-125">-ResourceGroupName</span></span>
<span data-ttu-id="7d17b-126">Bilgisayarları içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d17b-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="7d17b-127">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="7d17b-127">-UseLegacyCollector</span></span>
<span data-ttu-id="7d17b-128">Eski toplayıcıya veya varsayılan toplayıcıya kullanın.</span><span class="sxs-lookup"><span data-stu-id="7d17b-128">Use legacy collector or the default collector.</span></span>

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

### <span data-ttu-id="7d17b-129">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="7d17b-129">-Workspace</span></span>
<span data-ttu-id="7d17b-130">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d17b-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7d17b-131">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="7d17b-131">-WorkspaceName</span></span>
<span data-ttu-id="7d17b-132">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d17b-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7d17b-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="7d17b-133">-Confirm</span></span>
<span data-ttu-id="7d17b-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7d17b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d17b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d17b-135">-WhatIf</span></span>
<span data-ttu-id="7d17b-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7d17b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d17b-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7d17b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d17b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d17b-138">CommonParameters</span></span>
<span data-ttu-id="7d17b-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7d17b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d17b-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d17b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d17b-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7d17b-141">INPUTS</span></span>

### <span data-ttu-id="7d17b-142">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="7d17b-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="7d17b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7d17b-143">System.String</span></span>

### <span data-ttu-id="7d17b-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7d17b-144">System.Int32</span></span>

## <span data-ttu-id="7d17b-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7d17b-145">OUTPUTS</span></span>

### <span data-ttu-id="7d17b-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="7d17b-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="7d17b-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7d17b-147">NOTES</span></span>

## <span data-ttu-id="7d17b-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7d17b-148">RELATED LINKS</span></span>
