---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/enable-azurermoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 417bc080d707c3da02dd8a0083fb707f79d0a999
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590376"
---
# <span data-ttu-id="1b873-101">Enable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="1b873-101">Enable-AzureRmOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="1b873-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b873-102">SYNOPSIS</span></span>
<span data-ttu-id="1b873-103">Bir çalışma alanındaki bilgisayarlardan IIS günlükleri koleksiyonunu başlatır.</span><span class="sxs-lookup"><span data-stu-id="1b873-103">Starts collection of IIS logs from computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b873-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b873-104">SYNTAX</span></span>

### <span data-ttu-id="1b873-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1b873-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b873-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="1b873-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b873-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b873-107">DESCRIPTION</span></span>
<span data-ttu-id="1b873-108">**Enable-AzureRmOperationalInsightsIISLogCollection** cmdlet 'i, bir çalışma alanındaki bağlı bilgisayarlardan Internet Information SERVICES (IIS) günlüklerini başlatır.</span><span class="sxs-lookup"><span data-stu-id="1b873-108">The **Enable-AzureRmOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="1b873-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b873-109">EXAMPLES</span></span>

## <span data-ttu-id="1b873-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b873-110">PARAMETERS</span></span>

### <span data-ttu-id="1b873-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b873-111">-DefaultProfile</span></span>
<span data-ttu-id="1b873-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1b873-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b873-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b873-113">-ResourceGroupName</span></span>
<span data-ttu-id="1b873-114">Bilgisayarları içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b873-114">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b873-115">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="1b873-115">-Workspace</span></span>
<span data-ttu-id="1b873-116">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b873-116">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b873-117">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="1b873-117">-WorkspaceName</span></span>
<span data-ttu-id="1b873-118">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b873-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b873-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="1b873-119">-Confirm</span></span>
<span data-ttu-id="1b873-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1b873-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b873-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b873-121">-WhatIf</span></span>
<span data-ttu-id="1b873-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1b873-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b873-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1b873-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b873-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b873-124">CommonParameters</span></span>
<span data-ttu-id="1b873-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b873-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b873-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b873-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b873-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b873-127">INPUTS</span></span>

### <span data-ttu-id="1b873-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1b873-128">PSWorkspace</span></span>
<span data-ttu-id="1b873-129">Parametre ' çalışma alanı ', ardışık düzenin ' PSWorkspace ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="1b873-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="1b873-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b873-130">OUTPUTS</span></span>

### <span data-ttu-id="1b873-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="1b873-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="1b873-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b873-132">NOTES</span></span>

## <span data-ttu-id="1b873-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b873-133">RELATED LINKS</span></span>

[<span data-ttu-id="1b873-134">Disable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="1b873-134">Disable-AzureRmOperationalInsightsIISLogCollection</span></span>](./Disable-AzureRmOperationalInsightsIISLogCollection.md)


