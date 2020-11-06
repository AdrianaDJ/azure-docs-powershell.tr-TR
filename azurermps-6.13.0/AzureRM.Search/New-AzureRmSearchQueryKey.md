---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/new-azurermsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchQueryKey.md
ms.openlocfilehash: 417e1a546777824df86b72f3740079ac91835192
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592264"
---
# <span data-ttu-id="acc98-101">New-AzureRmSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="acc98-101">New-AzureRmSearchQueryKey</span></span>

## <span data-ttu-id="acc98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acc98-102">SYNOPSIS</span></span>
<span data-ttu-id="acc98-103">Azure Search hizmeti için yeni bir sorgu anahtarı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="acc98-103">Create a new query key for the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acc98-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="acc98-104">SYNTAX</span></span>

### <span data-ttu-id="acc98-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="acc98-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzureRmSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acc98-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="acc98-106">ParentObjectParameterSet</span></span>
```
New-AzureRmSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acc98-107">Parentresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="acc98-107">ParentResourceIdParameterSet</span></span>
```
New-AzureRmSearchQueryKey [-ParentResourceId] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acc98-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="acc98-108">DESCRIPTION</span></span>
<span data-ttu-id="acc98-109">**New-AzureRmSearchQueryKey** cmdlet 'ı Azure Search hizmeti için yeni bir sorgu anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="acc98-109">The **New-AzureRmSearchQueryKey** cmdlet creates a new query key for the Azure Search Service.</span></span>

## <span data-ttu-id="acc98-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="acc98-110">EXAMPLES</span></span>

### <span data-ttu-id="acc98-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="acc98-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="acc98-112">Örnek, Azure Search hizmeti için yeni bir sorgu anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="acc98-112">The example creates a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="acc98-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="acc98-113">PARAMETERS</span></span>

### <span data-ttu-id="acc98-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc98-114">-DefaultProfile</span></span>
<span data-ttu-id="acc98-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="acc98-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acc98-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="acc98-116">-Name</span></span>
<span data-ttu-id="acc98-117">Arama Hizmeti sorgu anahtarı adı.</span><span class="sxs-lookup"><span data-stu-id="acc98-117">Search Service query key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acc98-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="acc98-118">-ParentObject</span></span>
<span data-ttu-id="acc98-119">Arama hizmeti giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="acc98-119">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acc98-120">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="acc98-120">-ParentResourceId</span></span>
<span data-ttu-id="acc98-121">Arama hizmeti kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="acc98-121">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acc98-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acc98-122">-ResourceGroupName</span></span>
<span data-ttu-id="acc98-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="acc98-123">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acc98-124">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="acc98-124">-ServiceName</span></span>
<span data-ttu-id="acc98-125">Arama hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="acc98-125">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acc98-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="acc98-126">-Confirm</span></span>
<span data-ttu-id="acc98-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="acc98-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acc98-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acc98-128">-WhatIf</span></span>
<span data-ttu-id="acc98-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="acc98-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="acc98-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="acc98-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acc98-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc98-131">CommonParameters</span></span>
<span data-ttu-id="acc98-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="acc98-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc98-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acc98-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc98-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="acc98-134">INPUTS</span></span>

### <span data-ttu-id="acc98-135">Microsoft. Azure. Commands. Management. Search. model. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="acc98-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="acc98-136">Parametreler: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="acc98-136">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="acc98-137">System. String</span><span class="sxs-lookup"><span data-stu-id="acc98-137">System.String</span></span>

## <span data-ttu-id="acc98-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="acc98-138">OUTPUTS</span></span>

### <span data-ttu-id="acc98-139">Microsoft. Azure. Commands. Management. Search. model. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="acc98-139">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="acc98-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="acc98-140">NOTES</span></span>

## <span data-ttu-id="acc98-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="acc98-141">RELATED LINKS</span></span>

[<span data-ttu-id="acc98-142">Get-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="acc98-142">Get-AzureRmSearchQueryKey.md</span></span>](./Get-AzureRmSearchQueryKey.md)

[<span data-ttu-id="acc98-143">Remove-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="acc98-143">Remove-AzureRmSearchQueryKey.md</span></span>](./Remove-AzureRmSearchQueryKey.md)
