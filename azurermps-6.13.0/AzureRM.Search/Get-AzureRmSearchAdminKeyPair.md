---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchAdminKeyPair.md
ms.openlocfilehash: 92b2e7304c0f837e47f7464e84769478902c973a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591909"
---
# <span data-ttu-id="8d57a-101">Get-AzureRmSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="8d57a-101">Get-AzureRmSearchAdminKeyPair</span></span>

## <span data-ttu-id="8d57a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d57a-102">SYNOPSIS</span></span>
<span data-ttu-id="8d57a-103">Azure Search hizmetinin yönetici anahtarı çiftini alır.</span><span class="sxs-lookup"><span data-stu-id="8d57a-103">Gets admin key pair of the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d57a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8d57a-104">SYNTAX</span></span>

### <span data-ttu-id="8d57a-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8d57a-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d57a-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d57a-106">ParentObjectParameterSet</span></span>
```
Get-AzureRmSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8d57a-107">Parentresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="8d57a-107">ParentResourceIdParameterSet</span></span>
```
Get-AzureRmSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d57a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8d57a-108">DESCRIPTION</span></span>
<span data-ttu-id="8d57a-109">**Get-AzureRmSearchAdminKeyPair** cmdlet 'ı, Azure Search hizmetinin yönetici anahtarı çiftini alır.</span><span class="sxs-lookup"><span data-stu-id="8d57a-109">The **Get-AzureRmSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="8d57a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8d57a-110">EXAMPLES</span></span>

### <span data-ttu-id="8d57a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8d57a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="8d57a-112">Örnek, Azure Search hizmetinin yönetici anahtar çiftini alır.</span><span class="sxs-lookup"><span data-stu-id="8d57a-112">The example gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="8d57a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8d57a-113">PARAMETERS</span></span>

### <span data-ttu-id="8d57a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d57a-114">-DefaultProfile</span></span>
<span data-ttu-id="8d57a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8d57a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d57a-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8d57a-116">-ParentObject</span></span>
<span data-ttu-id="8d57a-117">Arama hizmeti giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8d57a-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="8d57a-118">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="8d57a-118">-ParentResourceId</span></span>
<span data-ttu-id="8d57a-119">Arama hizmeti kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="8d57a-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="8d57a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d57a-120">-ResourceGroupName</span></span>
<span data-ttu-id="8d57a-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8d57a-121">Resource Group name.</span></span>

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

### <span data-ttu-id="8d57a-122">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="8d57a-122">-ServiceName</span></span>
<span data-ttu-id="8d57a-123">Arama hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="8d57a-123">Search Service name.</span></span>

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

### <span data-ttu-id="8d57a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d57a-124">CommonParameters</span></span>
<span data-ttu-id="8d57a-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8d57a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d57a-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d57a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d57a-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8d57a-127">INPUTS</span></span>

### <span data-ttu-id="8d57a-128">Microsoft. Azure. Commands. Management. Search. model. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="8d57a-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="8d57a-129">Parametreler: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8d57a-129">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="8d57a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8d57a-130">System.String</span></span>

## <span data-ttu-id="8d57a-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8d57a-131">OUTPUTS</span></span>

### <span data-ttu-id="8d57a-132">Microsoft. Azure. Commands. Management. Search. model. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="8d57a-132">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="8d57a-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8d57a-133">NOTES</span></span>

## <span data-ttu-id="8d57a-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8d57a-134">RELATED LINKS</span></span>

[<span data-ttu-id="8d57a-135">New-AzureRmSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="8d57a-135">New-AzureRmSearchAdminKey</span></span>](./New-AzureRmSearchAdminKey.md)
