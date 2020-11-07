---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
ms.openlocfilehash: ae781b4c53e373cdbd8338f4db75d6913c863bfd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759275"
---
# <span data-ttu-id="395c4-101">Remove-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="395c4-101">Remove-AzSearchQueryKey</span></span>

## <span data-ttu-id="395c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="395c4-102">SYNOPSIS</span></span>
<span data-ttu-id="395c4-103">Azure Search hizmetinden sorgu anahtarını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="395c4-103">Remove the query key from the Azure Search service.</span></span>

## <span data-ttu-id="395c4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="395c4-104">SYNTAX</span></span>

### <span data-ttu-id="395c4-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="395c4-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="395c4-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="395c4-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="395c4-107">Parentresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="395c4-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="395c4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="395c4-108">DESCRIPTION</span></span>
<span data-ttu-id="395c4-109">**Remove-AzSearchQueryKey** cmdlet 'ı, Azure Search hizmetinden sorgu anahtarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="395c4-109">The **Remove-AzSearchQueryKey** cmdlet removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="395c4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="395c4-110">EXAMPLES</span></span>

### <span data-ttu-id="395c4-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="395c4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name         Key                             
----         ---                             
             D260F448EA192EBC19D59F7E5670E8BB
NewQueryKey1 B4C13E3F6FA76100D3488673CFDCD438

PS C:\> Remove-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyValue B4C13E3F6FA76100D3488673CFDCD438

Confirm
Are you sure you want to remove query key 'B4C13E3F6FA76100D3488673CFDCD438'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="395c4-112">Örnekte, sorgu anahtarı Azure Search hizmetinden kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="395c4-112">The example removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="395c4-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="395c4-113">PARAMETERS</span></span>

### <span data-ttu-id="395c4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="395c4-114">-DefaultProfile</span></span>
<span data-ttu-id="395c4-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="395c4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="395c4-116">-Force</span><span class="sxs-lookup"><span data-stu-id="395c4-116">-Force</span></span>
<span data-ttu-id="395c4-117">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="395c4-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="395c4-118">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="395c4-118">-KeyValue</span></span>
<span data-ttu-id="395c4-119">Arama Hizmeti sorgu anahtar değeri.</span><span class="sxs-lookup"><span data-stu-id="395c4-119">Search Service query key value.</span></span>

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

### <span data-ttu-id="395c4-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="395c4-120">-ParentObject</span></span>
<span data-ttu-id="395c4-121">Arama hizmeti giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="395c4-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="395c4-122">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="395c4-122">-ParentResourceId</span></span>
<span data-ttu-id="395c4-123">Arama hizmeti kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="395c4-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="395c4-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="395c4-124">-PassThru</span></span>
<span data-ttu-id="395c4-125">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="395c4-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="395c4-126">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="395c4-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="395c4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="395c4-127">-ResourceGroupName</span></span>
<span data-ttu-id="395c4-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="395c4-128">Resource Group name.</span></span>

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

### <span data-ttu-id="395c4-129">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="395c4-129">-ServiceName</span></span>
<span data-ttu-id="395c4-130">Arama hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="395c4-130">Search Service name.</span></span>

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

### <span data-ttu-id="395c4-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="395c4-131">-Confirm</span></span>
<span data-ttu-id="395c4-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="395c4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="395c4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="395c4-133">-WhatIf</span></span>
<span data-ttu-id="395c4-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="395c4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="395c4-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="395c4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="395c4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="395c4-136">CommonParameters</span></span>
<span data-ttu-id="395c4-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="395c4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="395c4-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="395c4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="395c4-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="395c4-139">INPUTS</span></span>

### <span data-ttu-id="395c4-140">Microsoft. Azure. Commands. Management. Search. model. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="395c4-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="395c4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="395c4-141">System.String</span></span>

## <span data-ttu-id="395c4-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="395c4-142">OUTPUTS</span></span>

### <span data-ttu-id="395c4-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="395c4-143">System.Boolean</span></span>

## <span data-ttu-id="395c4-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="395c4-144">NOTES</span></span>

## <span data-ttu-id="395c4-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="395c4-145">RELATED LINKS</span></span>

[<span data-ttu-id="395c4-146">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="395c4-146">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="395c4-147">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="395c4-147">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)
