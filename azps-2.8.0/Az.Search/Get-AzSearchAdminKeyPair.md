---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
ms.openlocfilehash: cd944184f4691b3f88934afc3a7bd9132eb23fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932527"
---
# <span data-ttu-id="5b349-101">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="5b349-101">Get-AzSearchAdminKeyPair</span></span>

## <span data-ttu-id="5b349-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b349-102">SYNOPSIS</span></span>
<span data-ttu-id="5b349-103">Azure Search hizmetinin yönetici anahtarı çiftini alır.</span><span class="sxs-lookup"><span data-stu-id="5b349-103">Gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="5b349-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5b349-104">SYNTAX</span></span>

### <span data-ttu-id="5b349-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5b349-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b349-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b349-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b349-107">Parentresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="5b349-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b349-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5b349-108">DESCRIPTION</span></span>
<span data-ttu-id="5b349-109">**Get-AzSearchAdminKeyPair** cmdlet 'ı, Azure Search hizmetinin yönetici anahtarı çiftini alır.</span><span class="sxs-lookup"><span data-stu-id="5b349-109">The **Get-AzSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="5b349-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5b349-110">EXAMPLES</span></span>

### <span data-ttu-id="5b349-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5b349-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="5b349-112">Örnek, Azure Search hizmetinin yönetici anahtar çiftini alır.</span><span class="sxs-lookup"><span data-stu-id="5b349-112">The example gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="5b349-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5b349-113">PARAMETERS</span></span>

### <span data-ttu-id="5b349-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b349-114">-DefaultProfile</span></span>
<span data-ttu-id="5b349-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5b349-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b349-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5b349-116">-ParentObject</span></span>
<span data-ttu-id="5b349-117">Arama hizmeti giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="5b349-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="5b349-118">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="5b349-118">-ParentResourceId</span></span>
<span data-ttu-id="5b349-119">Arama hizmeti kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="5b349-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="5b349-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b349-120">-ResourceGroupName</span></span>
<span data-ttu-id="5b349-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5b349-121">Resource Group name.</span></span>

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

### <span data-ttu-id="5b349-122">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="5b349-122">-ServiceName</span></span>
<span data-ttu-id="5b349-123">Arama hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="5b349-123">Search Service name.</span></span>

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

### <span data-ttu-id="5b349-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b349-124">CommonParameters</span></span>
<span data-ttu-id="5b349-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5b349-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b349-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b349-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b349-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5b349-127">INPUTS</span></span>

### <span data-ttu-id="5b349-128">Microsoft. Azure. Commands. Management. Search. model. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="5b349-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="5b349-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5b349-129">System.String</span></span>

## <span data-ttu-id="5b349-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5b349-130">OUTPUTS</span></span>

### <span data-ttu-id="5b349-131">Microsoft. Azure. Commands. Management. Search. model. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="5b349-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="5b349-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5b349-132">NOTES</span></span>

## <span data-ttu-id="5b349-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5b349-133">RELATED LINKS</span></span>

[<span data-ttu-id="5b349-134">Yeni-Azaramaadminkey</span><span class="sxs-lookup"><span data-stu-id="5b349-134">New-AzSearchAdminKey</span></span>](./New-AzSearchAdminKey.md)