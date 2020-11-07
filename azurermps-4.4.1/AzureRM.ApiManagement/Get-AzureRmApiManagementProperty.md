---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
ms.openlocfilehash: 7542e9621d90ffdb19bb8db679592dd17a216d5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762779"
---
# <span data-ttu-id="1be91-101">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="1be91-101">Get-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="1be91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1be91-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1be91-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1be91-103">SYNTAX</span></span>

### <span data-ttu-id="1be91-104">Tüm özellikleri al (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1be91-104">Get all properties (Default)</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1be91-105">Özellik KIMLIĞINE göre alma</span><span class="sxs-lookup"><span data-stu-id="1be91-105">Get by property ID</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1be91-106">Ad içeren özellikleri bulma</span><span class="sxs-lookup"><span data-stu-id="1be91-106">Find properties containing Name</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1be91-107">Etikete göre özellikler bul</span><span class="sxs-lookup"><span data-stu-id="1be91-107">Find properties by Tag</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1be91-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1be91-108">DESCRIPTION</span></span>

## <span data-ttu-id="1be91-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1be91-109">EXAMPLES</span></span>

### <span data-ttu-id="1be91-110">2</span><span class="sxs-lookup"><span data-stu-id="1be91-110">1:</span></span>
```
PS C:\> Get-AzureRmApiManagementProperty -Context $Context -Name $PropertyName
```

## <span data-ttu-id="1be91-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1be91-111">PARAMETERS</span></span>

### <span data-ttu-id="1be91-112">-Context</span><span class="sxs-lookup"><span data-stu-id="1be91-112">-Context</span></span>
```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1be91-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="1be91-113">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: Find properties containing Name
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1be91-114">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="1be91-114">-PropertyId</span></span>
```yaml
Type: System.String
Parameter Sets: Get by property ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1be91-115">Etiketli</span><span class="sxs-lookup"><span data-stu-id="1be91-115">-Tag</span></span>
<span data-ttu-id="1be91-116">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="1be91-116">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1be91-117">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="1be91-117">For example:</span></span>

<span data-ttu-id="1be91-118">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="1be91-118">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.String
Parameter Sets: Find properties by Tag
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1be91-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1be91-119">-DefaultProfile</span></span>
<span data-ttu-id="1be91-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1be91-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1be91-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1be91-121">CommonParameters</span></span>
<span data-ttu-id="1be91-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1be91-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1be91-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1be91-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1be91-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1be91-124">INPUTS</span></span>

## <span data-ttu-id="1be91-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1be91-125">OUTPUTS</span></span>

### <span data-ttu-id="1be91-126">System. Koleksiyonlar. Generic. IList ' 1 [Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. PsApiManagementProperty]</span><span class="sxs-lookup"><span data-stu-id="1be91-126">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty]</span></span>

### <span data-ttu-id="1be91-127">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproperty</span><span class="sxs-lookup"><span data-stu-id="1be91-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="1be91-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1be91-128">NOTES</span></span>

## <span data-ttu-id="1be91-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1be91-129">RELATED LINKS</span></span>

