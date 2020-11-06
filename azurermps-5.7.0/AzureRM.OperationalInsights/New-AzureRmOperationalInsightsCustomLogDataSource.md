---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: 510148c5d700c1378b0e468bbd5e8a9206491284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594907"
---
# <span data-ttu-id="27956-101">New-AzureRmOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="27956-101">New-AzureRmOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="27956-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27956-102">SYNOPSIS</span></span>
<span data-ttu-id="27956-103">Özel günlük koleksiyonu ilkesi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="27956-103">Defines a custom log collection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27956-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="27956-104">SYNTAX</span></span>

### <span data-ttu-id="27956-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="27956-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27956-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="27956-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="27956-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="27956-107">DESCRIPTION</span></span>
<span data-ttu-id="27956-108">**Yeni-Azurermoperationalınsightsccustomlogdatasource** cmdlet 'i özel günlük koleksiyonu ilkesi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="27956-108">The **New-AzureRmOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="27956-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="27956-109">EXAMPLES</span></span>

## <span data-ttu-id="27956-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="27956-110">PARAMETERS</span></span>

### <span data-ttu-id="27956-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="27956-111">-CustomLogRawJson</span></span>
<span data-ttu-id="27956-112">Özel koleksiyon ilkesini ham JavaScript nesne gösterimi (JSON) dizesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="27956-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27956-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27956-113">-DefaultProfile</span></span>
<span data-ttu-id="27956-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="27956-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27956-115">-Force</span><span class="sxs-lookup"><span data-stu-id="27956-115">-Force</span></span>
<span data-ttu-id="27956-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="27956-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27956-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="27956-117">-Name</span></span>
<span data-ttu-id="27956-118">Veri kaynağı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="27956-118">Specifies a name for the data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27956-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27956-119">-ResourceGroupName</span></span>
<span data-ttu-id="27956-120">Bilgisayarları içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27956-120">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="27956-121">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="27956-121">-Workspace</span></span>
<span data-ttu-id="27956-122">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27956-122">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="27956-123">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="27956-123">-WorkspaceName</span></span>
<span data-ttu-id="27956-124">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27956-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="27956-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="27956-125">-Confirm</span></span>
<span data-ttu-id="27956-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="27956-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27956-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27956-127">-WhatIf</span></span>
<span data-ttu-id="27956-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="27956-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27956-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="27956-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27956-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27956-130">CommonParameters</span></span>
<span data-ttu-id="27956-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="27956-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27956-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27956-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27956-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="27956-133">INPUTS</span></span>

### <span data-ttu-id="27956-134">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="27956-134">PSWorkspace</span></span>
<span data-ttu-id="27956-135">Parametre ' çalışma alanı ', ardışık düzenin ' PSWorkspace ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="27956-135">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="27956-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="27956-136">OUTPUTS</span></span>

### <span data-ttu-id="27956-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="27956-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="27956-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="27956-138">NOTES</span></span>

## <span data-ttu-id="27956-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="27956-139">RELATED LINKS</span></span>

[<span data-ttu-id="27956-140">Disable-Azurermoperationalınsightslinuxcustomlogcollection</span><span class="sxs-lookup"><span data-stu-id="27956-140">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="27956-141">Enable-Azurermoperationalınsightslinuxcustomlogcollection</span><span class="sxs-lookup"><span data-stu-id="27956-141">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)


