---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
ms.openlocfilehash: 62b8dff0b2d5fc52b080b35e4a205ad2bb00ea52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098971"
---
# <span data-ttu-id="0dd51-101">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="0dd51-101">Remove-AzSearchService</span></span>

## <span data-ttu-id="0dd51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dd51-102">SYNOPSIS</span></span>
<span data-ttu-id="0dd51-103">Azure Search hizmetini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="0dd51-103">Remove an Azure Search service.</span></span>

## <span data-ttu-id="0dd51-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0dd51-104">SYNTAX</span></span>

### <span data-ttu-id="0dd51-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0dd51-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dd51-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="0dd51-106">InputObjectParameterSet</span></span>
```
Remove-AzSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dd51-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="0dd51-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchService [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dd51-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0dd51-108">DESCRIPTION</span></span>
<span data-ttu-id="0dd51-109">**Remove-AzSearchService** cmdlet 'ı, Azure Search hizmetini belirtilen parametrelerle kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0dd51-109">The **Remove-AzSearchService** cmdlet removes an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="0dd51-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0dd51-110">EXAMPLES</span></span>

### <span data-ttu-id="0dd51-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0dd51-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="0dd51-112">Örnek, bir Azure Search hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0dd51-112">The example removes an Azure Search service.</span></span>

## <span data-ttu-id="0dd51-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0dd51-113">PARAMETERS</span></span>

### <span data-ttu-id="0dd51-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dd51-114">-DefaultProfile</span></span>
<span data-ttu-id="0dd51-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0dd51-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0dd51-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0dd51-116">-Force</span></span>
<span data-ttu-id="0dd51-117">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="0dd51-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0dd51-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0dd51-118">-InputObject</span></span>
<span data-ttu-id="0dd51-119">Arama hizmeti giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0dd51-119">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0dd51-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="0dd51-120">-Name</span></span>
<span data-ttu-id="0dd51-121">Arama hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="0dd51-121">Search Service name.</span></span>

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

### <span data-ttu-id="0dd51-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0dd51-122">-PassThru</span></span>
<span data-ttu-id="0dd51-123">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="0dd51-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="0dd51-124">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="0dd51-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="0dd51-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dd51-125">-ResourceGroupName</span></span>
<span data-ttu-id="0dd51-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0dd51-126">Resource Group name.</span></span>

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

### <span data-ttu-id="0dd51-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0dd51-127">-ResourceId</span></span>
<span data-ttu-id="0dd51-128">Arama hizmeti kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="0dd51-128">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dd51-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="0dd51-129">-Confirm</span></span>
<span data-ttu-id="0dd51-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0dd51-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dd51-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dd51-131">-WhatIf</span></span>
<span data-ttu-id="0dd51-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0dd51-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dd51-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0dd51-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dd51-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dd51-134">CommonParameters</span></span>
<span data-ttu-id="0dd51-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0dd51-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dd51-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dd51-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dd51-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0dd51-137">INPUTS</span></span>

### <span data-ttu-id="0dd51-138">Microsoft. Azure. Commands. Management. Search. model. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="0dd51-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="0dd51-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0dd51-139">System.String</span></span>

## <span data-ttu-id="0dd51-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0dd51-140">OUTPUTS</span></span>

### <span data-ttu-id="0dd51-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0dd51-141">System.Boolean</span></span>

## <span data-ttu-id="0dd51-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0dd51-142">NOTES</span></span>

## <span data-ttu-id="0dd51-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0dd51-143">RELATED LINKS</span></span>

[<span data-ttu-id="0dd51-144">Yeni-Azaramahizmeti</span><span class="sxs-lookup"><span data-stu-id="0dd51-144">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="0dd51-145">Get-Azaramahizmeti</span><span class="sxs-lookup"><span data-stu-id="0dd51-145">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="0dd51-146">Set-Azaramahizmeti</span><span class="sxs-lookup"><span data-stu-id="0dd51-146">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

