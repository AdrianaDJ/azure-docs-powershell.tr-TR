---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: c646e7f39b5149803161bfc7b97ed64b5517dd9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108535"
---
# <span data-ttu-id="075eb-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="075eb-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="075eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="075eb-102">SYNOPSIS</span></span>
<span data-ttu-id="075eb-103">Genel veya API kapsamındaki bir API yönetim tanılaması 'nı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="075eb-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="075eb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="075eb-104">SYNTAX</span></span>

### <span data-ttu-id="075eb-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="075eb-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="075eb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="075eb-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="075eb-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="075eb-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="075eb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="075eb-108">DESCRIPTION</span></span>
<span data-ttu-id="075eb-109">**Set-Azapsananagementdiagnostic** , genel veya API kapsamında yapılandırılmış olan tanılamayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="075eb-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="075eb-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="075eb-110">EXAMPLES</span></span>

### <span data-ttu-id="075eb-111">Örnek 1: genel kapsamda tanı değiştirme</span><span class="sxs-lookup"><span data-stu-id="075eb-111">Example 1: Modify a diagnostic at the Global scope</span></span>
```powershell
PS c:\> $context =New-AzApiManagementContext -ResourceGroupName Api-Default-WestUS -ServiceName contoso
PS c:\> $diagnostic=Get-AzApiManagementDiagnostic -Context $context -DiagnosticId "applicationinsights"
PS c:\> $diagnostic

DiagnosticId      : applicationinsights
AlwaysLog         : allErrors
LoggerId          : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/loggers/backendapisachinc
Sampling          : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
Frontend          :
Backend           :
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso


PS c:\> $diagnostic.Sampling

SamplingType Percentage
------------ ----------
fixed               100

PS c:\> $diagnostic.Sampling.Percentage = 50
PS c:\> $diagnostic.Sampling

SamplingType Percentage
------------ ----------
fixed                50

PS c:\> Set-AzApiManagementDiagnostic -InputObject $diagnostic
```

<span data-ttu-id="075eb-112">Bu komut, 100 ile 50 arasında belirtilen tanılama örnekleme yüzdesini değiştirir</span><span class="sxs-lookup"><span data-stu-id="075eb-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

### <span data-ttu-id="075eb-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="075eb-113">Example 2</span></span>

<span data-ttu-id="075eb-114">Genel veya API kapsamındaki bir API yönetim tanılaması 'nı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="075eb-114">Modifies an API Management diagnostic at the Global or Api scope.</span></span> <span data-ttu-id="075eb-115">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="075eb-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementDiagnostic -AlwaysLog allErrors -ApiId '0001' -Context <PsApiManagementContext> -DiagnosticId 'applicationinsights' -LoggerId 'Logger123' -SamplingSetting <PsApiManagementSamplingSetting>
```

## <span data-ttu-id="075eb-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="075eb-116">PARAMETERS</span></span>

### <span data-ttu-id="075eb-117">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="075eb-117">-AlwaysLog</span></span>
<span data-ttu-id="075eb-118">Hangi tür iletilerin örneklenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="075eb-118">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="075eb-119">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="075eb-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="075eb-120">-Apııd</span><span class="sxs-lookup"><span data-stu-id="075eb-120">-ApiId</span></span>
<span data-ttu-id="075eb-121">Var olan API tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="075eb-121">Identifier of existing API.</span></span>
<span data-ttu-id="075eb-122">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="075eb-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="075eb-123">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="075eb-123">-BackendSetting</span></span>
<span data-ttu-id="075eb-124">Gelen/giden http Iletilerinin arka uca tanılama ayarı.</span><span class="sxs-lookup"><span data-stu-id="075eb-124">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="075eb-125">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="075eb-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="075eb-126">-Context</span><span class="sxs-lookup"><span data-stu-id="075eb-126">-Context</span></span>
<span data-ttu-id="075eb-127">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="075eb-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="075eb-128">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="075eb-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="075eb-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="075eb-129">-DefaultProfile</span></span>
<span data-ttu-id="075eb-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="075eb-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="075eb-131">-Diagnosticıd</span><span class="sxs-lookup"><span data-stu-id="075eb-131">-DiagnosticId</span></span>
<span data-ttu-id="075eb-132">Var olan tanılayıcı tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="075eb-132">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="075eb-133">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="075eb-133">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="075eb-134">-Frontenval</span><span class="sxs-lookup"><span data-stu-id="075eb-134">-FrontEndSetting</span></span>
<span data-ttu-id="075eb-135">Gelen/giden http Iletilerini ağ geçidine yönelik tanılama ayarı.</span><span class="sxs-lookup"><span data-stu-id="075eb-135">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="075eb-136">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="075eb-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="075eb-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="075eb-137">-InputObject</span></span>
<span data-ttu-id="075eb-138">PsApiManagementDiagnostic örneği.</span><span class="sxs-lookup"><span data-stu-id="075eb-138">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="075eb-139">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="075eb-139">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="075eb-140">-Loggerıd</span><span class="sxs-lookup"><span data-stu-id="075eb-140">-LoggerId</span></span>
<span data-ttu-id="075eb-141">Tanılamayı göndermek için günlükçü tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="075eb-141">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="075eb-142">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="075eb-142">This parameter is required.</span></span>

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

### <span data-ttu-id="075eb-143">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="075eb-143">-PassThru</span></span>
<span data-ttu-id="075eb-144">Eğer belirtildiyse, set Diagnostic 'i temsil eden Microsoft. Azure. Commands. Apsananamedimentdiagnostic türü</span><span class="sxs-lookup"><span data-stu-id="075eb-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="075eb-145">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="075eb-145">-ResourceId</span></span>
<span data-ttu-id="075eb-146">Tanılama veya API tanısı kolu RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="075eb-146">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="075eb-147">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="075eb-147">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="075eb-148">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="075eb-148">-SamplingSetting</span></span>
<span data-ttu-id="075eb-149">Tanılama ayarı.</span><span class="sxs-lookup"><span data-stu-id="075eb-149">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="075eb-150">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="075eb-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="075eb-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="075eb-151">-Confirm</span></span>
<span data-ttu-id="075eb-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="075eb-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="075eb-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="075eb-153">-WhatIf</span></span>
<span data-ttu-id="075eb-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="075eb-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="075eb-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="075eb-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="075eb-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="075eb-156">CommonParameters</span></span>
<span data-ttu-id="075eb-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="075eb-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="075eb-158">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="075eb-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="075eb-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="075eb-159">INPUTS</span></span>

### <span data-ttu-id="075eb-160">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="075eb-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="075eb-161">System. String</span><span class="sxs-lookup"><span data-stu-id="075eb-161">System.String</span></span>

### <span data-ttu-id="075eb-162">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementdiagnostic</span><span class="sxs-lookup"><span data-stu-id="075eb-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="075eb-163">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsampsetting</span><span class="sxs-lookup"><span data-stu-id="075eb-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="075eb-164">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementıngesinedınoçıkartma ayarı</span><span class="sxs-lookup"><span data-stu-id="075eb-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="075eb-165">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="075eb-165">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="075eb-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="075eb-166">OUTPUTS</span></span>

### <span data-ttu-id="075eb-167">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementdiagnostic</span><span class="sxs-lookup"><span data-stu-id="075eb-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="075eb-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="075eb-168">NOTES</span></span>

## <span data-ttu-id="075eb-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="075eb-169">RELATED LINKS</span></span>
