---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightscomputergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
ms.openlocfilehash: 60c1db3595c3ca33676fbd874356376981a72407
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588430"
---
# <span data-ttu-id="8022c-101">New-AzureRmOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="8022c-101">New-AzureRmOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="8022c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8022c-102">SYNOPSIS</span></span>
<span data-ttu-id="8022c-103">Bilgisayar grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8022c-103">Creates a computer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8022c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8022c-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8022c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8022c-105">DESCRIPTION</span></span>
<span data-ttu-id="8022c-106">**Yeni-Azurermoperationalınsightscomputergroup** cmdlet 'i bir kaynak grubunda ve konumda bir bilgisayar grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8022c-106">The **New-AzureRmOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="8022c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8022c-107">EXAMPLES</span></span>

## <span data-ttu-id="8022c-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8022c-108">PARAMETERS</span></span>

### <span data-ttu-id="8022c-109">-Kategori</span><span class="sxs-lookup"><span data-stu-id="8022c-109">-Category</span></span>
<span data-ttu-id="8022c-110">Bilgisayar grubunun kategorisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8022c-110">Specifies the category of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8022c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8022c-111">-DefaultProfile</span></span>
<span data-ttu-id="8022c-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8022c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8022c-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8022c-113">-DisplayName</span></span>
<span data-ttu-id="8022c-114">Bilgisayar grubunun görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8022c-114">Specifies the display name of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8022c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8022c-115">-Force</span></span>
<span data-ttu-id="8022c-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="8022c-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8022c-117">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="8022c-117">-Query</span></span>
<span data-ttu-id="8022c-118">Bilgisayar grubunun sorgusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8022c-118">Specifies the query of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8022c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8022c-119">-ResourceGroupName</span></span>
<span data-ttu-id="8022c-120">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8022c-120">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8022c-121">Cmdlet, bu kaynak grubunda bilgisayar grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8022c-121">The cmdlet creates computer group in this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8022c-122">-Savedsearchıd</span><span class="sxs-lookup"><span data-stu-id="8022c-122">-SavedSearchId</span></span>
<span data-ttu-id="8022c-123">Bilgisayar grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8022c-123">Specifies the ID of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8022c-124">-Version</span><span class="sxs-lookup"><span data-stu-id="8022c-124">-Version</span></span>
<span data-ttu-id="8022c-125">Sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8022c-125">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8022c-126">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="8022c-126">-WorkspaceName</span></span>
<span data-ttu-id="8022c-127">Çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8022c-127">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8022c-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="8022c-128">-Confirm</span></span>
<span data-ttu-id="8022c-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8022c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8022c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8022c-130">-WhatIf</span></span>
<span data-ttu-id="8022c-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8022c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8022c-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8022c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8022c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8022c-133">CommonParameters</span></span>
<span data-ttu-id="8022c-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8022c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8022c-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8022c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8022c-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8022c-136">INPUTS</span></span>

### <span data-ttu-id="8022c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8022c-137">System.String</span></span>

### <span data-ttu-id="8022c-138">System. Int64</span><span class="sxs-lookup"><span data-stu-id="8022c-138">System.Int64</span></span>

## <span data-ttu-id="8022c-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8022c-139">OUTPUTS</span></span>

### <span data-ttu-id="8022c-140">Sistem .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="8022c-140">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="8022c-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8022c-141">NOTES</span></span>

## <span data-ttu-id="8022c-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8022c-142">RELATED LINKS</span></span>
