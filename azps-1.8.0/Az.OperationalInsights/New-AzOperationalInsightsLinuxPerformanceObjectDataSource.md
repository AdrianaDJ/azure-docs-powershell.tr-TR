---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 6372abc324601761c07ec4c69d52db188172ba0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759846"
---
# <span data-ttu-id="91751-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="91751-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="91751-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91751-102">SYNOPSIS</span></span>
<span data-ttu-id="91751-103">Çalışma alanındaki tüm Linux bilgisayarlara performans sayaçları ekler.</span><span class="sxs-lookup"><span data-stu-id="91751-103">Adds performance counters to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="91751-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91751-104">SYNTAX</span></span>

### <span data-ttu-id="91751-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="91751-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91751-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="91751-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91751-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="91751-107">DESCRIPTION</span></span>
<span data-ttu-id="91751-108">**New-Azoperationalınsightslinuxperformanceobjectdatasource** cmdlet 'i bir çalışma alanındaki tüm Linux bilgisayarlara veri topladığı performans sayaçlarını ekler.</span><span class="sxs-lookup"><span data-stu-id="91751-108">The **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="91751-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91751-109">EXAMPLES</span></span>

## <span data-ttu-id="91751-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91751-110">PARAMETERS</span></span>

### <span data-ttu-id="91751-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="91751-111">-CounterNames</span></span>
<span data-ttu-id="91751-112">Sayaçların adlarının dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="91751-112">Specifies an array of names of counters.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91751-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91751-113">-DefaultProfile</span></span>
<span data-ttu-id="91751-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="91751-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91751-115">-Force</span><span class="sxs-lookup"><span data-stu-id="91751-115">-Force</span></span>
<span data-ttu-id="91751-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="91751-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="91751-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="91751-117">-InstanceName</span></span>
<span data-ttu-id="91751-118">Bir örnek adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="91751-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="91751-119">-Intervalsaniye</span><span class="sxs-lookup"><span data-stu-id="91751-119">-IntervalSeconds</span></span>
<span data-ttu-id="91751-120">Koleksiyon aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91751-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="91751-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="91751-121">-Name</span></span>
<span data-ttu-id="91751-122">Veri kaynağı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="91751-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="91751-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="91751-123">-ObjectName</span></span>
<span data-ttu-id="91751-124">Nesnenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91751-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="91751-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91751-125">-ResourceGroupName</span></span>
<span data-ttu-id="91751-126">Linux bilgisayarlarını içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91751-126">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="91751-127">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="91751-127">-Workspace</span></span>
<span data-ttu-id="91751-128">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91751-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="91751-129">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="91751-129">-WorkspaceName</span></span>
<span data-ttu-id="91751-130">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91751-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="91751-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="91751-131">-Confirm</span></span>
<span data-ttu-id="91751-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="91751-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91751-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91751-133">-WhatIf</span></span>
<span data-ttu-id="91751-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="91751-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91751-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="91751-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91751-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91751-136">CommonParameters</span></span>
<span data-ttu-id="91751-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91751-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91751-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91751-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91751-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91751-139">INPUTS</span></span>

### <span data-ttu-id="91751-140">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="91751-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="91751-141">System. String</span><span class="sxs-lookup"><span data-stu-id="91751-141">System.String</span></span>

### <span data-ttu-id="91751-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="91751-142">System.String[]</span></span>

### <span data-ttu-id="91751-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="91751-143">System.Int32</span></span>

## <span data-ttu-id="91751-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91751-144">OUTPUTS</span></span>

### <span data-ttu-id="91751-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="91751-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="91751-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91751-146">NOTES</span></span>

## <span data-ttu-id="91751-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91751-147">RELATED LINKS</span></span>

[<span data-ttu-id="91751-148">Disable-Azoperationalınsightslinuxperformancecollection</span><span class="sxs-lookup"><span data-stu-id="91751-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="91751-149">Enable-Azoperationalınsightslinuxperformancecollection</span><span class="sxs-lookup"><span data-stu-id="91751-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)


