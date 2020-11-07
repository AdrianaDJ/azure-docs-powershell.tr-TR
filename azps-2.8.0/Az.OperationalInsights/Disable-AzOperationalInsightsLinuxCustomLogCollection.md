---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: EF3FE3F1-1C8F-41EB-990E-F2B30BD9D082
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: f36c6b87ed6e1fc916df228448426a441bc855ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932907"
---
# <span data-ttu-id="2443d-101">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="2443d-101">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="2443d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2443d-102">SYNOPSIS</span></span>
<span data-ttu-id="2443d-103">Linux bilgisayarlarından özel günlüklerin toplanmasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="2443d-103">Stops collection of custom logs from Linux computers.</span></span>

## <span data-ttu-id="2443d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2443d-104">SYNTAX</span></span>

### <span data-ttu-id="2443d-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2443d-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2443d-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="2443d-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2443d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2443d-107">DESCRIPTION</span></span>
<span data-ttu-id="2443d-108">**Disable-Azoperationalınsightslinuxcustomlogcollection** cmdlet 'i, bir çalışma alanındaki bağlı Linux bilgisayarlarından özel günlüklerin toplanmasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="2443d-108">The **Disable-AzOperationalInsightsLinuxCustomLogCollection** cmdlet stops collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="2443d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2443d-109">EXAMPLES</span></span>

## <span data-ttu-id="2443d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2443d-110">PARAMETERS</span></span>

### <span data-ttu-id="2443d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2443d-111">-DefaultProfile</span></span>
<span data-ttu-id="2443d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2443d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2443d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2443d-113">-ResourceGroupName</span></span>
<span data-ttu-id="2443d-114">Linux bilgisayarlarını içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2443d-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="2443d-115">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="2443d-115">-Workspace</span></span>
<span data-ttu-id="2443d-116">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2443d-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2443d-117">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="2443d-117">-WorkspaceName</span></span>
<span data-ttu-id="2443d-118">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2443d-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2443d-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="2443d-119">-Confirm</span></span>
<span data-ttu-id="2443d-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2443d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2443d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2443d-121">-WhatIf</span></span>
<span data-ttu-id="2443d-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2443d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2443d-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2443d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2443d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2443d-124">CommonParameters</span></span>
<span data-ttu-id="2443d-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2443d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2443d-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2443d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2443d-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2443d-127">INPUTS</span></span>

### <span data-ttu-id="2443d-128">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="2443d-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="2443d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2443d-129">System.String</span></span>

## <span data-ttu-id="2443d-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2443d-130">OUTPUTS</span></span>

### <span data-ttu-id="2443d-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="2443d-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="2443d-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2443d-132">NOTES</span></span>
* <span data-ttu-id="2443d-133">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, işletim, Öngörüler</span><span class="sxs-lookup"><span data-stu-id="2443d-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="2443d-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2443d-134">RELATED LINKS</span></span>

[<span data-ttu-id="2443d-135">Enable-Azoperationalınsightslinuxcustomlogcollection</span><span class="sxs-lookup"><span data-stu-id="2443d-135">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


