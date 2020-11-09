---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 5d7c10227876c2ee5b8eeab12623457be0f64aa8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325630"
---
# <span data-ttu-id="b0870-101">New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="b0870-101">New-AzOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="b0870-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0870-102">SYNOPSIS</span></span>
<span data-ttu-id="b0870-103">Windows işletim sistemini çalıştıran bilgisayarlardan olay günlükleri toplar.</span><span class="sxs-lookup"><span data-stu-id="b0870-103">Collects event logs from computers that run the Windows operating system.</span></span>

## <span data-ttu-id="b0870-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b0870-104">SYNTAX</span></span>

### <span data-ttu-id="b0870-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b0870-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0870-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="b0870-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0870-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b0870-107">DESCRIPTION</span></span>
<span data-ttu-id="b0870-108">**New-Azoperationalınsightswindowseventdatasource** cmdlet 'ı, Azure Operasyonel Öngörüler 'de Windows işletim sistemini çalıştıran bağlı bilgisayarlardan Windows olay günlüklerini toplayan bir veri kaynağı ekler.</span><span class="sxs-lookup"><span data-stu-id="b0870-108">The **New-AzOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="b0870-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b0870-109">EXAMPLES</span></span>

### <span data-ttu-id="b0870-110">Örnek 1: sistem Windows olayı veri kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="b0870-110">Example 1: Create system Windows event data source</span></span>
```
$EventLogNames       = @()
$EventLogNames      += 'Directory Service'
$EventLogNames      += 'Microsoft-Windows-EventCollector/Operational'
$EventLogNames      += 'System'
$ResourceGroupName   = 'MyResourceGroup'
$WorkspaceName       = 'MyWorkspaceName'

$Count = 0
foreach ($EventLogName in $EventLogNames) {
    $Count++
    $null = New-AzOperationalInsightsWindowsEventDataSource `
    -ResourceGroupName $ResourceGroupName `
    -WorkspaceName $WorkspaceName `
    -Name "Windows-event-$($Count)" `
    -EventLogName $EventLogName `
    -CollectErrors `
    -CollectWarnings `
    -CollectInformation
}

Get-AzOperationalInsightsDataSource `
   -ResourceGroupName $ResourceGroupName `
   -WorkspaceName $WorkspaceName `
   -Kind 'WindowsEvent'
```

## <span data-ttu-id="b0870-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b0870-111">PARAMETERS</span></span>

### <span data-ttu-id="b0870-112">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="b0870-112">-CollectErrors</span></span>
<span data-ttu-id="b0870-113">Işlemsel öngörülerle hata iletilerini topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="b0870-113">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="b0870-114">-Collectınformation</span><span class="sxs-lookup"><span data-stu-id="b0870-114">-CollectInformation</span></span>
<span data-ttu-id="b0870-115">Işlemsel Öngörüler 'in bilgi iletilerini topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="b0870-115">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="b0870-116">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="b0870-116">-CollectWarnings</span></span>
<span data-ttu-id="b0870-117">Işlemsel öngörülerle uyarı mesajları topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="b0870-117">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="b0870-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0870-118">-DefaultProfile</span></span>
<span data-ttu-id="b0870-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b0870-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0870-120">-EventLogName</span><span class="sxs-lookup"><span data-stu-id="b0870-120">-EventLogName</span></span>
<span data-ttu-id="b0870-121">Olay günlüğünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0870-121">Specifies the name of the event log.</span></span>

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

### <span data-ttu-id="b0870-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b0870-122">-Force</span></span>
<span data-ttu-id="b0870-123">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="b0870-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b0870-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="b0870-124">-Name</span></span>
<span data-ttu-id="b0870-125">Veri kaynağı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0870-125">Specifies a name for the data source.</span></span> <span data-ttu-id="b0870-126">Ad, Azure portalında gösterilmez ve tüm dizeler benzersiz olduğu sürece kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b0870-126">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="b0870-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0870-127">-ResourceGroupName</span></span>
<span data-ttu-id="b0870-128">Bilgisayarları içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0870-128">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="b0870-129">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="b0870-129">-Workspace</span></span>
<span data-ttu-id="b0870-130">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0870-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="b0870-131">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="b0870-131">-WorkspaceName</span></span>
<span data-ttu-id="b0870-132">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0870-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="b0870-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="b0870-133">-Confirm</span></span>
<span data-ttu-id="b0870-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b0870-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0870-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0870-135">-WhatIf</span></span>
<span data-ttu-id="b0870-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b0870-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0870-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b0870-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0870-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0870-138">CommonParameters</span></span>
<span data-ttu-id="b0870-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b0870-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0870-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0870-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0870-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b0870-141">INPUTS</span></span>

### <span data-ttu-id="b0870-142">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="b0870-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="b0870-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b0870-143">System.String</span></span>

## <span data-ttu-id="b0870-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b0870-144">OUTPUTS</span></span>

### <span data-ttu-id="b0870-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="b0870-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="b0870-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b0870-146">NOTES</span></span>

## <span data-ttu-id="b0870-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b0870-147">RELATED LINKS</span></span>
