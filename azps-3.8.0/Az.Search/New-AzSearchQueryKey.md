---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
ms.openlocfilehash: e01e5e244bd34e3e18aa287e0f2f5709c5e208ec
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938111"
---
# <span data-ttu-id="f6d1f-101">New-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="f6d1f-101">New-AzSearchQueryKey</span></span>

## <span data-ttu-id="f6d1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6d1f-102">SYNOPSIS</span></span>
<span data-ttu-id="f6d1f-103">Azure Search hizmeti için yeni bir sorgu anahtarı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f6d1f-103">Create a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="f6d1f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f6d1f-104">SYNTAX</span></span>

### <span data-ttu-id="f6d1f-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f6d1f-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6d1f-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6d1f-106">ParentObjectParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6d1f-107">Parentresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="f6d1f-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6d1f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6d1f-108">DESCRIPTION</span></span>
<span data-ttu-id="f6d1f-109">**New-Azaramaquerykey** cmdlet 'ı Azure Search hizmeti için yeni bir sorgu anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f6d1f-109">The **New-AzSearchQueryKey** cmdlet creates a new query key for the Azure Search Service.</span></span>

## <span data-ttu-id="f6d1f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f6d1f-110">EXAMPLES</span></span>

### <span data-ttu-id="f6d1f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f6d1f-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="f6d1f-112">Örnek, Azure Search hizmeti için yeni bir sorgu anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f6d1f-112">The example creates a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="f6d1f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f6d1f-113">PARAMETERS</span></span>

### <span data-ttu-id="f6d1f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6d1f-114">-DefaultProfile</span></span>
<span data-ttu-id="f6d1f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f6d1f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6d1f-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="f6d1f-116">-Name</span></span>
<span data-ttu-id="f6d1f-117">Arama Hizmeti sorgu anahtarı adı.</span><span class="sxs-lookup"><span data-stu-id="f6d1f-117">Search Service query key name.</span></span>

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

### <span data-ttu-id="f6d1f-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f6d1f-118">-ParentObject</span></span>
<span data-ttu-id="f6d1f-119">Arama hizmeti giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f6d1f-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="f6d1f-120">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="f6d1f-120">-ParentResourceId</span></span>
<span data-ttu-id="f6d1f-121">Arama hizmeti kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="f6d1f-121">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="f6d1f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6d1f-122">-ResourceGroupName</span></span>
<span data-ttu-id="f6d1f-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f6d1f-123">Resource Group name.</span></span>

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

### <span data-ttu-id="f6d1f-124">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="f6d1f-124">-ServiceName</span></span>
<span data-ttu-id="f6d1f-125">Arama hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="f6d1f-125">Search Service name.</span></span>

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

### <span data-ttu-id="f6d1f-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="f6d1f-126">-Confirm</span></span>
<span data-ttu-id="f6d1f-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f6d1f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6d1f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6d1f-128">-WhatIf</span></span>
<span data-ttu-id="f6d1f-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6d1f-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6d1f-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f6d1f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6d1f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6d1f-131">CommonParameters</span></span>
<span data-ttu-id="f6d1f-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f6d1f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6d1f-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6d1f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6d1f-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f6d1f-134">INPUTS</span></span>

### <span data-ttu-id="f6d1f-135">Microsoft. Azure. Commands. Management. Search. model. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="f6d1f-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="f6d1f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f6d1f-136">System.String</span></span>

## <span data-ttu-id="f6d1f-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f6d1f-137">OUTPUTS</span></span>

### <span data-ttu-id="f6d1f-138">Microsoft. Azure. Commands. Management. Search. model. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="f6d1f-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="f6d1f-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f6d1f-139">NOTES</span></span>

## <span data-ttu-id="f6d1f-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f6d1f-140">RELATED LINKS</span></span>

[<span data-ttu-id="f6d1f-141">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="f6d1f-141">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)

[<span data-ttu-id="f6d1f-142">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="f6d1f-142">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)
