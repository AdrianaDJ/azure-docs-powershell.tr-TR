---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/remove-azurermsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchQueryKey.md
ms.openlocfilehash: 1dbdf342335ca204287ccfd2efea737f2eb747fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592262"
---
# <span data-ttu-id="62aed-101">Remove-AzureRmSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="62aed-101">Remove-AzureRmSearchQueryKey</span></span>

## <span data-ttu-id="62aed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62aed-102">SYNOPSIS</span></span>
<span data-ttu-id="62aed-103">Azure Search hizmetinden sorgu anahtarını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="62aed-103">Remove the query key from the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62aed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="62aed-104">SYNTAX</span></span>

### <span data-ttu-id="62aed-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="62aed-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzureRmSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62aed-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62aed-106">ParentObjectParameterSet</span></span>
```
Remove-AzureRmSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62aed-107">Parentresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="62aed-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzureRmSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62aed-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="62aed-108">DESCRIPTION</span></span>
<span data-ttu-id="62aed-109">**Remove-AzureRmSearchQueryKey** cmdlet 'ı Azure Search hizmetinden sorgu anahtarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="62aed-109">The **Remove-AzureRmSearchQueryKey** cmdlet removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="62aed-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="62aed-110">EXAMPLES</span></span>

### <span data-ttu-id="62aed-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="62aed-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name         Key                             
----         ---                             
             D260F448EA192EBC19D59F7E5670E8BB
NewQueryKey1 B4C13E3F6FA76100D3488673CFDCD438

PS C:\> Remove-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyValue B4C13E3F6FA76100D3488673CFDCD438

Confirm
Are you sure you want to remove query key 'B4C13E3F6FA76100D3488673CFDCD438'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="62aed-112">Örnekte, sorgu anahtarı Azure Search hizmetinden kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="62aed-112">The example removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="62aed-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="62aed-113">PARAMETERS</span></span>

### <span data-ttu-id="62aed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62aed-114">-DefaultProfile</span></span>
<span data-ttu-id="62aed-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="62aed-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62aed-116">-Force</span><span class="sxs-lookup"><span data-stu-id="62aed-116">-Force</span></span>
<span data-ttu-id="62aed-117">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="62aed-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="62aed-118">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="62aed-118">-KeyValue</span></span>
<span data-ttu-id="62aed-119">Arama Hizmeti sorgu anahtar değeri.</span><span class="sxs-lookup"><span data-stu-id="62aed-119">Search Service query key value.</span></span>

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

### <span data-ttu-id="62aed-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="62aed-120">-ParentObject</span></span>
<span data-ttu-id="62aed-121">Arama hizmeti giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="62aed-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="62aed-122">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="62aed-122">-ParentResourceId</span></span>
<span data-ttu-id="62aed-123">Arama hizmeti kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="62aed-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="62aed-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="62aed-124">-PassThru</span></span>
<span data-ttu-id="62aed-125">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="62aed-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="62aed-126">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="62aed-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="62aed-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62aed-127">-ResourceGroupName</span></span>
<span data-ttu-id="62aed-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="62aed-128">Resource Group name.</span></span>

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

### <span data-ttu-id="62aed-129">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="62aed-129">-ServiceName</span></span>
<span data-ttu-id="62aed-130">Arama hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="62aed-130">Search Service name.</span></span>

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

### <span data-ttu-id="62aed-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="62aed-131">-Confirm</span></span>
<span data-ttu-id="62aed-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="62aed-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62aed-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62aed-133">-WhatIf</span></span>
<span data-ttu-id="62aed-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="62aed-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62aed-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="62aed-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62aed-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62aed-136">CommonParameters</span></span>
<span data-ttu-id="62aed-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="62aed-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62aed-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62aed-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62aed-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="62aed-139">INPUTS</span></span>

### <span data-ttu-id="62aed-140">Microsoft. Azure. Commands. Management. Search. model. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="62aed-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="62aed-141">Parametreler: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="62aed-141">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="62aed-142">System. String</span><span class="sxs-lookup"><span data-stu-id="62aed-142">System.String</span></span>

## <span data-ttu-id="62aed-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="62aed-143">OUTPUTS</span></span>

### <span data-ttu-id="62aed-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="62aed-144">System.Boolean</span></span>

## <span data-ttu-id="62aed-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="62aed-145">NOTES</span></span>

## <span data-ttu-id="62aed-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="62aed-146">RELATED LINKS</span></span>

[<span data-ttu-id="62aed-147">New-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="62aed-147">New-AzureRmSearchQueryKey.md</span></span>](./New-AzureRmSearchQueryKey.md)

[<span data-ttu-id="62aed-148">Get-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="62aed-148">Get-AzureRmSearchQueryKey.md</span></span>](./Get-AzureRmSearchQueryKey.md)
