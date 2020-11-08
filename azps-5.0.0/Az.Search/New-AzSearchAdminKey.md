---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchadminkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
ms.openlocfilehash: ae925d39dab3b56e70cb7c42b320e57eb7f7811a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279150"
---
# <span data-ttu-id="84fc8-101">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="84fc8-101">New-AzSearchAdminKey</span></span>

## <span data-ttu-id="84fc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="84fc8-103">Azure Search hizmetinin yönetim anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="84fc8-103">Regenerates an admin key of the Azure Search service.</span></span>

## <span data-ttu-id="84fc8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="84fc8-104">SYNTAX</span></span>

### <span data-ttu-id="84fc8-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="84fc8-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchAdminKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyKind <PSSearchAdminKeyKind>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84fc8-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84fc8-106">ParentObjectParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentObject] <PSSearchService> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84fc8-107">Parentresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="84fc8-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentResourceId] <String> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84fc8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="84fc8-108">DESCRIPTION</span></span>
<span data-ttu-id="84fc8-109">**Yeni-Azaramaadminkey** cmdlet 'ı Azure Search hizmetinin yönetim anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="84fc8-109">The **New-AzSearchAdminKey** cmdlet regenerates an admin key of the Azure Search service.</span></span>

## <span data-ttu-id="84fc8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="84fc8-110">EXAMPLES</span></span>

### <span data-ttu-id="84fc8-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="84fc8-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchAdminKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyKind Primary

Confirm
Are you sure you want to regenerate 'Primary' key for Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

Primary                          Secondary
-------                          ---------
85B3813D11904B591BE8A196C2C743A1 CEF791D5BAC2E6C0B232C56702F21E87
```

<span data-ttu-id="84fc8-112">Örnek Azure Search hizmetinin birincil anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="84fc8-112">The example regenerates Primary key of the Azure Search Service.</span></span>

## <span data-ttu-id="84fc8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="84fc8-113">PARAMETERS</span></span>

### <span data-ttu-id="84fc8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84fc8-114">-DefaultProfile</span></span>
<span data-ttu-id="84fc8-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="84fc8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84fc8-116">-Force</span><span class="sxs-lookup"><span data-stu-id="84fc8-116">-Force</span></span>
<span data-ttu-id="84fc8-117">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="84fc8-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="84fc8-118">-KeyKind</span><span class="sxs-lookup"><span data-stu-id="84fc8-118">-KeyKind</span></span>
<span data-ttu-id="84fc8-119">Arama Hizmeti Yöneticisi anahtar türü (birincil/Ikincil).</span><span class="sxs-lookup"><span data-stu-id="84fc8-119">Search Service admin key kind (Primary/Secondary).</span></span>

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

### <span data-ttu-id="84fc8-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="84fc8-120">-ParentObject</span></span>
<span data-ttu-id="84fc8-121">Arama hizmeti giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="84fc8-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="84fc8-122">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="84fc8-122">-ParentResourceId</span></span>
<span data-ttu-id="84fc8-123">Arama hizmeti kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="84fc8-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="84fc8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84fc8-124">-ResourceGroupName</span></span>
<span data-ttu-id="84fc8-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="84fc8-125">Resource Group name.</span></span>

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

### <span data-ttu-id="84fc8-126">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="84fc8-126">-ServiceName</span></span>
<span data-ttu-id="84fc8-127">Arama hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="84fc8-127">Search Service name.</span></span>

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

### <span data-ttu-id="84fc8-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="84fc8-128">-Confirm</span></span>
<span data-ttu-id="84fc8-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="84fc8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84fc8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84fc8-130">-WhatIf</span></span>
<span data-ttu-id="84fc8-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="84fc8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84fc8-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="84fc8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84fc8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84fc8-133">CommonParameters</span></span>
<span data-ttu-id="84fc8-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="84fc8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84fc8-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84fc8-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84fc8-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="84fc8-136">INPUTS</span></span>

### <span data-ttu-id="84fc8-137">Microsoft. Azure. Commands. Management. Search. model. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="84fc8-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="84fc8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="84fc8-138">System.String</span></span>

## <span data-ttu-id="84fc8-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="84fc8-139">OUTPUTS</span></span>

### <span data-ttu-id="84fc8-140">Microsoft. Azure. Commands. Management. Search. model. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="84fc8-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="84fc8-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="84fc8-141">NOTES</span></span>

## <span data-ttu-id="84fc8-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="84fc8-142">RELATED LINKS</span></span>

[<span data-ttu-id="84fc8-143">Get-Azaramaadminkeypair</span><span class="sxs-lookup"><span data-stu-id="84fc8-143">Get-AzSearchAdminKeyPair</span></span>](./Get-AzSearchAdminKeyPair.md)
