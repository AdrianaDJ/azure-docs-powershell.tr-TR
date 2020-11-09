---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: 833351c3abbf95eb898405f23241a20fe9affefa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322543"
---
# <span data-ttu-id="a8707-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="a8707-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="a8707-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8707-102">SYNOPSIS</span></span>
<span data-ttu-id="a8707-103">Var olan bir API 'ın yeni düzeltmesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a8707-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="a8707-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a8707-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ApiRevisionDescription <String>] [-SourceApiRevision <String>] [-ServiceUrl <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8707-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a8707-105">DESCRIPTION</span></span>

<span data-ttu-id="a8707-106">**Yeni-Azapsananagementapirevision** CMDLET 'ı API yönetim bağlamında var olan bir API Için API düzeltmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a8707-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="a8707-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a8707-107">EXAMPLES</span></span>

### <span data-ttu-id="a8707-108">Örnek 1: API için boş bir API düzeltmesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="a8707-108">Example 1: Create an empty API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"


New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"
```

<span data-ttu-id="a8707-109">Bu komut API 'ın API düzeltmesini oluşturur `2` `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="a8707-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

### <span data-ttu-id="a8707-110">Örnek 2: var olan bir API 'den bir API düzeltmesi oluşturma ve tüm işlemleri, etiketleri ve Ilkeleri kopyalama</span><span class="sxs-lookup"><span data-stu-id="a8707-110">Example 2: Create an API Revision from an Existing Api and copy All operations, tags and Policies</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5" -SourceApiRevision "1" -ServiceUrl "https://echoapi.cloudapp.net/rev4"


ApiId                         : echo-api;rev=5
Name                          : Echo API
Description                   :
ServiceUrl                    : http://echoapi.cloudapp.net/api
Path                          : echo
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 5
ApiVersion                    :
IsCurrent                     : False
IsOnline                      : False
SubscriptionRequired          : True
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               :
Id                            : /subscriptions/subid/resourceGroups/apimService1/providers/Microsoft.ApiManagement/service/sdktestapim4163/apis/echo-api;rev=5
ResourceGroupName             : apimService1
ServiceName                   : sdktestapim4163
```

<span data-ttu-id="a8707-111">Bu komut API 'ın API düzeltmesini oluşturur `5` `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="a8707-111">This command creates an API Revision `5` of the `echo-api` API.</span></span>

## <span data-ttu-id="a8707-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a8707-112">PARAMETERS</span></span>

### <span data-ttu-id="a8707-113">-Apııd</span><span class="sxs-lookup"><span data-stu-id="a8707-113">-ApiId</span></span>
<span data-ttu-id="a8707-114">Düzeltmesi oluşturulacak API tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="a8707-114">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="a8707-115">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="a8707-115">-ApiRevision</span></span>
<span data-ttu-id="a8707-116">API 'ın düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="a8707-116">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="a8707-117">-Apırevisiondescription</span><span class="sxs-lookup"><span data-stu-id="a8707-117">-ApiRevisionDescription</span></span>
<span data-ttu-id="a8707-118">API uyarlama açıklaması.</span><span class="sxs-lookup"><span data-stu-id="a8707-118">Api Revision Description.</span></span> <span data-ttu-id="a8707-119">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a8707-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="a8707-120">-Context</span><span class="sxs-lookup"><span data-stu-id="a8707-120">-Context</span></span>
<span data-ttu-id="a8707-121">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="a8707-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a8707-122">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a8707-122">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8707-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8707-123">-DefaultProfile</span></span>
<span data-ttu-id="a8707-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a8707-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8707-125">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="a8707-125">-ServiceUrl</span></span>
<span data-ttu-id="a8707-126">Arka uç hizmetindeki API 'yi kullanan Web hizmetinin URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="a8707-126">A URL of the web service exposing the API in the Backend service.</span></span> <span data-ttu-id="a8707-127">Bu URL yalnızca Azure API Yönetimi tarafından kullanılır ve genel kullanıma sunulacaktır.</span><span class="sxs-lookup"><span data-stu-id="a8707-127">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="a8707-128">1-2000 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a8707-128">Must be 1 to 2000 characters long.</span></span> <span data-ttu-id="a8707-129">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a8707-129">This parameter is required.</span></span>

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

### <span data-ttu-id="a8707-130">-Sourceapırevision</span><span class="sxs-lookup"><span data-stu-id="a8707-130">-SourceApiRevision</span></span>
<span data-ttu-id="a8707-131">Kaynak API 'sının API uyarlama tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="a8707-131">Api Revision identifier of the source API.</span></span> <span data-ttu-id="a8707-132">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a8707-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="a8707-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="a8707-133">-Confirm</span></span>
<span data-ttu-id="a8707-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a8707-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8707-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8707-135">-WhatIf</span></span>
<span data-ttu-id="a8707-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8707-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8707-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a8707-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8707-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8707-138">CommonParameters</span></span>
<span data-ttu-id="a8707-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a8707-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8707-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a8707-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8707-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a8707-141">INPUTS</span></span>

### <span data-ttu-id="a8707-142">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="a8707-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a8707-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a8707-143">System.String</span></span>

## <span data-ttu-id="a8707-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a8707-144">OUTPUTS</span></span>

### <span data-ttu-id="a8707-145">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="a8707-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="a8707-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a8707-146">NOTES</span></span>

## <span data-ttu-id="a8707-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a8707-147">RELATED LINKS</span></span>

[<span data-ttu-id="a8707-148">Get-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="a8707-148">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="a8707-149">Remove-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="a8707-149">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="a8707-150">Set-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="a8707-150">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)
