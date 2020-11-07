---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/new-azurermsearchadminkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchAdminKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchAdminKey.md
ms.openlocfilehash: fa7ea6f1e53b94a349d51856432f1c01b2e89ba0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763131"
---
# <span data-ttu-id="60f05-101">New-AzureRmSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="60f05-101">New-AzureRmSearchAdminKey</span></span>

## <span data-ttu-id="60f05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60f05-102">SYNOPSIS</span></span>
<span data-ttu-id="60f05-103">Azure Search hizmetinin yönetim anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="60f05-103">Regenerates an admin key of the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60f05-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="60f05-104">SYNTAX</span></span>

### <span data-ttu-id="60f05-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="60f05-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzureRmSearchAdminKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyKind <PSSearchAdminKeyKind>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60f05-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60f05-106">ParentObjectParameterSet</span></span>
```
New-AzureRmSearchAdminKey [-ParentObject] <PSSearchService> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60f05-107">Parentresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="60f05-107">ParentResourceIdParameterSet</span></span>
```
New-AzureRmSearchAdminKey [-ParentResourceId] <String> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60f05-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="60f05-108">DESCRIPTION</span></span>
<span data-ttu-id="60f05-109">**New-AzureRmSearchAdminKey** cmdlet 'ı Azure Search hizmetinin yönetim anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="60f05-109">The **New-AzureRmSearchAdminKey** cmdlet regenerates an admin key of the Azure Search service.</span></span>

## <span data-ttu-id="60f05-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="60f05-110">EXAMPLES</span></span>

### <span data-ttu-id="60f05-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="60f05-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSearchAdminKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyKind Primary

Confirm
Are you sure you want to regenerate 'Primary' key for Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

Primary                          Secondary
-------                          ---------
85B3813D11904B591BE8A196C2C743A1 CEF791D5BAC2E6C0B232C56702F21E87
```

<span data-ttu-id="60f05-112">Örnek Azure Search hizmetinin birincil anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="60f05-112">The example regenerates Primary key of the Azure Search Service.</span></span>

## <span data-ttu-id="60f05-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="60f05-113">PARAMETERS</span></span>

### <span data-ttu-id="60f05-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60f05-114">-DefaultProfile</span></span>
<span data-ttu-id="60f05-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="60f05-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60f05-116">-Force</span><span class="sxs-lookup"><span data-stu-id="60f05-116">-Force</span></span>
<span data-ttu-id="60f05-117">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="60f05-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="60f05-118">-KeyKind</span><span class="sxs-lookup"><span data-stu-id="60f05-118">-KeyKind</span></span>
<span data-ttu-id="60f05-119">Arama Hizmeti Yöneticisi anahtar türü (birincil/Ikincil).</span><span class="sxs-lookup"><span data-stu-id="60f05-119">Search Service admin key kind (Primary/Secondary).</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKeyKind
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60f05-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="60f05-120">-ParentObject</span></span>
<span data-ttu-id="60f05-121">Arama hizmeti giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="60f05-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="60f05-122">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="60f05-122">-ParentResourceId</span></span>
<span data-ttu-id="60f05-123">Arama hizmeti kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="60f05-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="60f05-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60f05-124">-ResourceGroupName</span></span>
<span data-ttu-id="60f05-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="60f05-125">Resource Group name.</span></span>

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

### <span data-ttu-id="60f05-126">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="60f05-126">-ServiceName</span></span>
<span data-ttu-id="60f05-127">Arama hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="60f05-127">Search Service name.</span></span>

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

### <span data-ttu-id="60f05-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="60f05-128">-Confirm</span></span>
<span data-ttu-id="60f05-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="60f05-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60f05-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60f05-130">-WhatIf</span></span>
<span data-ttu-id="60f05-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="60f05-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60f05-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="60f05-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60f05-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60f05-133">CommonParameters</span></span>
<span data-ttu-id="60f05-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="60f05-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60f05-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60f05-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60f05-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="60f05-136">INPUTS</span></span>

### <span data-ttu-id="60f05-137">Microsoft. Azure. Commands. Management. Search. model. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="60f05-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="60f05-138">Parametreler: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="60f05-138">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="60f05-139">System. String</span><span class="sxs-lookup"><span data-stu-id="60f05-139">System.String</span></span>

## <span data-ttu-id="60f05-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="60f05-140">OUTPUTS</span></span>

### <span data-ttu-id="60f05-141">Microsoft. Azure. Commands. Management. Search. model. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="60f05-141">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="60f05-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="60f05-142">NOTES</span></span>

## <span data-ttu-id="60f05-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="60f05-143">RELATED LINKS</span></span>

[<span data-ttu-id="60f05-144">Get-AzureRmSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="60f05-144">Get-AzureRmSearchAdminKeyPair</span></span>](./Get-AzureRmSearchAdminKeyPair.md)
