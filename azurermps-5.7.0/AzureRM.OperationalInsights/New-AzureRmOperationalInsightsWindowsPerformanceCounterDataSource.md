---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightswindowsperformancecounterdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: b827c9d133ff6fc0bb9df0e1e3e25c3eea23916f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588136"
---
# <span data-ttu-id="bab8f-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="bab8f-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="bab8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bab8f-102">SYNOPSIS</span></span>
<span data-ttu-id="bab8f-103">Windows işletim sistemini çalıştıran bağlı bilgisayarlara Windows performans sayacı veri kaynağı ekler.</span><span class="sxs-lookup"><span data-stu-id="bab8f-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bab8f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bab8f-104">SYNTAX</span></span>

### <span data-ttu-id="bab8f-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bab8f-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bab8f-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="bab8f-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bab8f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bab8f-107">DESCRIPTION</span></span>
<span data-ttu-id="bab8f-108">**New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet 'ı, Windows işletim sistemini çalıştıran bağlı bilgisayarlara Windows performans sayacı veri kaynağı ekler.</span><span class="sxs-lookup"><span data-stu-id="bab8f-108">The **New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="bab8f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bab8f-109">EXAMPLES</span></span>

## <span data-ttu-id="bab8f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bab8f-110">PARAMETERS</span></span>

### <span data-ttu-id="bab8f-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="bab8f-111">-CounterName</span></span>
<span data-ttu-id="bab8f-112">Bir sayacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bab8f-112">Specifies the name of a counter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bab8f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bab8f-113">-DefaultProfile</span></span>
<span data-ttu-id="bab8f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bab8f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bab8f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bab8f-115">-Force</span></span>
<span data-ttu-id="bab8f-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="bab8f-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bab8f-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="bab8f-117">-InstanceName</span></span>
<span data-ttu-id="bab8f-118">Bir örnek adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="bab8f-118">Specifies an instance name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bab8f-119">-Intervalsaniye</span><span class="sxs-lookup"><span data-stu-id="bab8f-119">-IntervalSeconds</span></span>
<span data-ttu-id="bab8f-120">Koleksiyon aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bab8f-120">Specifies the interval of collection.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bab8f-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="bab8f-121">-Name</span></span>
<span data-ttu-id="bab8f-122">Veri kaynağı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="bab8f-122">Specifies a name for the data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bab8f-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="bab8f-123">-ObjectName</span></span>
<span data-ttu-id="bab8f-124">Nesnenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bab8f-124">Specifies the name of an object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bab8f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bab8f-125">-ResourceGroupName</span></span>
<span data-ttu-id="bab8f-126">Bilgisayarları içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bab8f-126">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bab8f-127">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="bab8f-127">-UseLegacyCollector</span></span>
<span data-ttu-id="bab8f-128">Eski toplayıcıya veya varsayılan toplayıcıya kullanın.</span><span class="sxs-lookup"><span data-stu-id="bab8f-128">Use legacy collector or the default collector.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bab8f-129">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="bab8f-129">-Workspace</span></span>
<span data-ttu-id="bab8f-130">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bab8f-130">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bab8f-131">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="bab8f-131">-WorkspaceName</span></span>
<span data-ttu-id="bab8f-132">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bab8f-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bab8f-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="bab8f-133">-Confirm</span></span>
<span data-ttu-id="bab8f-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bab8f-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bab8f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bab8f-135">-WhatIf</span></span>
<span data-ttu-id="bab8f-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bab8f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bab8f-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bab8f-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bab8f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bab8f-138">CommonParameters</span></span>
<span data-ttu-id="bab8f-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bab8f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bab8f-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bab8f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bab8f-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bab8f-141">INPUTS</span></span>

### <span data-ttu-id="bab8f-142">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="bab8f-142">PSWorkspace</span></span>
<span data-ttu-id="bab8f-143">Parametre ' çalışma alanı ', ardışık düzenin ' PSWorkspace ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="bab8f-143">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="bab8f-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bab8f-144">OUTPUTS</span></span>

### <span data-ttu-id="bab8f-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="bab8f-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="bab8f-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bab8f-146">NOTES</span></span>

## <span data-ttu-id="bab8f-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bab8f-147">RELATED LINKS</span></span>

