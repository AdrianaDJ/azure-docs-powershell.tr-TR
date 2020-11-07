---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 3af374d6609a7063581e06aa8aa496e56a1fd45c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762589"
---
# <span data-ttu-id="ff146-101">Set-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="ff146-101">Set-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="ff146-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff146-102">SYNOPSIS</span></span>
<span data-ttu-id="ff146-103">Zaten mevcut olan kaydedilmiş bir aramayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ff146-103">Updates a saved search that already exists.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff146-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ff146-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff146-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ff146-105">DESCRIPTION</span></span>
<span data-ttu-id="ff146-106">**Set-Azurermoperationalınsightssavedsearch** cmdlet 'i zaten var olan kaydedilmiş bir aramayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ff146-106">The **Set-AzureRmOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="ff146-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ff146-107">EXAMPLES</span></span>

### <span data-ttu-id="ff146-108">Örnek 1: kaydedilmiş bir aramayı güncelleştirilmiş özelliklerle ayarlar</span><span class="sxs-lookup"><span data-stu-id="ff146-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="ff146-109">Bu komut, kaydedilmiş bir aramayı güncelleştirilmiş özelliklerle ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ff146-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="ff146-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ff146-110">PARAMETERS</span></span>

### <span data-ttu-id="ff146-111">-Kategori</span><span class="sxs-lookup"><span data-stu-id="ff146-111">-Category</span></span>
<span data-ttu-id="ff146-112">Kategori adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ff146-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="ff146-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff146-113">-DefaultProfile</span></span>
<span data-ttu-id="ff146-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ff146-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff146-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ff146-115">-DisplayName</span></span>
<span data-ttu-id="ff146-116">Görünen adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="ff146-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="ff146-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="ff146-117">-ETag</span></span>
<span data-ttu-id="ff146-118">ETag adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ff146-118">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="ff146-119">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="ff146-119">-Query</span></span>
<span data-ttu-id="ff146-120">Sorgu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ff146-120">Specifies the query name.</span></span>

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

### <span data-ttu-id="ff146-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff146-121">-ResourceGroupName</span></span>
<span data-ttu-id="ff146-122">Kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ff146-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="ff146-123">-Savedsearchıd</span><span class="sxs-lookup"><span data-stu-id="ff146-123">-SavedSearchId</span></span>
<span data-ttu-id="ff146-124">Kayıtlı arama KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ff146-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="ff146-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ff146-125">-Tag</span></span>
<span data-ttu-id="ff146-126">Kaydedilmiş arama etiketleri.</span><span class="sxs-lookup"><span data-stu-id="ff146-126">The saved search tags.</span></span>

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

### <span data-ttu-id="ff146-127">-Version</span><span class="sxs-lookup"><span data-stu-id="ff146-127">-Version</span></span>
```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff146-128">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="ff146-128">-WorkspaceName</span></span>
<span data-ttu-id="ff146-129">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ff146-129">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="ff146-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff146-130">CommonParameters</span></span>
<span data-ttu-id="ff146-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ff146-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff146-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff146-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff146-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ff146-133">INPUTS</span></span>

### <span data-ttu-id="ff146-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ff146-134">System.String</span></span>

### <span data-ttu-id="ff146-135">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ff146-135">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ff146-136">System. Int64</span><span class="sxs-lookup"><span data-stu-id="ff146-136">System.Int64</span></span>

## <span data-ttu-id="ff146-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ff146-137">OUTPUTS</span></span>

### <span data-ttu-id="ff146-138">Sistem .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="ff146-138">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="ff146-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ff146-139">NOTES</span></span>

## <span data-ttu-id="ff146-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ff146-140">RELATED LINKS</span></span>

[<span data-ttu-id="ff146-141">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="ff146-141">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


