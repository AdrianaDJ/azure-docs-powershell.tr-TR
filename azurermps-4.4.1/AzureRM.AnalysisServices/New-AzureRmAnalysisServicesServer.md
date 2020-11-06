---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 0093393f926af257e07b7d697a7f267fa62b483a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587052"
---
# <span data-ttu-id="9f38a-101">New-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9f38a-101">New-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="9f38a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f38a-102">SYNOPSIS</span></span>
<span data-ttu-id="9f38a-103">Yeni bir Analysis Services sunucusu oluşturur</span><span class="sxs-lookup"><span data-stu-id="9f38a-103">Creates a new Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f38a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f38a-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f38a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f38a-105">DESCRIPTION</span></span>
<span data-ttu-id="9f38a-106">New-AzureRmAnalysisServicesServer cmdlet 'i yeni bir Analysis Services sunucusu oluşturur</span><span class="sxs-lookup"><span data-stu-id="9f38a-106">The New-AzureRmAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="9f38a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f38a-107">EXAMPLES</span></span>

### <span data-ttu-id="9f38a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9f38a-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="9f38a-109">A-US ve kaynak grubu testresrourcegroup 'ta TestServer adlı bir sunucu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9f38a-109">Creates a server named testserver in the Azure region West-US and in resource group testresrourcegroup.</span></span> <span data-ttu-id="9f38a-110">Sunucu için SKU düzeyi S1 olacaktır.</span><span class="sxs-lookup"><span data-stu-id="9f38a-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="9f38a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f38a-111">PARAMETERS</span></span>

### <span data-ttu-id="9f38a-112">-Yönetici</span><span class="sxs-lookup"><span data-stu-id="9f38a-112">-Administrator</span></span>
<span data-ttu-id="9f38a-113">Sunucuda yönetici olarak ayarlanacak Kullanıcı veya grupların virgülle ayrılmış listesini temsil eden dize.</span><span class="sxs-lookup"><span data-stu-id="9f38a-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="9f38a-114">Kullanıcıların veya grupların UPN biçiminde ( user@contoso.com veya groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="9f38a-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f38a-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="9f38a-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="9f38a-116">Çözümleme Hizmetleri sunucusunu yedeklemek için blob kapsayıcı URI 'Si</span><span class="sxs-lookup"><span data-stu-id="9f38a-116">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f38a-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="9f38a-117">-Location</span></span>
<span data-ttu-id="9f38a-118">Analysis Services sunucusunun barındırıldığı Azure bölgesi</span><span class="sxs-lookup"><span data-stu-id="9f38a-118">The Azure region where the Analysis Services server is hosted</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: North Central US, South Central US, Central US, West Europe, North Europe, West US, East US, East US 2, Japan East, Japan West, Brazil South, Southeast Asia, East Asia, Australia East, Australia Southeast

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f38a-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="9f38a-119">-Name</span></span>
<span data-ttu-id="9f38a-120">Analysis Services sunucusunun adı</span><span class="sxs-lookup"><span data-stu-id="9f38a-120">Name of the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f38a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f38a-121">-ResourceGroupName</span></span>
<span data-ttu-id="9f38a-122">Sunucunun ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="9f38a-122">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f38a-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="9f38a-123">-Sku</span></span>
<span data-ttu-id="9f38a-124">Sunucunun SKU adı.</span><span class="sxs-lookup"><span data-stu-id="9f38a-124">The name of the Sku for the server.</span></span>
<span data-ttu-id="9f38a-125">Desteklenen değerler, Standart katman için 0 ' ın 1 ' i 1 ' in 2 ' nin 4 ' ü; ' B1 ', temel katman için ' B2 ' ve geliştirme katmanı için 1 '.</span><span class="sxs-lookup"><span data-stu-id="9f38a-125">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f38a-126">Etiketli</span><span class="sxs-lookup"><span data-stu-id="9f38a-126">-Tag</span></span>
<span data-ttu-id="9f38a-127">Sunucuda etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="9f38a-127">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f38a-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="9f38a-128">-Confirm</span></span>
<span data-ttu-id="9f38a-129">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="9f38a-129">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f38a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f38a-130">-WhatIf</span></span>
<span data-ttu-id="9f38a-131">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="9f38a-131">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f38a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f38a-132">CommonParameters</span></span>
<span data-ttu-id="9f38a-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9f38a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f38a-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f38a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f38a-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f38a-135">INPUTS</span></span>

## <span data-ttu-id="9f38a-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f38a-136">OUTPUTS</span></span>

### <span data-ttu-id="9f38a-137">Microsoft. Azure. Commands. AnalysisServices. modeller. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9f38a-137">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="9f38a-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f38a-138">NOTES</span></span>
<span data-ttu-id="9f38a-139">Diğer ad: New-AzureAs</span><span class="sxs-lookup"><span data-stu-id="9f38a-139">Alias: New-AzureAs</span></span>

## <span data-ttu-id="9f38a-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f38a-140">RELATED LINKS</span></span>

[<span data-ttu-id="9f38a-141">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9f38a-141">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="9f38a-142">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9f38a-142">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
