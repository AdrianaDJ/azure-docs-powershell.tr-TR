---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
ms.openlocfilehash: 47167e0729ab3476c74124e16d6ae95901f57ad2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589922"
---
# <span data-ttu-id="d748b-101">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="d748b-101">Get-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="d748b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d748b-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d748b-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d748b-103">SYNTAX</span></span>

### <span data-ttu-id="d748b-104">GetAllProperties (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d748b-104">GetAllProperties (Default)</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d748b-105">Getbypropertyıd</span><span class="sxs-lookup"><span data-stu-id="d748b-105">GetByPropertyId</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d748b-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="d748b-106">GetByName</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d748b-107">GetByTag</span><span class="sxs-lookup"><span data-stu-id="d748b-107">GetByTag</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d748b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d748b-108">DESCRIPTION</span></span>

## <span data-ttu-id="d748b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d748b-109">EXAMPLES</span></span>

### <span data-ttu-id="d748b-110">Örnek 1: ada göre Özellik Al</span><span class="sxs-lookup"><span data-stu-id="d748b-110">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

## <span data-ttu-id="d748b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d748b-111">PARAMETERS</span></span>

### <span data-ttu-id="d748b-112">-Context</span><span class="sxs-lookup"><span data-stu-id="d748b-112">-Context</span></span>
```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d748b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d748b-113">-DefaultProfile</span></span>
<span data-ttu-id="d748b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d748b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d748b-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="d748b-115">-Name</span></span>
```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d748b-116">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="d748b-116">-PropertyId</span></span>
```yaml
Type: String
Parameter Sets: GetByPropertyId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d748b-117">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d748b-117">-Tag</span></span>
<span data-ttu-id="d748b-118">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="d748b-118">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d748b-119">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="d748b-119">For example:</span></span>

<span data-ttu-id="d748b-120">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="d748b-120">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: String
Parameter Sets: GetByTag
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d748b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d748b-121">CommonParameters</span></span>
<span data-ttu-id="d748b-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d748b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d748b-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d748b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d748b-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d748b-124">INPUTS</span></span>

### <span data-ttu-id="d748b-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d748b-125">None</span></span>
<span data-ttu-id="d748b-126">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="d748b-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d748b-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d748b-127">OUTPUTS</span></span>

### <span data-ttu-id="d748b-128">System. Koleksiyonlar. Generic. IList ' 1 [Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. PsApiManagementProperty]</span><span class="sxs-lookup"><span data-stu-id="d748b-128">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty]</span></span>

### <span data-ttu-id="d748b-129">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproperty</span><span class="sxs-lookup"><span data-stu-id="d748b-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="d748b-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d748b-130">NOTES</span></span>

## <span data-ttu-id="d748b-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d748b-131">RELATED LINKS</span></span>

