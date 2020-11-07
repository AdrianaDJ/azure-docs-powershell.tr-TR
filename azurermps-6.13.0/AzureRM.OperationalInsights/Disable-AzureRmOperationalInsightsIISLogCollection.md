---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/disable-azurermoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 085aa91321f9e263e4fa5620f982beb01eab2b16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762240"
---
# <span data-ttu-id="d3b45-101">Disable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="d3b45-101">Disable-AzureRmOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="d3b45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3b45-102">SYNOPSIS</span></span>
<span data-ttu-id="d3b45-103">Bilgisayarlardan gelen IIS günlükleri koleksiyonunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="d3b45-103">Stops collection of IIS logs from computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3b45-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3b45-104">SYNTAX</span></span>

### <span data-ttu-id="d3b45-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d3b45-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3b45-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="d3b45-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3b45-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3b45-107">DESCRIPTION</span></span>
<span data-ttu-id="d3b45-108">**Disable-AzureRmOperationalInsightsIISLogCollection** cmdlet 'i, bir çalışma alanındaki bağlı bilgisayarlardan gelen Internet Information SERVICES (IIS) günlüklerini durdurur.</span><span class="sxs-lookup"><span data-stu-id="d3b45-108">The **Disable-AzureRmOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="d3b45-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3b45-109">EXAMPLES</span></span>

## <span data-ttu-id="d3b45-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3b45-110">PARAMETERS</span></span>

### <span data-ttu-id="d3b45-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3b45-111">-DefaultProfile</span></span>
<span data-ttu-id="d3b45-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d3b45-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3b45-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3b45-113">-ResourceGroupName</span></span>
<span data-ttu-id="d3b45-114">Bilgisayarları içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3b45-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="d3b45-115">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="d3b45-115">-Workspace</span></span>
<span data-ttu-id="d3b45-116">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3b45-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d3b45-117">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="d3b45-117">-WorkspaceName</span></span>
<span data-ttu-id="d3b45-118">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3b45-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d3b45-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="d3b45-119">-Confirm</span></span>
<span data-ttu-id="d3b45-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d3b45-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3b45-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3b45-121">-WhatIf</span></span>
<span data-ttu-id="d3b45-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d3b45-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3b45-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d3b45-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3b45-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3b45-124">CommonParameters</span></span>
<span data-ttu-id="d3b45-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3b45-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3b45-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3b45-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3b45-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3b45-127">INPUTS</span></span>

### <span data-ttu-id="d3b45-128">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d3b45-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="d3b45-129">Parametreler: çalışma alanı (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d3b45-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="d3b45-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d3b45-130">System.String</span></span>

## <span data-ttu-id="d3b45-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3b45-131">OUTPUTS</span></span>

### <span data-ttu-id="d3b45-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="d3b45-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d3b45-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3b45-133">NOTES</span></span>
* <span data-ttu-id="d3b45-134">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, işletim, Öngörüler</span><span class="sxs-lookup"><span data-stu-id="d3b45-134">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="d3b45-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3b45-135">RELATED LINKS</span></span>

[<span data-ttu-id="d3b45-136">Enable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="d3b45-136">Enable-AzureRmOperationalInsightsIISLogCollection</span></span>](./Enable-AzureRmOperationalInsightsIISLogCollection.md)


