---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: f57a95e97c0ec74e7e45338e15a028feab60849b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591478"
---
# <span data-ttu-id="0c17e-101">Get-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="0c17e-101">Get-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="0c17e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c17e-102">SYNOPSIS</span></span>
<span data-ttu-id="0c17e-103">API 'nin tüm API düzeltmelerinin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="0c17e-103">Gets details of all the API Revisions of an API</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c17e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c17e-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c17e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c17e-105">DESCRIPTION</span></span>
<span data-ttu-id="0c17e-106">**Get-Azurermapsananagementapirevision** cmdlet 'inin tüm düzeltmelerinin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="0c17e-106">The **Get-AzureRmApiManagementApiRevision** cmdlet gets the details of all revisions of an API</span></span>

## <span data-ttu-id="0c17e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c17e-107">EXAMPLES</span></span>

### <span data-ttu-id="0c17e-108">Örnek 1: API 'nin tüm API düzeltmelerini alma</span><span class="sxs-lookup"><span data-stu-id="0c17e-108">Example 1: Get all API Revisions of an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiRevision -Context $ApiMgmtContext -ApiId "5adf6fbf0faadf3ad8558065"

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=3
ApiRevision     : 3
CreatedDateTime : 4/26/2018 10:57:42 PM
UpdatedDateTime : 4/26/2018 10:57:42 PM
Description     : ddsds
PrivateUrl      : /httpbin/v1;rev=3
IsOnline        : True
IsCurrent       : False

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=2
ApiRevision     : 2
CreatedDateTime : 4/26/2018 10:57:33 PM
UpdatedDateTime : 4/26/2018 10:57:33 PM
Description     : AA
PrivateUrl      : /httpbin/v1
IsOnline        : True
IsCurrent       : True

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=1
ApiRevision     : 1
CreatedDateTime : 4/24/2018 5:56:17 PM
UpdatedDateTime : 5/9/2018 9:29:06 PM
Description     :
PrivateUrl      : /httpbin/v1;rev=1
IsOnline        : True
IsCurrent       : False
```

<span data-ttu-id="0c17e-109">Bu komut, belirli bir API için belirtilen API 'nin tüm API düzeltmesini alır.</span><span class="sxs-lookup"><span data-stu-id="0c17e-109">This command gets all of the API revision of specified API for particular ApiManagement Context.</span></span>

## <span data-ttu-id="0c17e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c17e-110">PARAMETERS</span></span>

### <span data-ttu-id="0c17e-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="0c17e-111">-ApiId</span></span>
<span data-ttu-id="0c17e-112">Düzeltmeleri listelemek istediğimiz API tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="0c17e-112">API identifier whose revisions we want to list.</span></span>
<span data-ttu-id="0c17e-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="0c17e-113">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c17e-114">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="0c17e-114">-ApiRevision</span></span>
<span data-ttu-id="0c17e-115">Belirli API düzeltmesinin düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="0c17e-115">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="0c17e-116">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="0c17e-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c17e-117">-Context</span><span class="sxs-lookup"><span data-stu-id="0c17e-117">-Context</span></span>
<span data-ttu-id="0c17e-118">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="0c17e-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0c17e-119">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="0c17e-119">This parameter is required.</span></span>

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

### <span data-ttu-id="0c17e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c17e-120">-DefaultProfile</span></span>
<span data-ttu-id="0c17e-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0c17e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c17e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c17e-122">CommonParameters</span></span>
<span data-ttu-id="0c17e-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c17e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c17e-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c17e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c17e-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c17e-125">INPUTS</span></span>

### <span data-ttu-id="0c17e-126">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="0c17e-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0c17e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="0c17e-127">System.String</span></span>

## <span data-ttu-id="0c17e-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c17e-128">OUTPUTS</span></span>

### <span data-ttu-id="0c17e-129">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapirevision</span><span class="sxs-lookup"><span data-stu-id="0c17e-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span></span>

## <span data-ttu-id="0c17e-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c17e-130">NOTES</span></span>

## <span data-ttu-id="0c17e-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c17e-131">RELATED LINKS</span></span>
