---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchQueryKey.md
ms.openlocfilehash: 3535e9d7723c87e0f528192e47c921d3835ff9e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588349"
---
# <span data-ttu-id="bda9b-101">Get-AzureRmSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="bda9b-101">Get-AzureRmSearchQueryKey</span></span>

## <span data-ttu-id="bda9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bda9b-102">SYNOPSIS</span></span>
<span data-ttu-id="bda9b-103">Azure Search hizmetinin sorgu anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="bda9b-103">Gets query key(s) of the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bda9b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bda9b-104">SYNTAX</span></span>

### <span data-ttu-id="bda9b-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bda9b-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bda9b-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bda9b-106">ParentObjectParameterSet</span></span>
```
Get-AzureRmSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bda9b-107">Parentresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="bda9b-107">ParentResourceIdParameterSet</span></span>
```
Get-AzureRmSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bda9b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bda9b-108">DESCRIPTION</span></span>
<span data-ttu-id="bda9b-109">**Get-AzureRmSearchQueryKey** cmdlet 'ı Azure Search hizmetinin sorgu anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="bda9b-109">The **Get-AzureRmSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="bda9b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bda9b-110">EXAMPLES</span></span>

### <span data-ttu-id="bda9b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bda9b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="bda9b-112">Örnekte, Azure Search hizmetinin tüm sorgu anahtarları alınır.</span><span class="sxs-lookup"><span data-stu-id="bda9b-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="bda9b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bda9b-113">PARAMETERS</span></span>

### <span data-ttu-id="bda9b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bda9b-114">-DefaultProfile</span></span>
<span data-ttu-id="bda9b-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bda9b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bda9b-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bda9b-116">-ParentObject</span></span>
<span data-ttu-id="bda9b-117">Arama hizmeti giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="bda9b-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="bda9b-118">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="bda9b-118">-ParentResourceId</span></span>
<span data-ttu-id="bda9b-119">Arama hizmeti kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="bda9b-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="bda9b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bda9b-120">-ResourceGroupName</span></span>
<span data-ttu-id="bda9b-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="bda9b-121">Resource Group name.</span></span>

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

### <span data-ttu-id="bda9b-122">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="bda9b-122">-ServiceName</span></span>
<span data-ttu-id="bda9b-123">Arama hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="bda9b-123">Search Service name.</span></span>

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

### <span data-ttu-id="bda9b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bda9b-124">CommonParameters</span></span>
<span data-ttu-id="bda9b-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bda9b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bda9b-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bda9b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bda9b-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bda9b-127">INPUTS</span></span>

### <span data-ttu-id="bda9b-128">Microsoft. Azure. Commands. Management. Search. model. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="bda9b-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="bda9b-129">Parametreler: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bda9b-129">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="bda9b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bda9b-130">System.String</span></span>

## <span data-ttu-id="bda9b-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bda9b-131">OUTPUTS</span></span>

### <span data-ttu-id="bda9b-132">Microsoft. Azure. Commands. Management. Search. model. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="bda9b-132">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="bda9b-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bda9b-133">NOTES</span></span>

## <span data-ttu-id="bda9b-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bda9b-134">RELATED LINKS</span></span>

[<span data-ttu-id="bda9b-135">New-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="bda9b-135">New-AzureRmSearchQueryKey.md</span></span>](./New-AzureRmSearchQueryKey.md)

[<span data-ttu-id="bda9b-136">Remove-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="bda9b-136">Remove-AzureRmSearchQueryKey.md</span></span>](./Remove-AzureRmSearchQueryKey.md)
