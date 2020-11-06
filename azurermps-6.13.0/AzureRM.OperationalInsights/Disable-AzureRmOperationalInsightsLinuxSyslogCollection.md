---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 4A91EEDA-D8F0-4109-A32E-B83694952C06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/disable-azurermoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: 3fdd6b407753e8edd9ba7faa074e287062f15fb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588446"
---
# <span data-ttu-id="5211c-101">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="5211c-101">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="5211c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5211c-102">SYNOPSIS</span></span>
<span data-ttu-id="5211c-103">Linux bilgisayarlarından Syslog verileri koleksiyonunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="5211c-103">Stops collection of syslog data from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5211c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5211c-104">SYNTAX</span></span>

### <span data-ttu-id="5211c-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5211c-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5211c-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="5211c-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5211c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5211c-107">DESCRIPTION</span></span>
<span data-ttu-id="5211c-108">**Disable-Azurermoperationalınsightslinuxsyslogcollection** cmdlet 'i, bir çalışma alanındaki bağlı Linux bilgisayarlarından Syslog verileri derlemesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="5211c-108">The **Disable-AzureRmOperationalInsightsLinuxSyslogCollection** cmdlet stops collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="5211c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5211c-109">EXAMPLES</span></span>

## <span data-ttu-id="5211c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5211c-110">PARAMETERS</span></span>

### <span data-ttu-id="5211c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5211c-111">-DefaultProfile</span></span>
<span data-ttu-id="5211c-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5211c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5211c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5211c-113">-ResourceGroupName</span></span>
<span data-ttu-id="5211c-114">Linux bilgisayarlarını içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5211c-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="5211c-115">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="5211c-115">-Workspace</span></span>
<span data-ttu-id="5211c-116">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5211c-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5211c-117">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="5211c-117">-WorkspaceName</span></span>
<span data-ttu-id="5211c-118">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5211c-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5211c-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="5211c-119">-Confirm</span></span>
<span data-ttu-id="5211c-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5211c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5211c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5211c-121">-WhatIf</span></span>
<span data-ttu-id="5211c-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5211c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5211c-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5211c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5211c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5211c-124">CommonParameters</span></span>
<span data-ttu-id="5211c-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5211c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5211c-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5211c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5211c-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5211c-127">INPUTS</span></span>

### <span data-ttu-id="5211c-128">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="5211c-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="5211c-129">Parametreler: çalışma alanı (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5211c-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="5211c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5211c-130">System.String</span></span>

## <span data-ttu-id="5211c-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5211c-131">OUTPUTS</span></span>

### <span data-ttu-id="5211c-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="5211c-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="5211c-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5211c-133">NOTES</span></span>
* <span data-ttu-id="5211c-134">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, işletim, Öngörüler</span><span class="sxs-lookup"><span data-stu-id="5211c-134">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="5211c-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5211c-135">RELATED LINKS</span></span>

[<span data-ttu-id="5211c-136">Enable-Azurermoperationalınsightslinuxsyslogcollection</span><span class="sxs-lookup"><span data-stu-id="5211c-136">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="5211c-137">Yeni-Azurermoperationalınsightslinuxsyslogdatasource</span><span class="sxs-lookup"><span data-stu-id="5211c-137">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzureRmOperationalInsightsLinuxSyslogDataSource.md)


