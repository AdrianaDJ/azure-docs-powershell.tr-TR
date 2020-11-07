---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 71a0089b4f593032404b71f17ba432486f5498d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937201"
---
# <span data-ttu-id="3027c-101">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="3027c-101">Disable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="3027c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3027c-102">SYNOPSIS</span></span>
<span data-ttu-id="3027c-103">Bilgisayarlardan gelen IIS günlükleri koleksiyonunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="3027c-103">Stops collection of IIS logs from computers.</span></span>

## <span data-ttu-id="3027c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3027c-104">SYNTAX</span></span>

### <span data-ttu-id="3027c-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3027c-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3027c-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="3027c-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3027c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3027c-107">DESCRIPTION</span></span>
<span data-ttu-id="3027c-108">**Disable-AzOperationalInsightsIISLogCollection** cmdlet 'i, bir çalışma alanındaki bağlı bilgisayarlardan gelen Internet Information SERVICES (IIS) günlüklerini durdurur.</span><span class="sxs-lookup"><span data-stu-id="3027c-108">The **Disable-AzOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="3027c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3027c-109">EXAMPLES</span></span>

## <span data-ttu-id="3027c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3027c-110">PARAMETERS</span></span>

### <span data-ttu-id="3027c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3027c-111">-DefaultProfile</span></span>
<span data-ttu-id="3027c-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3027c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3027c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3027c-113">-ResourceGroupName</span></span>
<span data-ttu-id="3027c-114">Bilgisayarları içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3027c-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="3027c-115">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="3027c-115">-Workspace</span></span>
<span data-ttu-id="3027c-116">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3027c-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3027c-117">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="3027c-117">-WorkspaceName</span></span>
<span data-ttu-id="3027c-118">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3027c-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3027c-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="3027c-119">-Confirm</span></span>
<span data-ttu-id="3027c-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3027c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3027c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3027c-121">-WhatIf</span></span>
<span data-ttu-id="3027c-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3027c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3027c-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3027c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3027c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3027c-124">CommonParameters</span></span>
<span data-ttu-id="3027c-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3027c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3027c-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3027c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3027c-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3027c-127">INPUTS</span></span>

### <span data-ttu-id="3027c-128">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="3027c-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="3027c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3027c-129">System.String</span></span>

## <span data-ttu-id="3027c-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3027c-130">OUTPUTS</span></span>

### <span data-ttu-id="3027c-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="3027c-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="3027c-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3027c-132">NOTES</span></span>
* <span data-ttu-id="3027c-133">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, işletim, Öngörüler</span><span class="sxs-lookup"><span data-stu-id="3027c-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="3027c-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3027c-134">RELATED LINKS</span></span>

[<span data-ttu-id="3027c-135">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="3027c-135">Enable-AzOperationalInsightsIISLogCollection</span></span>](./Enable-AzOperationalInsightsIISLogCollection.md)


