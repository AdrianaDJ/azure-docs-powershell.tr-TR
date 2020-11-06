---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightswindowsperformancecounterdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: 5a772007850342bd400666a5815d6d8b936f7c5d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591314"
---
# <span data-ttu-id="8ebd5-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="8ebd5-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="8ebd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ebd5-102">SYNOPSIS</span></span>
<span data-ttu-id="8ebd5-103">Windows işletim sistemini çalıştıran bağlı bilgisayarlara Windows performans sayacı veri kaynağı ekler.</span><span class="sxs-lookup"><span data-stu-id="8ebd5-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ebd5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8ebd5-104">SYNTAX</span></span>

### <span data-ttu-id="8ebd5-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8ebd5-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ebd5-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="8ebd5-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ebd5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ebd5-107">DESCRIPTION</span></span>
<span data-ttu-id="8ebd5-108">**New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet 'ı, Windows işletim sistemini çalıştıran bağlı bilgisayarlara Windows performans sayacı veri kaynağı ekler.</span><span class="sxs-lookup"><span data-stu-id="8ebd5-108">The **New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="8ebd5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8ebd5-109">EXAMPLES</span></span>

## <span data-ttu-id="8ebd5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8ebd5-110">PARAMETERS</span></span>

### <span data-ttu-id="8ebd5-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="8ebd5-111">-CounterName</span></span>
<span data-ttu-id="8ebd5-112">Bir sayacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ebd5-112">Specifies the name of a counter.</span></span>

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

### <span data-ttu-id="8ebd5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ebd5-113">-DefaultProfile</span></span>
<span data-ttu-id="8ebd5-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8ebd5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ebd5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8ebd5-115">-Force</span></span>
<span data-ttu-id="8ebd5-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="8ebd5-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8ebd5-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="8ebd5-117">-InstanceName</span></span>
<span data-ttu-id="8ebd5-118">Bir örnek adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ebd5-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="8ebd5-119">-Intervalsaniye</span><span class="sxs-lookup"><span data-stu-id="8ebd5-119">-IntervalSeconds</span></span>
<span data-ttu-id="8ebd5-120">Koleksiyon aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ebd5-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="8ebd5-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="8ebd5-121">-Name</span></span>
<span data-ttu-id="8ebd5-122">Veri kaynağı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ebd5-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="8ebd5-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="8ebd5-123">-ObjectName</span></span>
<span data-ttu-id="8ebd5-124">Nesnenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ebd5-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="8ebd5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ebd5-125">-ResourceGroupName</span></span>
<span data-ttu-id="8ebd5-126">Bilgisayarları içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ebd5-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="8ebd5-127">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="8ebd5-127">-UseLegacyCollector</span></span>
<span data-ttu-id="8ebd5-128">Eski toplayıcıya veya varsayılan toplayıcıya kullanın.</span><span class="sxs-lookup"><span data-stu-id="8ebd5-128">Use legacy collector or the default collector.</span></span>

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

### <span data-ttu-id="8ebd5-129">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="8ebd5-129">-Workspace</span></span>
<span data-ttu-id="8ebd5-130">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ebd5-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="8ebd5-131">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="8ebd5-131">-WorkspaceName</span></span>
<span data-ttu-id="8ebd5-132">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ebd5-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="8ebd5-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="8ebd5-133">-Confirm</span></span>
<span data-ttu-id="8ebd5-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8ebd5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ebd5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ebd5-135">-WhatIf</span></span>
<span data-ttu-id="8ebd5-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8ebd5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ebd5-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8ebd5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ebd5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ebd5-138">CommonParameters</span></span>
<span data-ttu-id="8ebd5-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8ebd5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ebd5-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ebd5-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ebd5-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8ebd5-141">INPUTS</span></span>

### <span data-ttu-id="8ebd5-142">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="8ebd5-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="8ebd5-143">Parametreler: çalışma alanı (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8ebd5-143">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="8ebd5-144">System. String</span><span class="sxs-lookup"><span data-stu-id="8ebd5-144">System.String</span></span>

### <span data-ttu-id="8ebd5-145">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8ebd5-145">System.Int32</span></span>

## <span data-ttu-id="8ebd5-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8ebd5-146">OUTPUTS</span></span>

### <span data-ttu-id="8ebd5-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="8ebd5-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="8ebd5-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8ebd5-148">NOTES</span></span>

## <span data-ttu-id="8ebd5-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8ebd5-149">RELATED LINKS</span></span>
