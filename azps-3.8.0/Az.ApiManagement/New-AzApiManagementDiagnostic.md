---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
ms.openlocfilehash: 1c3bea7efffe066ec85b44ec9e5f0f7c222efcf8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097719"
---
# <span data-ttu-id="6bd75-101">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6bd75-101">New-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="6bd75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bd75-102">SYNOPSIS</span></span>
<span data-ttu-id="6bd75-103">Genel kapsamda veya API kapsamında yeni bir tanılama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6bd75-103">Creates a new diagnostics at the Global scope or Api Scope.</span></span>

## <span data-ttu-id="6bd75-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6bd75-104">SYNTAX</span></span>

```
New-AzApiManagementDiagnostic -Context <PsApiManagementContext> -LoggerId <String> [-DiagnosticId <String>]
 [-AlwaysLog <String>] [-ApiId <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bd75-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6bd75-105">DESCRIPTION</span></span>
<span data-ttu-id="6bd75-106">**New-Azapsananagementdiagnostic** cmdlet 'i genel kapsamda veya belirli bir API kapsamında bir tanılama varlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6bd75-106">The cmdlet **New-AzApiManagementDiagnostic** creates a diagnostic entity either at Global scope or specific Api scope.</span></span>

## <span data-ttu-id="6bd75-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6bd75-107">EXAMPLES</span></span>

### <span data-ttu-id="6bd75-108">Örnek 1: yeni bir genel kapsam tanılaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="6bd75-108">Example 1 : Create a new Global scope Diagnostic</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS D:\github\azure-powershell> $logger = Get-AzApiManagementLogger -Context $context -LoggerId "backendapisachinc"
PS D:\github\azure-powershell> $samplingsetting = New-AzApiManagementSamplingSetting -SamplingType fixed -SamplingPercentage 100
PS D:\github\azure-powershell> New-AzApiManagementDiagnostic -LoggerId $logger.LoggerId -Context $context -AlwaysLog allErrors -SamplingSetting $samplingSetting  -DiagnosticId "applicationinsights"

DiagnosticId                 : applicationinsights
ApiId                        :
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUs/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUs
ServiceName                  : contoso
```

<span data-ttu-id="6bd75-109">Bu örnek genel kapsamda bir tanılama varlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6bd75-109">This example create a diagnostic entity at the Global Scope.</span></span>

### <span data-ttu-id="6bd75-110">Örnek 2: API kapsamında tanılama oluşturma</span><span class="sxs-lookup"><span data-stu-id="6bd75-110">Example 2: Create a diagnostic at Api scope</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS D:\github\azure-powershell> $logger = Get-AzApiManagementLogger -Context $context -LoggerId azuremonitor
PS D:\github\azure-powershell> $samplingsetting = New-AzApiManagementSamplingSetting -SamplingType fixed -SamplingPercentage 100
PS D:\github\azure-powershell> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -HeadersToLog 'Content-Type', 'User-Agent' -BodyBytesToLog 100
PS D:\github\azure-powershell> $pipelineDiagnostic = New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic
PS D:\github\azure-powershell> New-AzApiManagementDiagnostic -LoggerId $logger.LoggerId -Context $context -ApiId httpbin -AlwaysLog allErrors -SamplingSetting $samplingsetting -FrontEndSetting $pipelineDiagnostic -BackendSetting $pipelineDiagnostic -DiagnosticId azuremonitor

DiagnosticId                 : azuremonitor
ApiId                        : httpbin
AlwaysLog                    : allErrors
LoggerId                     : azuremonitor
EnableHttpCorrelationHeaders :
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
BackendSetting               : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/httpbin/diagnostics/azuremonitor      
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="6bd75-111">Yukarıdaki örnekte, bir API `httpbin` üst bilgisini ve 100 baytlarını `azuremonitor` günlükçü</span><span class="sxs-lookup"><span data-stu-id="6bd75-111">The example above create a diagnostic for the API `httpbin` to log the Header and 100 Bytes of Body to `azuremonitor` logger.</span></span>

## <span data-ttu-id="6bd75-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6bd75-112">PARAMETERS</span></span>

### <span data-ttu-id="6bd75-113">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="6bd75-113">-AlwaysLog</span></span>
<span data-ttu-id="6bd75-114">Hangi tür iletilerin örneklenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bd75-114">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="6bd75-115">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="6bd75-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="6bd75-116">-Apııd</span><span class="sxs-lookup"><span data-stu-id="6bd75-116">-ApiId</span></span>
<span data-ttu-id="6bd75-117">Var olan API tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="6bd75-117">Identifier of existing API.</span></span>
<span data-ttu-id="6bd75-118">Belirtilmişse API kapsam ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6bd75-118">If specified will set API-scope policy.</span></span>
<span data-ttu-id="6bd75-119">Bu parametreler gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6bd75-119">This parameters is required.</span></span>

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

### <span data-ttu-id="6bd75-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="6bd75-120">-BackendSetting</span></span>
<span data-ttu-id="6bd75-121">Gelen/giden http Iletilerinin arka uca tanılama ayarı.</span><span class="sxs-lookup"><span data-stu-id="6bd75-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="6bd75-122">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="6bd75-122">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd75-123">-Context</span><span class="sxs-lookup"><span data-stu-id="6bd75-123">-Context</span></span>
<span data-ttu-id="6bd75-124">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="6bd75-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6bd75-125">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6bd75-125">This parameter is required.</span></span>

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

### <span data-ttu-id="6bd75-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bd75-126">-DefaultProfile</span></span>
<span data-ttu-id="6bd75-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6bd75-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bd75-128">-Diagnosticıd</span><span class="sxs-lookup"><span data-stu-id="6bd75-128">-DiagnosticId</span></span>
<span data-ttu-id="6bd75-129">Tanılama varlığının tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="6bd75-129">Identifier of the diagnostics entity.</span></span>
<span data-ttu-id="6bd75-130">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="6bd75-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="6bd75-131">-Frontenval</span><span class="sxs-lookup"><span data-stu-id="6bd75-131">-FrontEndSetting</span></span>
<span data-ttu-id="6bd75-132">Gelen/giden http Iletilerini ağ geçidine yönelik tanılama ayarı.</span><span class="sxs-lookup"><span data-stu-id="6bd75-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="6bd75-133">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="6bd75-133">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd75-134">-Loggerıd</span><span class="sxs-lookup"><span data-stu-id="6bd75-134">-LoggerId</span></span>
<span data-ttu-id="6bd75-135">Tanılamayı göndermek için günlükçü tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="6bd75-135">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="6bd75-136">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6bd75-136">This parameter is required.</span></span>

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

### <span data-ttu-id="6bd75-137">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="6bd75-137">-SamplingSetting</span></span>
<span data-ttu-id="6bd75-138">Tanılama ayarı.</span><span class="sxs-lookup"><span data-stu-id="6bd75-138">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="6bd75-139">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="6bd75-139">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd75-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="6bd75-140">-Confirm</span></span>
<span data-ttu-id="6bd75-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6bd75-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bd75-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bd75-142">-WhatIf</span></span>
<span data-ttu-id="6bd75-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6bd75-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bd75-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6bd75-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bd75-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bd75-145">CommonParameters</span></span>
<span data-ttu-id="6bd75-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6bd75-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bd75-147">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6bd75-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bd75-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6bd75-148">INPUTS</span></span>

### <span data-ttu-id="6bd75-149">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="6bd75-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6bd75-150">System. String</span><span class="sxs-lookup"><span data-stu-id="6bd75-150">System.String</span></span>

### <span data-ttu-id="6bd75-151">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsampsetting</span><span class="sxs-lookup"><span data-stu-id="6bd75-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="6bd75-152">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementıngesinedınoçıkartma ayarı</span><span class="sxs-lookup"><span data-stu-id="6bd75-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="6bd75-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6bd75-153">OUTPUTS</span></span>

### <span data-ttu-id="6bd75-154">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementdiagnostic</span><span class="sxs-lookup"><span data-stu-id="6bd75-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="6bd75-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6bd75-155">NOTES</span></span>

## <span data-ttu-id="6bd75-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6bd75-156">RELATED LINKS</span></span>

[<span data-ttu-id="6bd75-157">Get-Azapsananagementdiagnostic</span><span class="sxs-lookup"><span data-stu-id="6bd75-157">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="6bd75-158">Remove-Azapsananagementdiagnostic</span><span class="sxs-lookup"><span data-stu-id="6bd75-158">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="6bd75-159">Set-Azapsananagementdiagnostic</span><span class="sxs-lookup"><span data-stu-id="6bd75-159">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="6bd75-160">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6bd75-160">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)

[<span data-ttu-id="6bd75-161">Yeni-Azapsanana,</span><span class="sxs-lookup"><span data-stu-id="6bd75-161">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)