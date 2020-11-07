---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
ms.openlocfilehash: 2ff4660a0e8f4929e8f79c20a8e42e0deac11f3c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753593"
---
# <span data-ttu-id="af967-101">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="af967-101">Get-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="af967-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af967-102">SYNOPSIS</span></span>
<span data-ttu-id="af967-103">Hizmet düzeyinde veya API düzeyinde yapılandırılmış tanı ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="af967-103">Get details of the Diagnostic configured at the service level or the Api Level.</span></span> <span data-ttu-id="af967-104">Tanılama, API yönetim ağ geçidinden istek/yanıtları günlüğe kaydetmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="af967-104">Diagnostics are used to log requests/responses from Api Management gateway.</span></span>

## <span data-ttu-id="af967-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af967-105">SYNTAX</span></span>

### <span data-ttu-id="af967-106">ContextParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="af967-106">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-DiagnosticId <String>] [-ApiId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af967-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="af967-107">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementDiagnostic -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af967-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="af967-108">DESCRIPTION</span></span>
<span data-ttu-id="af967-109">**Get-Azapsananagementdiagnostic** , belirli bir kapsamda API Yönetim hizmetinde yapılandırılan tanılamaların ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="af967-109">The **Get-AzApiManagementDiagnostic** gets details of the diagnostics configured in the Api management service at a given scope.</span></span>

## <span data-ttu-id="af967-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af967-110">EXAMPLES</span></span>

### <span data-ttu-id="af967-111">Örnek 1: kiracı kapsamında yapılandırılmış tüm tanılamayı alın.</span><span class="sxs-lookup"><span data-stu-id="af967-111">Example 1: Get all the diagnostic configured at the tenant scope.</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext

DiagnosticId                 : applicationinsights
ApiId                        :
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso

DiagnosticId                 : azuremonitor
ApiId                        :
AlwaysLog                    :
LoggerId                     : azuremonitor
EnableHttpCorrelationHeaders :
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               : 
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/azuremonitor
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="af967-112">Bu komut, API Yönetim hizmetinde yapılandırılmış tüm tanılamayı alır.</span><span class="sxs-lookup"><span data-stu-id="af967-112">This command gets all the diagnostics configured in the Api Management service.</span></span>

### <span data-ttu-id="af967-113">Örnek 2: API kapsamında yapılandırılmış tüm tanılamayı alma</span><span class="sxs-lookup"><span data-stu-id="af967-113">Example 2: Get all the diagnostics configured at the Api scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext -ApiId "echo-api"

DiagnosticId                 : applicationinsights
ApiId                        : echo-api
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
BackendSetting               : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="af967-114">Bu komut API kapsamında yapılandırılmış tüm tanılamayı alır `echo-api`</span><span class="sxs-lookup"><span data-stu-id="af967-114">This command gets all the diagnostics configured at the `echo-api` Api scope</span></span>

### <span data-ttu-id="af967-115">Örnek 3: bir kimlikle belirtilen API kapsam tanılaması 'nı alma</span><span class="sxs-lookup"><span data-stu-id="af967-115">Example 3: Get the API-scope diagnostic specified by an Id</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext -ApiId "echo-api" -DiagnosticId "applicationinsights"

DiagnosticId                 : applicationinsights
ApiId                        : echo-api
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="af967-116">Bu komut `applicationinsights` API 'de yapılandırılan tanılamaları alır `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="af967-116">This command gets the `applicationinsights` diagnostics configured in api `echo-api`.</span></span>

## <span data-ttu-id="af967-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af967-117">PARAMETERS</span></span>

### <span data-ttu-id="af967-118">-Apııd</span><span class="sxs-lookup"><span data-stu-id="af967-118">-ApiId</span></span>
<span data-ttu-id="af967-119">Var olan API tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="af967-119">Identifier of existing API.</span></span>
<span data-ttu-id="af967-120">Belirtilmişse API kapsam tanılaması döndürür.</span><span class="sxs-lookup"><span data-stu-id="af967-120">If specified will return API-scope diagnostic.</span></span>
<span data-ttu-id="af967-121">Bu parametreler gereklidir.</span><span class="sxs-lookup"><span data-stu-id="af967-121">This parameters is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af967-122">-Context</span><span class="sxs-lookup"><span data-stu-id="af967-122">-Context</span></span>
<span data-ttu-id="af967-123">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="af967-123">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="af967-124">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="af967-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af967-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af967-125">-DefaultProfile</span></span>
<span data-ttu-id="af967-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af967-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af967-127">-Diagnosticıd</span><span class="sxs-lookup"><span data-stu-id="af967-127">-DiagnosticId</span></span>
<span data-ttu-id="af967-128">Var olan tanılayıcı tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="af967-128">Identifier of existing diagnostic.</span></span>
<span data-ttu-id="af967-129">Belirtilmişse ürün kapsam ilkesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="af967-129">If specified will return product-scope policy.</span></span>
<span data-ttu-id="af967-130">Bu parametreler isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="af967-130">This parameters is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af967-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="af967-131">-ResourceId</span></span>
<span data-ttu-id="af967-132">Bir tanılama veya API tanısı kolu kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="af967-132">Arm Resource Identifier of a Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="af967-133">Belirtilmişse tanımlayıcı tarafından tanılama bulmayı dener.</span><span class="sxs-lookup"><span data-stu-id="af967-133">If specified will try to find diagnostic by the identifier.</span></span> <span data-ttu-id="af967-134">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="af967-134">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af967-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af967-135">CommonParameters</span></span>
<span data-ttu-id="af967-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af967-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af967-137">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="af967-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af967-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af967-138">INPUTS</span></span>

### <span data-ttu-id="af967-139">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="af967-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="af967-140">System. String</span><span class="sxs-lookup"><span data-stu-id="af967-140">System.String</span></span>

## <span data-ttu-id="af967-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af967-141">OUTPUTS</span></span>

### <span data-ttu-id="af967-142">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementdiagnostic</span><span class="sxs-lookup"><span data-stu-id="af967-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="af967-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af967-143">NOTES</span></span>

## <span data-ttu-id="af967-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af967-144">RELATED LINKS</span></span>
