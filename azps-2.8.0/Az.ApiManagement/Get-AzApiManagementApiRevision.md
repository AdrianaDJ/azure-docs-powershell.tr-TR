---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
ms.openlocfilehash: 5abd20ac1515cb2d7de96d7f5ed42938cee09a57
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753604"
---
# <span data-ttu-id="97d3f-101">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="97d3f-101">Get-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="97d3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97d3f-102">SYNOPSIS</span></span>
<span data-ttu-id="97d3f-103">API 'nin tüm API düzeltmelerinin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="97d3f-103">Gets details of all the API Revisions of an API</span></span>

## <span data-ttu-id="97d3f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97d3f-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97d3f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="97d3f-105">DESCRIPTION</span></span>
<span data-ttu-id="97d3f-106">**Get-Azapsananagementapirevision** cmdlet 'inin tüm düzeltmelerinin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="97d3f-106">The **Get-AzApiManagementApiRevision** cmdlet gets the details of all revisions of an API</span></span>

## <span data-ttu-id="97d3f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97d3f-107">EXAMPLES</span></span>

### <span data-ttu-id="97d3f-108">Örnek 1: API 'nin tüm API düzeltmelerini alma</span><span class="sxs-lookup"><span data-stu-id="97d3f-108">Example 1: Get all API Revisions of an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "5adf6fbf0faadf3ad8558065"

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

<span data-ttu-id="97d3f-109">Bu komut, belirli bir API için belirtilen API 'nin tüm API düzeltmesini alır.</span><span class="sxs-lookup"><span data-stu-id="97d3f-109">This command gets all of the API revision of specified API for particular ApiManagement Context.</span></span>

## <span data-ttu-id="97d3f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97d3f-110">PARAMETERS</span></span>

### <span data-ttu-id="97d3f-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="97d3f-111">-ApiId</span></span>
<span data-ttu-id="97d3f-112">Düzeltmeleri listelemek istediğimiz API tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="97d3f-112">API identifier whose revisions we want to list.</span></span>
<span data-ttu-id="97d3f-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="97d3f-113">This parameter is required.</span></span>

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

### <span data-ttu-id="97d3f-114">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="97d3f-114">-ApiRevision</span></span>
<span data-ttu-id="97d3f-115">Belirli API düzeltmesinin düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="97d3f-115">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="97d3f-116">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="97d3f-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="97d3f-117">-Context</span><span class="sxs-lookup"><span data-stu-id="97d3f-117">-Context</span></span>
<span data-ttu-id="97d3f-118">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="97d3f-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="97d3f-119">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="97d3f-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97d3f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97d3f-120">-DefaultProfile</span></span>
<span data-ttu-id="97d3f-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="97d3f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97d3f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97d3f-122">CommonParameters</span></span>
<span data-ttu-id="97d3f-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97d3f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97d3f-124">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="97d3f-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97d3f-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97d3f-125">INPUTS</span></span>

### <span data-ttu-id="97d3f-126">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="97d3f-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="97d3f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="97d3f-127">System.String</span></span>

## <span data-ttu-id="97d3f-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97d3f-128">OUTPUTS</span></span>

### <span data-ttu-id="97d3f-129">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapirevision</span><span class="sxs-lookup"><span data-stu-id="97d3f-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span></span>

## <span data-ttu-id="97d3f-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97d3f-130">NOTES</span></span>

## <span data-ttu-id="97d3f-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97d3f-131">RELATED LINKS</span></span>
