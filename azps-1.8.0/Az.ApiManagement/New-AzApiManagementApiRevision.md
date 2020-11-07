---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: 81a80acdfb89f30cc1add6b1cfc10bcd7d745dfd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751124"
---
# <span data-ttu-id="7baed-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="7baed-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="7baed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7baed-102">SYNOPSIS</span></span>
<span data-ttu-id="7baed-103">Var olan bir API 'ın yeni düzeltmesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7baed-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="7baed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7baed-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7baed-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7baed-105">DESCRIPTION</span></span>

<span data-ttu-id="7baed-106">**Yeni-Azapsananagementapirevision** CMDLET 'ı API yönetim bağlamında var olan bir API Için API düzeltmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7baed-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="7baed-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7baed-107">EXAMPLES</span></span>

### <span data-ttu-id="7baed-108">Örnek 1: API için API düzeltmesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="7baed-108">Example 1: Create an API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $ApiMgmtContext  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6


ApiId                         : 5adf6fbf0faadf3ad8558065;rev=6
Name                          : httpbin.org
Description                   : API Management facade for a very handy and free online HTTP tool.
ServiceUrl                    : https://httpbin.org/
Path                          : httpbin
ApiType                       : http
Protocols                     : {Http, Https}
AuthorizationServerId         : contoso-oauth
AuthorizationScope            : contoso-oauth
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 6
ApiVersion                    : v1
IsCurrent                     : False
IsOnline                      : False
Id                            : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065;rev=6
ResourceGroupName             : Api-Default-WestUS
ServiceName                   : contoso
```

<span data-ttu-id="7baed-109">Bu komut API 'ın API düzeltmesini oluşturur `2` `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="7baed-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

## <span data-ttu-id="7baed-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7baed-110">PARAMETERS</span></span>

### <span data-ttu-id="7baed-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="7baed-111">-ApiId</span></span>
<span data-ttu-id="7baed-112">Düzeltmesi oluşturulacak API tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="7baed-112">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="7baed-113">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="7baed-113">-ApiRevision</span></span>
<span data-ttu-id="7baed-114">API 'ın düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="7baed-114">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="7baed-115">-Context</span><span class="sxs-lookup"><span data-stu-id="7baed-115">-Context</span></span>
<span data-ttu-id="7baed-116">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="7baed-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7baed-117">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="7baed-117">This parameter is required.</span></span>

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

### <span data-ttu-id="7baed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7baed-118">-DefaultProfile</span></span>
<span data-ttu-id="7baed-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7baed-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7baed-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="7baed-120">-Confirm</span></span>
<span data-ttu-id="7baed-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7baed-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7baed-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7baed-122">-WhatIf</span></span>
<span data-ttu-id="7baed-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7baed-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7baed-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7baed-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7baed-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7baed-125">CommonParameters</span></span>
<span data-ttu-id="7baed-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7baed-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7baed-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7baed-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7baed-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7baed-128">INPUTS</span></span>

### <span data-ttu-id="7baed-129">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="7baed-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7baed-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7baed-130">System.String</span></span>

## <span data-ttu-id="7baed-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7baed-131">OUTPUTS</span></span>

### <span data-ttu-id="7baed-132">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="7baed-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="7baed-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7baed-133">NOTES</span></span>

## <span data-ttu-id="7baed-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7baed-134">RELATED LINKS</span></span>

[<span data-ttu-id="7baed-135">Get-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="7baed-135">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="7baed-136">Remove-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="7baed-136">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="7baed-137">Set-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="7baed-137">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)
