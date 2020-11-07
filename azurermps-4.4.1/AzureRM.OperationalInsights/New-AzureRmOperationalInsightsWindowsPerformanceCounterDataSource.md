---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: dfdea6498ac7f553dafeea186a8b60f157cbd904
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762428"
---
# <span data-ttu-id="d0c4e-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="d0c4e-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="d0c4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0c4e-102">SYNOPSIS</span></span>
<span data-ttu-id="d0c4e-103">Windows işletim sistemini çalıştıran bağlı bilgisayarlara Windows performans sayacı veri kaynağı ekler.</span><span class="sxs-lookup"><span data-stu-id="d0c4e-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0c4e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d0c4e-104">SYNTAX</span></span>

### <span data-ttu-id="d0c4e-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d0c4e-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0c4e-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="d0c4e-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0c4e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d0c4e-107">DESCRIPTION</span></span>
<span data-ttu-id="d0c4e-108">**New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet 'ı, Windows işletim sistemini çalıştıran bağlı bilgisayarlara Windows performans sayacı veri kaynağı ekler.</span><span class="sxs-lookup"><span data-stu-id="d0c4e-108">The **New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="d0c4e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d0c4e-109">EXAMPLES</span></span>

## <span data-ttu-id="d0c4e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d0c4e-110">PARAMETERS</span></span>

### <span data-ttu-id="d0c4e-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="d0c4e-111">-CounterName</span></span>
<span data-ttu-id="d0c4e-112">Bir sayacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0c4e-112">Specifies the name of a counter.</span></span>

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

### <span data-ttu-id="d0c4e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d0c4e-113">-Force</span></span>
<span data-ttu-id="d0c4e-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="d0c4e-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d0c4e-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d0c4e-115">-InstanceName</span></span>
<span data-ttu-id="d0c4e-116">Bir örnek adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0c4e-116">Specifies an instance name.</span></span>

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

### <span data-ttu-id="d0c4e-117">-Intervalsaniye</span><span class="sxs-lookup"><span data-stu-id="d0c4e-117">-IntervalSeconds</span></span>
<span data-ttu-id="d0c4e-118">Koleksiyon aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0c4e-118">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="d0c4e-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="d0c4e-119">-Name</span></span>
<span data-ttu-id="d0c4e-120">Veri kaynağı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0c4e-120">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="d0c4e-121">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="d0c4e-121">-ObjectName</span></span>
<span data-ttu-id="d0c4e-122">Nesnenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0c4e-122">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="d0c4e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0c4e-123">-ResourceGroupName</span></span>
<span data-ttu-id="d0c4e-124">Bilgisayarları içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0c4e-124">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="d0c4e-125">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="d0c4e-125">-UseLegacyCollector</span></span>
<span data-ttu-id="d0c4e-126">Eski toplayıcıya veya varsayılan toplayıcıya kullanın.</span><span class="sxs-lookup"><span data-stu-id="d0c4e-126">Use legacy collector or the default collector.</span></span>

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

### <span data-ttu-id="d0c4e-127">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="d0c4e-127">-Workspace</span></span>
<span data-ttu-id="d0c4e-128">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0c4e-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d0c4e-129">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="d0c4e-129">-WorkspaceName</span></span>
<span data-ttu-id="d0c4e-130">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0c4e-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d0c4e-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="d0c4e-131">-Confirm</span></span>
<span data-ttu-id="d0c4e-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d0c4e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0c4e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0c4e-133">-WhatIf</span></span>
<span data-ttu-id="d0c4e-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d0c4e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0c4e-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d0c4e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0c4e-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0c4e-136">-DefaultProfile</span></span>
<span data-ttu-id="d0c4e-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d0c4e-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0c4e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0c4e-138">CommonParameters</span></span>
<span data-ttu-id="d0c4e-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d0c4e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0c4e-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0c4e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0c4e-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d0c4e-141">INPUTS</span></span>

### <span data-ttu-id="d0c4e-142">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d0c4e-142">PSWorkspace</span></span>
<span data-ttu-id="d0c4e-143">Parametre ' çalışma alanı ', ardışık düzenin ' PSWorkspace ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d0c4e-143">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="d0c4e-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d0c4e-144">OUTPUTS</span></span>

### <span data-ttu-id="d0c4e-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="d0c4e-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d0c4e-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d0c4e-146">NOTES</span></span>

## <span data-ttu-id="d0c4e-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d0c4e-147">RELATED LINKS</span></span>

