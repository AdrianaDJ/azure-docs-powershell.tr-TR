---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 535fbe737184b996ee0caa030c83137ea8cd1019
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93938691"
---
# <span data-ttu-id="1ad7c-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="1ad7c-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="1ad7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ad7c-102">SYNOPSIS</span></span>
<span data-ttu-id="1ad7c-103">Zaten mevcut olan kaydedilmiş bir aramayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1ad7c-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="1ad7c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1ad7c-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ad7c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1ad7c-105">DESCRIPTION</span></span>
<span data-ttu-id="1ad7c-106">**Set-Azoperationalınsightssavedsearch** cmdlet 'i zaten var olan kaydedilmiş bir aramayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1ad7c-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="1ad7c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1ad7c-107">EXAMPLES</span></span>

### <span data-ttu-id="1ad7c-108">Örnek 1: kaydedilmiş bir aramayı güncelleştirilmiş özelliklerle ayarlar</span><span class="sxs-lookup"><span data-stu-id="1ad7c-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="1ad7c-109">Bu komut, kaydedilmiş bir aramayı güncelleştirilmiş özelliklerle ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1ad7c-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="1ad7c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1ad7c-110">PARAMETERS</span></span>

### <span data-ttu-id="1ad7c-111">-Kategori</span><span class="sxs-lookup"><span data-stu-id="1ad7c-111">-Category</span></span>
<span data-ttu-id="1ad7c-112">Kategori adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ad7c-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="1ad7c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ad7c-113">-DefaultProfile</span></span>
<span data-ttu-id="1ad7c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1ad7c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ad7c-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1ad7c-115">-DisplayName</span></span>
<span data-ttu-id="1ad7c-116">Görünen adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ad7c-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="1ad7c-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="1ad7c-117">-ETag</span></span>
<span data-ttu-id="1ad7c-118">ETag adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ad7c-118">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="1ad7c-119">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="1ad7c-119">-Query</span></span>
<span data-ttu-id="1ad7c-120">Sorgu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ad7c-120">Specifies the query name.</span></span>

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

### <span data-ttu-id="1ad7c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ad7c-121">-ResourceGroupName</span></span>
<span data-ttu-id="1ad7c-122">Kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ad7c-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="1ad7c-123">-Savedsearchıd</span><span class="sxs-lookup"><span data-stu-id="1ad7c-123">-SavedSearchId</span></span>
<span data-ttu-id="1ad7c-124">Kayıtlı arama KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ad7c-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="1ad7c-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="1ad7c-125">-Tag</span></span>
<span data-ttu-id="1ad7c-126">Kaydedilmiş arama etiketleri.</span><span class="sxs-lookup"><span data-stu-id="1ad7c-126">The saved search tags.</span></span>

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

### <span data-ttu-id="1ad7c-127">-Version</span><span class="sxs-lookup"><span data-stu-id="1ad7c-127">-Version</span></span>
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

### <span data-ttu-id="1ad7c-128">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="1ad7c-128">-WorkspaceName</span></span>
<span data-ttu-id="1ad7c-129">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ad7c-129">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="1ad7c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ad7c-130">CommonParameters</span></span>
<span data-ttu-id="1ad7c-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1ad7c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ad7c-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ad7c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ad7c-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1ad7c-133">INPUTS</span></span>

### <span data-ttu-id="1ad7c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1ad7c-134">System.String</span></span>

### <span data-ttu-id="1ad7c-135">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1ad7c-135">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1ad7c-136">System. Int64</span><span class="sxs-lookup"><span data-stu-id="1ad7c-136">System.Int64</span></span>

## <span data-ttu-id="1ad7c-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1ad7c-137">OUTPUTS</span></span>

### <span data-ttu-id="1ad7c-138">Sistem .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="1ad7c-138">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="1ad7c-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1ad7c-139">NOTES</span></span>

## <span data-ttu-id="1ad7c-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1ad7c-140">RELATED LINKS</span></span>

[<span data-ttu-id="1ad7c-141">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="1ad7c-141">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

