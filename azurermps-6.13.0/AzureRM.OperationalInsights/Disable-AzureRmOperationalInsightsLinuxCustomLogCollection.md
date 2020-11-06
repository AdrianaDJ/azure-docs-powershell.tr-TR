---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: EF3FE3F1-1C8F-41EB-990E-F2B30BD9D082
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/disable-azurermoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 2eecf19ad385729bfe0a140f234f2ddf5053e746
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588447"
---
# <span data-ttu-id="bd48b-101">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="bd48b-101">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="bd48b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd48b-102">SYNOPSIS</span></span>
<span data-ttu-id="bd48b-103">Linux bilgisayarlarından özel günlüklerin toplanmasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="bd48b-103">Stops collection of custom logs from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd48b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bd48b-104">SYNTAX</span></span>

### <span data-ttu-id="bd48b-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bd48b-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd48b-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="bd48b-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd48b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bd48b-107">DESCRIPTION</span></span>
<span data-ttu-id="bd48b-108">**Disable-Azurermoperationalınsightslinuxcustomlogcollection** cmdlet 'i, bir çalışma alanındaki bağlı Linux bilgisayarlarından özel günlüklerin toplanmasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="bd48b-108">The **Disable-AzureRmOperationalInsightsLinuxCustomLogCollection** cmdlet stops collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="bd48b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bd48b-109">EXAMPLES</span></span>

## <span data-ttu-id="bd48b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bd48b-110">PARAMETERS</span></span>

### <span data-ttu-id="bd48b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd48b-111">-DefaultProfile</span></span>
<span data-ttu-id="bd48b-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bd48b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd48b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd48b-113">-ResourceGroupName</span></span>
<span data-ttu-id="bd48b-114">Linux bilgisayarlarını içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd48b-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="bd48b-115">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="bd48b-115">-Workspace</span></span>
<span data-ttu-id="bd48b-116">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd48b-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="bd48b-117">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="bd48b-117">-WorkspaceName</span></span>
<span data-ttu-id="bd48b-118">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd48b-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="bd48b-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="bd48b-119">-Confirm</span></span>
<span data-ttu-id="bd48b-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bd48b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd48b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd48b-121">-WhatIf</span></span>
<span data-ttu-id="bd48b-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bd48b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd48b-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bd48b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd48b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd48b-124">CommonParameters</span></span>
<span data-ttu-id="bd48b-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bd48b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd48b-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd48b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd48b-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bd48b-127">INPUTS</span></span>

### <span data-ttu-id="bd48b-128">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="bd48b-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="bd48b-129">Parametreler: çalışma alanı (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bd48b-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="bd48b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bd48b-130">System.String</span></span>

## <span data-ttu-id="bd48b-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bd48b-131">OUTPUTS</span></span>

### <span data-ttu-id="bd48b-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="bd48b-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="bd48b-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bd48b-133">NOTES</span></span>
* <span data-ttu-id="bd48b-134">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, işletim, Öngörüler</span><span class="sxs-lookup"><span data-stu-id="bd48b-134">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="bd48b-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bd48b-135">RELATED LINKS</span></span>

[<span data-ttu-id="bd48b-136">Enable-Azurermoperationalınsightslinuxcustomlogcollection</span><span class="sxs-lookup"><span data-stu-id="bd48b-136">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)


