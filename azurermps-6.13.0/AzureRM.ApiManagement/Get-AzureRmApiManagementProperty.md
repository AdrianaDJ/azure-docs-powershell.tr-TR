---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
ms.openlocfilehash: 22cba1b904032ee654b091d1adae541848fd50c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573089"
---
# <span data-ttu-id="3c69d-101">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="3c69d-101">Get-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="3c69d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c69d-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c69d-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3c69d-103">SYNTAX</span></span>

### <span data-ttu-id="3c69d-104">GetAllProperties (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3c69d-104">GetAllProperties (Default)</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3c69d-105">Getbypropertyıd</span><span class="sxs-lookup"><span data-stu-id="3c69d-105">GetByPropertyId</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c69d-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="3c69d-106">GetByName</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c69d-107">GetByTag</span><span class="sxs-lookup"><span data-stu-id="3c69d-107">GetByTag</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c69d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c69d-108">DESCRIPTION</span></span>

## <span data-ttu-id="3c69d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3c69d-109">EXAMPLES</span></span>

### <span data-ttu-id="3c69d-110">Örnek 1: ada göre Özellik Al</span><span class="sxs-lookup"><span data-stu-id="3c69d-110">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

## <span data-ttu-id="3c69d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3c69d-111">PARAMETERS</span></span>

### <span data-ttu-id="3c69d-112">-Context</span><span class="sxs-lookup"><span data-stu-id="3c69d-112">-Context</span></span>
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

### <span data-ttu-id="3c69d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c69d-113">-DefaultProfile</span></span>
<span data-ttu-id="3c69d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3c69d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c69d-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="3c69d-115">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c69d-116">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="3c69d-116">-PropertyId</span></span>
```yaml
Type: System.String
Parameter Sets: GetByPropertyId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c69d-117">Etiketli</span><span class="sxs-lookup"><span data-stu-id="3c69d-117">-Tag</span></span>
<span data-ttu-id="3c69d-118">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="3c69d-118">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3c69d-119">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="3c69d-119">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTag
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c69d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c69d-120">CommonParameters</span></span>
<span data-ttu-id="3c69d-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3c69d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c69d-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c69d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c69d-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3c69d-123">INPUTS</span></span>

### <span data-ttu-id="3c69d-124">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="3c69d-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3c69d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3c69d-125">System.String</span></span>

## <span data-ttu-id="3c69d-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3c69d-126">OUTPUTS</span></span>

### <span data-ttu-id="3c69d-127">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproperty</span><span class="sxs-lookup"><span data-stu-id="3c69d-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="3c69d-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3c69d-128">NOTES</span></span>

## <span data-ttu-id="3c69d-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3c69d-129">RELATED LINKS</span></span>
