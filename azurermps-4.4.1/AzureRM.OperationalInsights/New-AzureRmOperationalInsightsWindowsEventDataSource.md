---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: c82388dbfebb33c840b1c1066e41ab6c022e87d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589183"
---
# <span data-ttu-id="0a744-101">New-AzureRmOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="0a744-101">New-AzureRmOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="0a744-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a744-102">SYNOPSIS</span></span>
<span data-ttu-id="0a744-103">Windows işletim sistemini çalıştıran bilgisayarlardan olay günlükleri toplar.</span><span class="sxs-lookup"><span data-stu-id="0a744-103">Collects event logs from computers that run the Windows operating system.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a744-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0a744-104">SYNTAX</span></span>

### <span data-ttu-id="0a744-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0a744-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a744-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="0a744-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a744-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0a744-107">DESCRIPTION</span></span>
<span data-ttu-id="0a744-108">**Yeni-Azurermoperationalınsightswindowseventdatasource** cmdlet 'ı, Azure Operasyonel Öngörüler 'de Windows işletim sistemini çalıştıran bağlı bilgisayarlardan Windows olay günlüklerini toplayan bir veri kaynağı ekler.</span><span class="sxs-lookup"><span data-stu-id="0a744-108">The **New-AzureRmOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="0a744-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0a744-109">EXAMPLES</span></span>

## <span data-ttu-id="0a744-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0a744-110">PARAMETERS</span></span>

### <span data-ttu-id="0a744-111">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="0a744-111">-CollectErrors</span></span>
<span data-ttu-id="0a744-112">Işlemsel öngörülerle hata iletilerini topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="0a744-112">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="0a744-113">-Collectınformation</span><span class="sxs-lookup"><span data-stu-id="0a744-113">-CollectInformation</span></span>
<span data-ttu-id="0a744-114">Işlemsel Öngörüler 'in bilgi iletilerini topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="0a744-114">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="0a744-115">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="0a744-115">-CollectWarnings</span></span>
<span data-ttu-id="0a744-116">Işlemsel öngörülerle uyarı mesajları topladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="0a744-116">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="0a744-117">-EventLogName</span><span class="sxs-lookup"><span data-stu-id="0a744-117">-EventLogName</span></span>
<span data-ttu-id="0a744-118">Olay günlüğünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a744-118">Specifies the name of the event log.</span></span>

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

### <span data-ttu-id="0a744-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0a744-119">-Force</span></span>
<span data-ttu-id="0a744-120">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="0a744-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0a744-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="0a744-121">-Name</span></span>
<span data-ttu-id="0a744-122">Veri kaynağı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a744-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="0a744-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a744-123">-ResourceGroupName</span></span>
<span data-ttu-id="0a744-124">Bilgisayarları içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a744-124">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="0a744-125">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="0a744-125">-Workspace</span></span>
<span data-ttu-id="0a744-126">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a744-126">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="0a744-127">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="0a744-127">-WorkspaceName</span></span>
<span data-ttu-id="0a744-128">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a744-128">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="0a744-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="0a744-129">-Confirm</span></span>
<span data-ttu-id="0a744-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0a744-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a744-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a744-131">-WhatIf</span></span>
<span data-ttu-id="0a744-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0a744-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a744-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0a744-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a744-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a744-134">-DefaultProfile</span></span>
<span data-ttu-id="0a744-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0a744-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a744-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a744-136">CommonParameters</span></span>
<span data-ttu-id="0a744-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0a744-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a744-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a744-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a744-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0a744-139">INPUTS</span></span>

### <span data-ttu-id="0a744-140">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0a744-140">PSWorkspace</span></span>
<span data-ttu-id="0a744-141">Parametre ' çalışma alanı ', ardışık düzenin ' PSWorkspace ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="0a744-141">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="0a744-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0a744-142">OUTPUTS</span></span>

### <span data-ttu-id="0a744-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="0a744-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="0a744-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0a744-144">NOTES</span></span>

## <span data-ttu-id="0a744-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0a744-145">RELATED LINKS</span></span>

