---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: a0dddf6e7cc5080ca4028b1348381c1b5fb72df6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279151"
---
# <span data-ttu-id="9c5cb-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="9c5cb-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="9c5cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c5cb-102">SYNOPSIS</span></span>
<span data-ttu-id="9c5cb-103">Azure Search hizmetinin sorgu anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="9c5cb-103">Gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="9c5cb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9c5cb-104">SYNTAX</span></span>

### <span data-ttu-id="9c5cb-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9c5cb-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c5cb-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c5cb-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c5cb-107">Parentresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="9c5cb-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c5cb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9c5cb-108">DESCRIPTION</span></span>
<span data-ttu-id="9c5cb-109">**Get-Azaramaquerykey** cmdlet 'ı Azure Search hizmetinin sorgu anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="9c5cb-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="9c5cb-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9c5cb-110">EXAMPLES</span></span>

### <span data-ttu-id="9c5cb-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9c5cb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="9c5cb-112">Örnekte, Azure Search hizmetinin tüm sorgu anahtarları alınır.</span><span class="sxs-lookup"><span data-stu-id="9c5cb-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="9c5cb-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9c5cb-113">PARAMETERS</span></span>

### <span data-ttu-id="9c5cb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c5cb-114">-DefaultProfile</span></span>
<span data-ttu-id="9c5cb-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9c5cb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c5cb-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9c5cb-116">-ParentObject</span></span>
<span data-ttu-id="9c5cb-117">Arama hizmeti giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9c5cb-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="9c5cb-118">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="9c5cb-118">-ParentResourceId</span></span>
<span data-ttu-id="9c5cb-119">Arama hizmeti kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="9c5cb-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="9c5cb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c5cb-120">-ResourceGroupName</span></span>
<span data-ttu-id="9c5cb-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9c5cb-121">Resource Group name.</span></span>

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

### <span data-ttu-id="9c5cb-122">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="9c5cb-122">-ServiceName</span></span>
<span data-ttu-id="9c5cb-123">Arama hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="9c5cb-123">Search Service name.</span></span>

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

### <span data-ttu-id="9c5cb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c5cb-124">CommonParameters</span></span>
<span data-ttu-id="9c5cb-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9c5cb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c5cb-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c5cb-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c5cb-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9c5cb-127">INPUTS</span></span>

### <span data-ttu-id="9c5cb-128">Microsoft. Azure. Commands. Management. Search. model. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="9c5cb-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="9c5cb-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9c5cb-129">System.String</span></span>

## <span data-ttu-id="9c5cb-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9c5cb-130">OUTPUTS</span></span>

### <span data-ttu-id="9c5cb-131">Microsoft. Azure. Commands. Management. Search. model. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="9c5cb-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="9c5cb-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9c5cb-132">NOTES</span></span>

## <span data-ttu-id="9c5cb-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9c5cb-133">RELATED LINKS</span></span>

[<span data-ttu-id="9c5cb-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="9c5cb-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="9c5cb-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="9c5cb-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)