---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: f3add9f35e56d4ba6d92b8438b970ddf8c682804
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103857"
---
# <span data-ttu-id="2db28-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2db28-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="2db28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2db28-102">SYNOPSIS</span></span>
<span data-ttu-id="2db28-103">Genel veya API kapsamındaki bir API yönetim tanılaması 'nı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2db28-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="2db28-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2db28-104">SYNTAX</span></span>

### <span data-ttu-id="2db28-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2db28-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2db28-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2db28-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2db28-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="2db28-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2db28-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2db28-108">DESCRIPTION</span></span>
<span data-ttu-id="2db28-109">**Set-Azapsananagementdiagnostic** , genel veya API kapsamında yapılandırılmış olan tanılamayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2db28-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="2db28-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2db28-110">EXAMPLES</span></span>

### <span data-ttu-id="2db28-111">Örnek 1: genel kapsamda tanı değiştirme</span><span class="sxs-lookup"><span data-stu-id="2db28-111">Example 1: Modify a diagnostic at the Global scope</span></span>
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

<span data-ttu-id="2db28-112">Bu komut, 100 ile 50 arasında belirtilen tanılama örnekleme yüzdesini değiştirir</span><span class="sxs-lookup"><span data-stu-id="2db28-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

## <span data-ttu-id="2db28-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2db28-113">PARAMETERS</span></span>

### <span data-ttu-id="2db28-114">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="2db28-114">-AlwaysLog</span></span>
<span data-ttu-id="2db28-115">Hangi tür iletilerin örneklenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2db28-115">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="2db28-116">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="2db28-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="2db28-117">-Apııd</span><span class="sxs-lookup"><span data-stu-id="2db28-117">-ApiId</span></span>
<span data-ttu-id="2db28-118">Var olan API tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="2db28-118">Identifier of existing API.</span></span>
<span data-ttu-id="2db28-119">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="2db28-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="2db28-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="2db28-120">-BackendSetting</span></span>
<span data-ttu-id="2db28-121">Gelen/giden http Iletilerinin arka uca tanılama ayarı.</span><span class="sxs-lookup"><span data-stu-id="2db28-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="2db28-122">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="2db28-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="2db28-123">-Context</span><span class="sxs-lookup"><span data-stu-id="2db28-123">-Context</span></span>
<span data-ttu-id="2db28-124">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="2db28-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2db28-125">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2db28-125">This parameter is required.</span></span>

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

### <span data-ttu-id="2db28-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2db28-126">-DefaultProfile</span></span>
<span data-ttu-id="2db28-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2db28-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2db28-128">-Diagnosticıd</span><span class="sxs-lookup"><span data-stu-id="2db28-128">-DiagnosticId</span></span>
<span data-ttu-id="2db28-129">Var olan tanılayıcı tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="2db28-129">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="2db28-130">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2db28-130">This parameter is required.</span></span>

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

### <span data-ttu-id="2db28-131">-Frontenval</span><span class="sxs-lookup"><span data-stu-id="2db28-131">-FrontEndSetting</span></span>
<span data-ttu-id="2db28-132">Gelen/giden http Iletilerini ağ geçidine yönelik tanılama ayarı.</span><span class="sxs-lookup"><span data-stu-id="2db28-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="2db28-133">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="2db28-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="2db28-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2db28-134">-InputObject</span></span>
<span data-ttu-id="2db28-135">PsApiManagementDiagnostic örneği.</span><span class="sxs-lookup"><span data-stu-id="2db28-135">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="2db28-136">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2db28-136">This parameter is required.</span></span>

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

### <span data-ttu-id="2db28-137">-Loggerıd</span><span class="sxs-lookup"><span data-stu-id="2db28-137">-LoggerId</span></span>
<span data-ttu-id="2db28-138">Tanılamayı göndermek için günlükçü tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="2db28-138">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="2db28-139">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2db28-139">This parameter is required.</span></span>

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

### <span data-ttu-id="2db28-140">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2db28-140">-PassThru</span></span>
<span data-ttu-id="2db28-141">Eğer belirtildiyse, set Diagnostic 'i temsil eden Microsoft. Azure. Commands. Apsananamedimentdiagnostic türü</span><span class="sxs-lookup"><span data-stu-id="2db28-141">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="2db28-142">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2db28-142">-ResourceId</span></span>
<span data-ttu-id="2db28-143">Tanılama veya API tanısı kolu RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="2db28-143">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="2db28-144">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2db28-144">This parameter is required.</span></span>

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

### <span data-ttu-id="2db28-145">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="2db28-145">-SamplingSetting</span></span>
<span data-ttu-id="2db28-146">Tanılama ayarı.</span><span class="sxs-lookup"><span data-stu-id="2db28-146">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="2db28-147">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="2db28-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="2db28-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="2db28-148">-Confirm</span></span>
<span data-ttu-id="2db28-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2db28-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2db28-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2db28-150">-WhatIf</span></span>
<span data-ttu-id="2db28-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2db28-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2db28-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2db28-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2db28-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2db28-153">CommonParameters</span></span>
<span data-ttu-id="2db28-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2db28-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2db28-155">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2db28-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2db28-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2db28-156">INPUTS</span></span>

### <span data-ttu-id="2db28-157">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="2db28-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2db28-158">System. String</span><span class="sxs-lookup"><span data-stu-id="2db28-158">System.String</span></span>

### <span data-ttu-id="2db28-159">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementdiagnostic</span><span class="sxs-lookup"><span data-stu-id="2db28-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="2db28-160">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsampsetting</span><span class="sxs-lookup"><span data-stu-id="2db28-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="2db28-161">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementıngesinedınoçıkartma ayarı</span><span class="sxs-lookup"><span data-stu-id="2db28-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="2db28-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2db28-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2db28-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2db28-163">OUTPUTS</span></span>

### <span data-ttu-id="2db28-164">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementdiagnostic</span><span class="sxs-lookup"><span data-stu-id="2db28-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="2db28-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2db28-165">NOTES</span></span>

## <span data-ttu-id="2db28-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2db28-166">RELATED LINKS</span></span>
