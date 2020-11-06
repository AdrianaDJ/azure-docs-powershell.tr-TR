---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 10141D75-B58D-42B0-B0A6-92FF630E534C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 1ef047fa821a2eb74f0c06f82b42f51a1197dfc5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593050"
---
# <span data-ttu-id="e0b44-101">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="e0b44-101">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="e0b44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0b44-102">SYNOPSIS</span></span>
<span data-ttu-id="e0b44-103">Linux bilgisayarlarından performans sayaçları toplamayı başlatır.</span><span class="sxs-lookup"><span data-stu-id="e0b44-103">Starts collection of performance counters from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0b44-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0b44-104">SYNTAX</span></span>

### <span data-ttu-id="e0b44-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e0b44-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0b44-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="e0b44-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0b44-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0b44-107">DESCRIPTION</span></span>
<span data-ttu-id="e0b44-108">**Enable-Azurermoperationalınsightslinuxperformance cecollection** cmdlet 'i, bir çalışma alanındaki bağlı Linux bilgisayarlarından performans sayaçlarının toplanmasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="e0b44-108">The **Enable-AzureRmOperationalInsightsLinuxPerformanceCollection** cmdlet starts collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="e0b44-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0b44-109">EXAMPLES</span></span>

## <span data-ttu-id="e0b44-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0b44-110">PARAMETERS</span></span>

### <span data-ttu-id="e0b44-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0b44-111">-ResourceGroupName</span></span>
<span data-ttu-id="e0b44-112">Linux bilgisayarlarını içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0b44-112">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="e0b44-113">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="e0b44-113">-Workspace</span></span>
<span data-ttu-id="e0b44-114">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0b44-114">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e0b44-115">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="e0b44-115">-WorkspaceName</span></span>
<span data-ttu-id="e0b44-116">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0b44-116">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e0b44-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="e0b44-117">-Confirm</span></span>
<span data-ttu-id="e0b44-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e0b44-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0b44-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0b44-119">-WhatIf</span></span>
<span data-ttu-id="e0b44-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e0b44-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0b44-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e0b44-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0b44-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0b44-122">-DefaultProfile</span></span>
<span data-ttu-id="e0b44-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e0b44-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0b44-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0b44-124">CommonParameters</span></span>
<span data-ttu-id="e0b44-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0b44-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0b44-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0b44-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0b44-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0b44-127">INPUTS</span></span>

### <span data-ttu-id="e0b44-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e0b44-128">PSWorkspace</span></span>
<span data-ttu-id="e0b44-129">Parametre ' çalışma alanı ', ardışık düzenin ' PSWorkspace ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="e0b44-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="e0b44-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0b44-130">OUTPUTS</span></span>

### <span data-ttu-id="e0b44-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="e0b44-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="e0b44-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0b44-132">NOTES</span></span>
* <span data-ttu-id="e0b44-133">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, işletim, Öngörüler</span><span class="sxs-lookup"><span data-stu-id="e0b44-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="e0b44-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0b44-134">RELATED LINKS</span></span>

[<span data-ttu-id="e0b44-135">Disable-Azurermoperationalınsightslinuxperformancecollection</span><span class="sxs-lookup"><span data-stu-id="e0b44-135">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)


