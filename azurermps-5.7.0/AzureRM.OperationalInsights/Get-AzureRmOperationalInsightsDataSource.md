---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 057437e55fd7877154343bdbfc5f25d216412b8e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590372"
---
# <span data-ttu-id="702d4-101">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="702d4-101">Get-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="702d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="702d4-102">SYNOPSIS</span></span>
<span data-ttu-id="702d4-103">Azure Log Analytics çalışma alanı altında veri kaynakları alın.</span><span class="sxs-lookup"><span data-stu-id="702d4-103">Get datasources under Azure Log Analytics workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="702d4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="702d4-104">SYNTAX</span></span>

### <span data-ttu-id="702d4-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="702d4-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="702d4-106">Byworkspace Nesnebyname</span><span class="sxs-lookup"><span data-stu-id="702d4-106">ByWorkspaceObjectByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="702d4-107">By</span><span class="sxs-lookup"><span data-stu-id="702d4-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="702d4-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="702d4-108">ByWorkspaceNameByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="702d4-109">ByWorkspaceNameByKind</span><span class="sxs-lookup"><span data-stu-id="702d4-109">ByWorkspaceNameByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="702d4-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="702d4-110">DESCRIPTION</span></span>
<span data-ttu-id="702d4-111">**Get-Azurermoperationalınsightsdatasource** cmdlet 'i veri kaynaklarını alır.</span><span class="sxs-lookup"><span data-stu-id="702d4-111">The **Get-AzureRmOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="702d4-112">Alınacak bir veri kaynağı belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="702d4-112">You can specify a data source to get.</span></span>
<span data-ttu-id="702d4-113">Sonuçları veri kaynağının türüne göre filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="702d4-113">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="702d4-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="702d4-114">EXAMPLES</span></span>

## <span data-ttu-id="702d4-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="702d4-115">PARAMETERS</span></span>

### <span data-ttu-id="702d4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="702d4-116">-DefaultProfile</span></span>
<span data-ttu-id="702d4-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="702d4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="702d4-118">-Tür</span><span class="sxs-lookup"><span data-stu-id="702d4-118">-Kind</span></span>
<span data-ttu-id="702d4-119">Alınacak veri kaynağı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="702d4-119">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="702d4-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="702d4-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="702d4-121">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="702d4-121">AzureActivityLog</span></span> 
- <span data-ttu-id="702d4-122">CustomLog</span><span class="sxs-lookup"><span data-stu-id="702d4-122">CustomLog</span></span> 
- <span data-ttu-id="702d4-123">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="702d4-123">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="702d4-124">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="702d4-124">LinuxSyslog</span></span> 
- <span data-ttu-id="702d4-125">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="702d4-125">WindowsEvent</span></span> 
- <span data-ttu-id="702d4-126">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="702d4-126">WindowsPerformanceCounter</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceObjectByKind
Aliases: 
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByKind
Aliases: 
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="702d4-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="702d4-127">-Name</span></span>
<span data-ttu-id="702d4-128">Alınacak veri kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="702d4-128">Specifies the name of a data source to get.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceObjectByName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByName
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="702d4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="702d4-129">-ResourceGroupName</span></span>
<span data-ttu-id="702d4-130">Alınacak veri kaynaklarını içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="702d4-130">Specifies the name of a resource group that contains data sources to get.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByKind
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="702d4-131">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="702d4-131">-Workspace</span></span>
<span data-ttu-id="702d4-132">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="702d4-132">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObjectByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObjectByKind
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="702d4-133">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="702d4-133">-WorkspaceName</span></span>
<span data-ttu-id="702d4-134">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="702d4-134">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByKind
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="702d4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="702d4-135">CommonParameters</span></span>
<span data-ttu-id="702d4-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="702d4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="702d4-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="702d4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="702d4-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="702d4-138">INPUTS</span></span>

### <span data-ttu-id="702d4-139">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="702d4-139">PSWorkspace</span></span>
<span data-ttu-id="702d4-140">Parametre ' çalışma alanı ', ardışık düzenin ' PSWorkspace ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="702d4-140">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

### <span data-ttu-id="702d4-141">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="702d4-141">PSWorkspace</span></span>
<span data-ttu-id="702d4-142">Parametre ' çalışma alanı ', ardışık düzenin ' PSWorkspace ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="702d4-142">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="702d4-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="702d4-143">OUTPUTS</span></span>

### <span data-ttu-id="702d4-144">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource]</span><span class="sxs-lookup"><span data-stu-id="702d4-144">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource]</span></span>

### <span data-ttu-id="702d4-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="702d4-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="702d4-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="702d4-146">NOTES</span></span>
* <span data-ttu-id="702d4-147">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, işletim, Öngörüler</span><span class="sxs-lookup"><span data-stu-id="702d4-147">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="702d4-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="702d4-148">RELATED LINKS</span></span>

[<span data-ttu-id="702d4-149">Remove-Azurermoperationalınsightsdatasource</span><span class="sxs-lookup"><span data-stu-id="702d4-149">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="702d4-150">Set-Azurermoperationalınsightsdatasource</span><span class="sxs-lookup"><span data-stu-id="702d4-150">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


