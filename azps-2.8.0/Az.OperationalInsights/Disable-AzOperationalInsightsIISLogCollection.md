---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: d808f7287a8ae3c03d86867f409d28820325e858
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932908"
---
# <span data-ttu-id="ff2cd-101">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="ff2cd-101">Disable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="ff2cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff2cd-102">SYNOPSIS</span></span>
<span data-ttu-id="ff2cd-103">Bilgisayarlardan gelen IIS günlükleri koleksiyonunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="ff2cd-103">Stops collection of IIS logs from computers.</span></span>

## <span data-ttu-id="ff2cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ff2cd-104">SYNTAX</span></span>

### <span data-ttu-id="ff2cd-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ff2cd-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff2cd-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="ff2cd-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff2cd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ff2cd-107">DESCRIPTION</span></span>
<span data-ttu-id="ff2cd-108">**Disable-AzOperationalInsightsIISLogCollection** cmdlet 'i, bir çalışma alanındaki bağlı bilgisayarlardan gelen Internet Information SERVICES (IIS) günlüklerini durdurur.</span><span class="sxs-lookup"><span data-stu-id="ff2cd-108">The **Disable-AzOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="ff2cd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ff2cd-109">EXAMPLES</span></span>

## <span data-ttu-id="ff2cd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ff2cd-110">PARAMETERS</span></span>

### <span data-ttu-id="ff2cd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff2cd-111">-DefaultProfile</span></span>
<span data-ttu-id="ff2cd-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ff2cd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff2cd-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff2cd-113">-ResourceGroupName</span></span>
<span data-ttu-id="ff2cd-114">Bilgisayarları içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ff2cd-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="ff2cd-115">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="ff2cd-115">-Workspace</span></span>
<span data-ttu-id="ff2cd-116">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ff2cd-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ff2cd-117">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="ff2cd-117">-WorkspaceName</span></span>
<span data-ttu-id="ff2cd-118">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ff2cd-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ff2cd-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="ff2cd-119">-Confirm</span></span>
<span data-ttu-id="ff2cd-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ff2cd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff2cd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff2cd-121">-WhatIf</span></span>
<span data-ttu-id="ff2cd-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ff2cd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff2cd-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ff2cd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff2cd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff2cd-124">CommonParameters</span></span>
<span data-ttu-id="ff2cd-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ff2cd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff2cd-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff2cd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff2cd-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ff2cd-127">INPUTS</span></span>

### <span data-ttu-id="ff2cd-128">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ff2cd-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="ff2cd-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ff2cd-129">System.String</span></span>

## <span data-ttu-id="ff2cd-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ff2cd-130">OUTPUTS</span></span>

### <span data-ttu-id="ff2cd-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="ff2cd-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="ff2cd-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ff2cd-132">NOTES</span></span>
* <span data-ttu-id="ff2cd-133">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, işletim, Öngörüler</span><span class="sxs-lookup"><span data-stu-id="ff2cd-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="ff2cd-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ff2cd-134">RELATED LINKS</span></span>

[<span data-ttu-id="ff2cd-135">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="ff2cd-135">Enable-AzOperationalInsightsIISLogCollection</span></span>](./Enable-AzOperationalInsightsIISLogCollection.md)

