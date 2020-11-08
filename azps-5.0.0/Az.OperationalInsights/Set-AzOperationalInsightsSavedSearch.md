---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 46427a53a04e94fe42c20cfa2e6ab016a6b8c613
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278075"
---
# <span data-ttu-id="fe23d-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="fe23d-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="fe23d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe23d-102">SYNOPSIS</span></span>
<span data-ttu-id="fe23d-103">Zaten mevcut olan kaydedilmiş bir aramayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fe23d-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="fe23d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fe23d-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe23d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe23d-105">DESCRIPTION</span></span>
<span data-ttu-id="fe23d-106">**Set-Azoperationalınsightssavedsearch** cmdlet 'i zaten var olan kaydedilmiş bir aramayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fe23d-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="fe23d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fe23d-107">EXAMPLES</span></span>

### <span data-ttu-id="fe23d-108">Örnek 1: kaydedilmiş bir aramayı güncelleştirilmiş özelliklerle ayarlar</span><span class="sxs-lookup"><span data-stu-id="fe23d-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="fe23d-109">Bu komut, kaydedilmiş bir aramayı güncelleştirilmiş özelliklerle ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fe23d-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="fe23d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fe23d-110">PARAMETERS</span></span>

### <span data-ttu-id="fe23d-111">-Kategori</span><span class="sxs-lookup"><span data-stu-id="fe23d-111">-Category</span></span>
<span data-ttu-id="fe23d-112">Kategori adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe23d-112">Specifies the category name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe23d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe23d-113">-DefaultProfile</span></span>
<span data-ttu-id="fe23d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fe23d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe23d-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fe23d-115">-DisplayName</span></span>
<span data-ttu-id="fe23d-116">Görünen adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe23d-116">Specifies the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe23d-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="fe23d-117">-ETag</span></span>
<span data-ttu-id="fe23d-118">ETag adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe23d-118">Specifies the ETag name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe23d-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="fe23d-119">-FunctionAlias</span></span>
<span data-ttu-id="fe23d-120">Sorgu işlev olarak işlev görüyorsa işlev diğer adı.</span><span class="sxs-lookup"><span data-stu-id="fe23d-120">The function alias if query serves as a function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe23d-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="fe23d-121">-FunctionParameter</span></span>
<span data-ttu-id="fe23d-122">Sorgu işlev olarak işlev görüyorsa isteğe bağlı işlev parametreleri.</span><span class="sxs-lookup"><span data-stu-id="fe23d-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="fe23d-123">Değer şu biçimde olmalıdır: ' param-name1: Type1 = default_value1, param-AD2: type2 = default_value2 '.</span><span class="sxs-lookup"><span data-stu-id="fe23d-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="fe23d-124">Daha fazla örnek ve uygun söz dizimi için lütfen başvuru bölümüne bakın https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="fe23d-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FunctionParameters

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe23d-125">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="fe23d-125">-Query</span></span>
<span data-ttu-id="fe23d-126">Sorgu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe23d-126">Specifies the query name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe23d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe23d-127">-ResourceGroupName</span></span>
<span data-ttu-id="fe23d-128">Kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe23d-128">Specifies the resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe23d-129">-Savedsearchıd</span><span class="sxs-lookup"><span data-stu-id="fe23d-129">-SavedSearchId</span></span>
<span data-ttu-id="fe23d-130">Kayıtlı arama KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe23d-130">Specifies the saved search ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe23d-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="fe23d-131">-Tag</span></span>
<span data-ttu-id="fe23d-132">Kaydedilmiş arama etiketleri.</span><span class="sxs-lookup"><span data-stu-id="fe23d-132">The saved search tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe23d-133">-Version</span><span class="sxs-lookup"><span data-stu-id="fe23d-133">-Version</span></span>
```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe23d-134">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="fe23d-134">-WorkspaceName</span></span>
<span data-ttu-id="fe23d-135">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe23d-135">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe23d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe23d-136">CommonParameters</span></span>
<span data-ttu-id="fe23d-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fe23d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe23d-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fe23d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe23d-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fe23d-139">INPUTS</span></span>

### <span data-ttu-id="fe23d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="fe23d-140">System.String</span></span>

### <span data-ttu-id="fe23d-141">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fe23d-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fe23d-142">System. Int64</span><span class="sxs-lookup"><span data-stu-id="fe23d-142">System.Int64</span></span>

## <span data-ttu-id="fe23d-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fe23d-143">OUTPUTS</span></span>

### <span data-ttu-id="fe23d-144">Sistem .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="fe23d-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="fe23d-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fe23d-145">NOTES</span></span>

## <span data-ttu-id="fe23d-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fe23d-146">RELATED LINKS</span></span>

[<span data-ttu-id="fe23d-147">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="fe23d-147">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


