---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightscomputergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
ms.openlocfilehash: 999e9e5fd9f0b93e71b222f228b1575e0492073d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593716"
---
# <span data-ttu-id="83552-101">New-AzureRmOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="83552-101">New-AzureRmOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="83552-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83552-102">SYNOPSIS</span></span>
<span data-ttu-id="83552-103">Bilgisayar grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="83552-103">Creates a computer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83552-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="83552-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83552-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="83552-105">DESCRIPTION</span></span>
<span data-ttu-id="83552-106">**Yeni-Azurermoperationalınsightscomputergroup** cmdlet 'i bir kaynak grubunda ve konumda bir bilgisayar grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="83552-106">The **New-AzureRmOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="83552-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="83552-107">EXAMPLES</span></span>

## <span data-ttu-id="83552-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="83552-108">PARAMETERS</span></span>

### <span data-ttu-id="83552-109">-Kategori</span><span class="sxs-lookup"><span data-stu-id="83552-109">-Category</span></span>
<span data-ttu-id="83552-110">Bilgisayar grubunun kategorisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="83552-110">Specifies the category of the computer group.</span></span>

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

### <span data-ttu-id="83552-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83552-111">-DefaultProfile</span></span>
<span data-ttu-id="83552-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="83552-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83552-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="83552-113">-DisplayName</span></span>
<span data-ttu-id="83552-114">Bilgisayar grubunun görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="83552-114">Specifies the display name of the computer group.</span></span>

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

### <span data-ttu-id="83552-115">-Force</span><span class="sxs-lookup"><span data-stu-id="83552-115">-Force</span></span>
<span data-ttu-id="83552-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="83552-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="83552-117">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="83552-117">-Query</span></span>
<span data-ttu-id="83552-118">Bilgisayar grubunun sorgusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="83552-118">Specifies the query of the computer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83552-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83552-119">-ResourceGroupName</span></span>
<span data-ttu-id="83552-120">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="83552-120">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="83552-121">Cmdlet, bu kaynak grubunda bilgisayar grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="83552-121">The cmdlet creates computer group in this resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83552-122">-Savedsearchıd</span><span class="sxs-lookup"><span data-stu-id="83552-122">-SavedSearchId</span></span>
<span data-ttu-id="83552-123">Bilgisayar grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="83552-123">Specifies the ID of the computer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83552-124">-Version</span><span class="sxs-lookup"><span data-stu-id="83552-124">-Version</span></span>
<span data-ttu-id="83552-125">Sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="83552-125">Specifies the version.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83552-126">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="83552-126">-WorkspaceName</span></span>
<span data-ttu-id="83552-127">Çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="83552-127">Specifies the name of the workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83552-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="83552-128">-Confirm</span></span>
<span data-ttu-id="83552-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="83552-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83552-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83552-130">-WhatIf</span></span>
<span data-ttu-id="83552-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="83552-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83552-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="83552-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83552-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83552-133">CommonParameters</span></span>
<span data-ttu-id="83552-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="83552-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83552-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83552-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83552-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="83552-136">INPUTS</span></span>

### <span data-ttu-id="83552-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="83552-137">None</span></span>
<span data-ttu-id="83552-138">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="83552-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="83552-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="83552-139">OUTPUTS</span></span>

## <span data-ttu-id="83552-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="83552-140">NOTES</span></span>

## <span data-ttu-id="83552-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="83552-141">RELATED LINKS</span></span>

