---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: a1f37a96d5be5443d2fb28c5a52964dd1612fc6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591319"
---
# <span data-ttu-id="d94f4-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="d94f4-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="d94f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d94f4-102">SYNOPSIS</span></span>
<span data-ttu-id="d94f4-103">Çalışma alanındaki tüm Linux bilgisayarlara performans sayaçları ekler.</span><span class="sxs-lookup"><span data-stu-id="d94f4-103">Adds performance counters to all Linux computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d94f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d94f4-104">SYNTAX</span></span>

### <span data-ttu-id="d94f4-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d94f4-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d94f4-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="d94f4-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d94f4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d94f4-107">DESCRIPTION</span></span>
<span data-ttu-id="d94f4-108">**Yeni-Azurermoperationalınsightslinuxperformanceobjectdatasource** cmdlet, bir çalışma alanındaki tüm Linux bilgisayarlara veri topladığı performans sayaçlarını ekler.</span><span class="sxs-lookup"><span data-stu-id="d94f4-108">The **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="d94f4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d94f4-109">EXAMPLES</span></span>

## <span data-ttu-id="d94f4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d94f4-110">PARAMETERS</span></span>

### <span data-ttu-id="d94f4-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="d94f4-111">-CounterNames</span></span>
<span data-ttu-id="d94f4-112">Sayaçların adlarının dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d94f4-112">Specifies an array of names of counters.</span></span>

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

### <span data-ttu-id="d94f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d94f4-113">-DefaultProfile</span></span>
<span data-ttu-id="d94f4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d94f4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d94f4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d94f4-115">-Force</span></span>
<span data-ttu-id="d94f4-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="d94f4-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d94f4-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d94f4-117">-InstanceName</span></span>
<span data-ttu-id="d94f4-118">Bir örnek adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="d94f4-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="d94f4-119">-Intervalsaniye</span><span class="sxs-lookup"><span data-stu-id="d94f4-119">-IntervalSeconds</span></span>
<span data-ttu-id="d94f4-120">Koleksiyon aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d94f4-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="d94f4-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="d94f4-121">-Name</span></span>
<span data-ttu-id="d94f4-122">Veri kaynağı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="d94f4-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="d94f4-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="d94f4-123">-ObjectName</span></span>
<span data-ttu-id="d94f4-124">Nesnenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d94f4-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="d94f4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d94f4-125">-ResourceGroupName</span></span>
<span data-ttu-id="d94f4-126">Linux bilgisayarlarını içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d94f4-126">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="d94f4-127">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="d94f4-127">-Workspace</span></span>
<span data-ttu-id="d94f4-128">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d94f4-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d94f4-129">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="d94f4-129">-WorkspaceName</span></span>
<span data-ttu-id="d94f4-130">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d94f4-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d94f4-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="d94f4-131">-Confirm</span></span>
<span data-ttu-id="d94f4-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d94f4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d94f4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d94f4-133">-WhatIf</span></span>
<span data-ttu-id="d94f4-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d94f4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d94f4-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d94f4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d94f4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d94f4-136">CommonParameters</span></span>
<span data-ttu-id="d94f4-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d94f4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d94f4-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d94f4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d94f4-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d94f4-139">INPUTS</span></span>

### <span data-ttu-id="d94f4-140">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d94f4-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="d94f4-141">Parametreler: çalışma alanı (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d94f4-141">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="d94f4-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d94f4-142">System.String</span></span>

### <span data-ttu-id="d94f4-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="d94f4-143">System.String[]</span></span>

### <span data-ttu-id="d94f4-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d94f4-144">System.Int32</span></span>

## <span data-ttu-id="d94f4-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d94f4-145">OUTPUTS</span></span>

### <span data-ttu-id="d94f4-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="d94f4-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d94f4-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d94f4-147">NOTES</span></span>

## <span data-ttu-id="d94f4-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d94f4-148">RELATED LINKS</span></span>

[<span data-ttu-id="d94f4-149">Disable-Azurermoperationalınsightslinuxperformancecollection</span><span class="sxs-lookup"><span data-stu-id="d94f4-149">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="d94f4-150">Enable-Azurermoperationalınsightslinuxperformancecollection</span><span class="sxs-lookup"><span data-stu-id="d94f4-150">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)


