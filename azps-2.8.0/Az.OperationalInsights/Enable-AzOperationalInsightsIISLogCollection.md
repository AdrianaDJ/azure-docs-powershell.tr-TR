---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 75b037903adf52b1ba1407ff40e2bfbb610a6dc9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932901"
---
# <span data-ttu-id="7e4e0-101">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="7e4e0-101">Enable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="7e4e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e4e0-102">SYNOPSIS</span></span>
<span data-ttu-id="7e4e0-103">Bir çalışma alanındaki bilgisayarlardan IIS günlükleri koleksiyonunu başlatır.</span><span class="sxs-lookup"><span data-stu-id="7e4e0-103">Starts collection of IIS logs from computers in a workspace.</span></span>

## <span data-ttu-id="7e4e0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e4e0-104">SYNTAX</span></span>

### <span data-ttu-id="7e4e0-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7e4e0-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e4e0-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="7e4e0-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e4e0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e4e0-107">DESCRIPTION</span></span>
<span data-ttu-id="7e4e0-108">**Enable-AzOperationalInsightsIISLogCollection** cmdlet 'i, bir çalışma alanındaki bağlı bilgisayarlardan Internet Information SERVICES (IIS) günlüklerini başlatır.</span><span class="sxs-lookup"><span data-stu-id="7e4e0-108">The **Enable-AzOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="7e4e0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e4e0-109">EXAMPLES</span></span>

## <span data-ttu-id="7e4e0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e4e0-110">PARAMETERS</span></span>

### <span data-ttu-id="7e4e0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e4e0-111">-DefaultProfile</span></span>
<span data-ttu-id="7e4e0-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7e4e0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e4e0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e4e0-113">-ResourceGroupName</span></span>
<span data-ttu-id="7e4e0-114">Bilgisayarları içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e4e0-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="7e4e0-115">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="7e4e0-115">-Workspace</span></span>
<span data-ttu-id="7e4e0-116">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e4e0-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7e4e0-117">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="7e4e0-117">-WorkspaceName</span></span>
<span data-ttu-id="7e4e0-118">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e4e0-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7e4e0-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="7e4e0-119">-Confirm</span></span>
<span data-ttu-id="7e4e0-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7e4e0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e4e0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e4e0-121">-WhatIf</span></span>
<span data-ttu-id="7e4e0-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7e4e0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e4e0-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7e4e0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e4e0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e4e0-124">CommonParameters</span></span>
<span data-ttu-id="7e4e0-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e4e0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e4e0-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e4e0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e4e0-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e4e0-127">INPUTS</span></span>

### <span data-ttu-id="7e4e0-128">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="7e4e0-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="7e4e0-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7e4e0-129">System.String</span></span>

## <span data-ttu-id="7e4e0-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e4e0-130">OUTPUTS</span></span>

### <span data-ttu-id="7e4e0-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="7e4e0-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="7e4e0-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e4e0-132">NOTES</span></span>

## <span data-ttu-id="7e4e0-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e4e0-133">RELATED LINKS</span></span>

[<span data-ttu-id="7e4e0-134">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="7e4e0-134">Disable-AzOperationalInsightsIISLogCollection</span></span>](./Disable-AzOperationalInsightsIISLogCollection.md)

