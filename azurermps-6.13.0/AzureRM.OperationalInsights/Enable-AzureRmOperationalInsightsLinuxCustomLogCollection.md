---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 99865242-6623-425E-92F2-0B229FC4EDAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/enable-azurermoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 2b6bc41feb283e4a9f4be18f65c9a5be127598e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588443"
---
# <span data-ttu-id="7e9b2-101">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="7e9b2-101">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="7e9b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e9b2-102">SYNOPSIS</span></span>
<span data-ttu-id="7e9b2-103">Linux bilgisayarlardan özel günlükleri koleksiyonunu başlatır.</span><span class="sxs-lookup"><span data-stu-id="7e9b2-103">Starts collection of custom logs from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e9b2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e9b2-104">SYNTAX</span></span>

### <span data-ttu-id="7e9b2-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7e9b2-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e9b2-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="7e9b2-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e9b2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e9b2-107">DESCRIPTION</span></span>
<span data-ttu-id="7e9b2-108">**Enable-Azurermoperationalınsightslinuxcustomlogcollection** cmdlet 'i, bir çalışma alanındaki bağlı Linux bilgisayarlarından özel Günlükler koleksiyonunu başlatır.</span><span class="sxs-lookup"><span data-stu-id="7e9b2-108">The **Enable-AzureRmOperationalInsightsLinuxCustomLogCollection** cmdlet starts collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="7e9b2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e9b2-109">EXAMPLES</span></span>

## <span data-ttu-id="7e9b2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e9b2-110">PARAMETERS</span></span>

### <span data-ttu-id="7e9b2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e9b2-111">-DefaultProfile</span></span>
<span data-ttu-id="7e9b2-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7e9b2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e9b2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e9b2-113">-ResourceGroupName</span></span>
<span data-ttu-id="7e9b2-114">Linux bilgisayarlarını içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e9b2-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="7e9b2-115">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="7e9b2-115">-Workspace</span></span>
<span data-ttu-id="7e9b2-116">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e9b2-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7e9b2-117">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="7e9b2-117">-WorkspaceName</span></span>
<span data-ttu-id="7e9b2-118">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e9b2-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7e9b2-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="7e9b2-119">-Confirm</span></span>
<span data-ttu-id="7e9b2-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7e9b2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e9b2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e9b2-121">-WhatIf</span></span>
<span data-ttu-id="7e9b2-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7e9b2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e9b2-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7e9b2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e9b2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e9b2-124">CommonParameters</span></span>
<span data-ttu-id="7e9b2-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e9b2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e9b2-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e9b2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e9b2-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e9b2-127">INPUTS</span></span>

### <span data-ttu-id="7e9b2-128">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="7e9b2-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="7e9b2-129">Parametreler: çalışma alanı (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7e9b2-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="7e9b2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7e9b2-130">System.String</span></span>

## <span data-ttu-id="7e9b2-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e9b2-131">OUTPUTS</span></span>

### <span data-ttu-id="7e9b2-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="7e9b2-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="7e9b2-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e9b2-133">NOTES</span></span>
* <span data-ttu-id="7e9b2-134">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, işletim, Öngörüler</span><span class="sxs-lookup"><span data-stu-id="7e9b2-134">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="7e9b2-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e9b2-135">RELATED LINKS</span></span>

[<span data-ttu-id="7e9b2-136">Disable-Azurermoperationalınsightslinuxcustomlogcollection</span><span class="sxs-lookup"><span data-stu-id="7e9b2-136">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)


