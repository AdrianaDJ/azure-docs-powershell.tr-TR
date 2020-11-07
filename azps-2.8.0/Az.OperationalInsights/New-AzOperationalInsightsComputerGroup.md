---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscomputergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
ms.openlocfilehash: d1a1633303e30fc10c5eee7432101fa075f4d38f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932885"
---
# <span data-ttu-id="c615a-101">New-AzOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="c615a-101">New-AzOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="c615a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c615a-102">SYNOPSIS</span></span>
<span data-ttu-id="c615a-103">Bilgisayar grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c615a-103">Creates a computer group.</span></span>

## <span data-ttu-id="c615a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c615a-104">SYNTAX</span></span>

```
New-AzOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c615a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c615a-105">DESCRIPTION</span></span>
<span data-ttu-id="c615a-106">**New-Azoperationalınsightscomputergroup** cmdlet 'i bir kaynak grubunda ve konumda bir bilgisayar grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c615a-106">The **New-AzOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="c615a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c615a-107">EXAMPLES</span></span>

## <span data-ttu-id="c615a-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c615a-108">PARAMETERS</span></span>

### <span data-ttu-id="c615a-109">-Kategori</span><span class="sxs-lookup"><span data-stu-id="c615a-109">-Category</span></span>
<span data-ttu-id="c615a-110">Bilgisayar grubunun kategorisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c615a-110">Specifies the category of the computer group.</span></span>

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

### <span data-ttu-id="c615a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c615a-111">-DefaultProfile</span></span>
<span data-ttu-id="c615a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c615a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c615a-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c615a-113">-DisplayName</span></span>
<span data-ttu-id="c615a-114">Bilgisayar grubunun görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c615a-114">Specifies the display name of the computer group.</span></span>

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

### <span data-ttu-id="c615a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c615a-115">-Force</span></span>
<span data-ttu-id="c615a-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="c615a-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c615a-117">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="c615a-117">-Query</span></span>
<span data-ttu-id="c615a-118">Bilgisayar grubunun sorgusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c615a-118">Specifies the query of the computer group.</span></span>

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

### <span data-ttu-id="c615a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c615a-119">-ResourceGroupName</span></span>
<span data-ttu-id="c615a-120">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c615a-120">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c615a-121">Cmdlet, bu kaynak grubunda bilgisayar grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c615a-121">The cmdlet creates computer group in this resource group.</span></span>

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

### <span data-ttu-id="c615a-122">-Savedsearchıd</span><span class="sxs-lookup"><span data-stu-id="c615a-122">-SavedSearchId</span></span>
<span data-ttu-id="c615a-123">Bilgisayar grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c615a-123">Specifies the ID of the computer group.</span></span>

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

### <span data-ttu-id="c615a-124">-Version</span><span class="sxs-lookup"><span data-stu-id="c615a-124">-Version</span></span>
<span data-ttu-id="c615a-125">Sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c615a-125">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c615a-126">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="c615a-126">-WorkspaceName</span></span>
<span data-ttu-id="c615a-127">Çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c615a-127">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="c615a-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="c615a-128">-Confirm</span></span>
<span data-ttu-id="c615a-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c615a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c615a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c615a-130">-WhatIf</span></span>
<span data-ttu-id="c615a-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c615a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c615a-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c615a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c615a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c615a-133">CommonParameters</span></span>
<span data-ttu-id="c615a-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c615a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c615a-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c615a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c615a-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c615a-136">INPUTS</span></span>

### <span data-ttu-id="c615a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c615a-137">System.String</span></span>

### <span data-ttu-id="c615a-138">System. Int64</span><span class="sxs-lookup"><span data-stu-id="c615a-138">System.Int64</span></span>

## <span data-ttu-id="c615a-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c615a-139">OUTPUTS</span></span>

### <span data-ttu-id="c615a-140">Sistem .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="c615a-140">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="c615a-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c615a-141">NOTES</span></span>

## <span data-ttu-id="c615a-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c615a-142">RELATED LINKS</span></span>
