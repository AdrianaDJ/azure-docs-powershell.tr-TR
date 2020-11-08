---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 4fb6a38ff9c79a16d150402d3a2e2be135e0c004
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275928"
---
# <span data-ttu-id="9759d-101">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="9759d-101">Get-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="9759d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9759d-102">SYNOPSIS</span></span>
<span data-ttu-id="9759d-103">Azure Log Analytics çalışma alanı altında veri kaynakları alın.</span><span class="sxs-lookup"><span data-stu-id="9759d-103">Get datasources under Azure Log Analytics workspace.</span></span>

## <span data-ttu-id="9759d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9759d-104">SYNTAX</span></span>

### <span data-ttu-id="9759d-105">ByWorkspaceNameByKind (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9759d-105">ByWorkspaceNameByKind (Default)</span></span>
```
Get-AzOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9759d-106">Byworkspace Nesnebyname</span><span class="sxs-lookup"><span data-stu-id="9759d-106">ByWorkspaceObjectByName</span></span>
```
Get-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9759d-107">By</span><span class="sxs-lookup"><span data-stu-id="9759d-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9759d-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="9759d-108">ByWorkspaceNameByName</span></span>
```
Get-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9759d-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="9759d-109">DESCRIPTION</span></span>
<span data-ttu-id="9759d-110">**Get-Azoperationalınsightsdatasource** cmdlet 'i veri kaynaklarını alır.</span><span class="sxs-lookup"><span data-stu-id="9759d-110">The **Get-AzOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="9759d-111">Alınacak bir veri kaynağı belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9759d-111">You can specify a data source to get.</span></span>
<span data-ttu-id="9759d-112">Sonuçları veri kaynağının türüne göre filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9759d-112">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="9759d-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9759d-113">EXAMPLES</span></span>

## <span data-ttu-id="9759d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9759d-114">PARAMETERS</span></span>

### <span data-ttu-id="9759d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9759d-115">-DefaultProfile</span></span>
<span data-ttu-id="9759d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9759d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9759d-117">-Tür</span><span class="sxs-lookup"><span data-stu-id="9759d-117">-Kind</span></span>
<span data-ttu-id="9759d-118">Alınacak veri kaynağı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="9759d-118">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="9759d-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9759d-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9759d-120">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="9759d-120">AzureActivityLog</span></span> 
- <span data-ttu-id="9759d-121">CustomLog</span><span class="sxs-lookup"><span data-stu-id="9759d-121">CustomLog</span></span> 
- <span data-ttu-id="9759d-122">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="9759d-122">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="9759d-123">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="9759d-123">LinuxSyslog</span></span> 
- <span data-ttu-id="9759d-124">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="9759d-124">WindowsEvent</span></span> 
- <span data-ttu-id="9759d-125">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="9759d-125">WindowsPerformanceCounter</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, ApplicationInsights

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, ApplicationInsights

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9759d-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="9759d-126">-Name</span></span>
<span data-ttu-id="9759d-127">Alınacak veri kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9759d-127">Specifies the name of a data source to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByName
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9759d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9759d-128">-ResourceGroupName</span></span>
<span data-ttu-id="9759d-129">Alınacak veri kaynaklarını içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9759d-129">Specifies the name of a resource group that contains data sources to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9759d-130">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="9759d-130">-Workspace</span></span>
<span data-ttu-id="9759d-131">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9759d-131">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByKind
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9759d-132">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="9759d-132">-WorkspaceName</span></span>
<span data-ttu-id="9759d-133">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9759d-133">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9759d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9759d-134">CommonParameters</span></span>
<span data-ttu-id="9759d-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9759d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9759d-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9759d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9759d-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9759d-137">INPUTS</span></span>

### <span data-ttu-id="9759d-138">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="9759d-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="9759d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9759d-139">System.String</span></span>

## <span data-ttu-id="9759d-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9759d-140">OUTPUTS</span></span>

### <span data-ttu-id="9759d-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="9759d-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="9759d-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9759d-142">NOTES</span></span>
* <span data-ttu-id="9759d-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, işletim, Öngörüler</span><span class="sxs-lookup"><span data-stu-id="9759d-143">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="9759d-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9759d-144">RELATED LINKS</span></span>

[<span data-ttu-id="9759d-145">Remove-Azoperationalınsightsdatasource</span><span class="sxs-lookup"><span data-stu-id="9759d-145">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="9759d-146">Set-Azoperationalınsightsdatasource</span><span class="sxs-lookup"><span data-stu-id="9759d-146">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


