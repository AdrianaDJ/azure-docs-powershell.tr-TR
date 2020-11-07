---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: f5cf0d9f80b15f178cb701b4474fa5dc13d957eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753422"
---
# <span data-ttu-id="157ed-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="157ed-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="157ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="157ed-102">SYNOPSIS</span></span>
<span data-ttu-id="157ed-103">Arka uç güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="157ed-103">Updates a Backend.</span></span>

## <span data-ttu-id="157ed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="157ed-104">SYNTAX</span></span>

### <span data-ttu-id="157ed-105">ContextParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="157ed-105">ContextParameterSet (Default)</span></span>
```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="157ed-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="157ed-106">ByInputObject</span></span>
```
Set-AzApiManagementBackend -InputObject <PsApiManagementBackend> [-Protocol <String>] [-Url <String>]
 [-ResourceId <String>] [-Title <String>] [-Description <String>] [-SkipCertificateChainValidation <Boolean>]
 [-SkipCertificateNameValidation <Boolean>] [-Credential <PsApiManagementBackendCredential>]
 [-Proxy <PsApiManagementBackendProxy>] [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="157ed-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="157ed-107">DESCRIPTION</span></span>
<span data-ttu-id="157ed-108">API yönetiminde varolan bir arka uç 'Yi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="157ed-108">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="157ed-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="157ed-109">EXAMPLES</span></span>

### <span data-ttu-id="157ed-110">Arka uç 123 'in açıklamasını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="157ed-110">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="157ed-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="157ed-111">PARAMETERS</span></span>

### <span data-ttu-id="157ed-112">-Backenmuydunuz</span><span class="sxs-lookup"><span data-stu-id="157ed-112">-BackendId</span></span>
<span data-ttu-id="157ed-113">Yeni arka ucun tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="157ed-113">Identifier of new backend.</span></span>
<span data-ttu-id="157ed-114">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="157ed-114">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="157ed-115">-Context</span><span class="sxs-lookup"><span data-stu-id="157ed-115">-Context</span></span>
<span data-ttu-id="157ed-116">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="157ed-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="157ed-117">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="157ed-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="157ed-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="157ed-118">-Credential</span></span>
<span data-ttu-id="157ed-119">Arka uca konuşurken kullanılması gereken kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="157ed-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="157ed-120">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="157ed-120">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="157ed-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="157ed-121">-DefaultProfile</span></span>
<span data-ttu-id="157ed-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="157ed-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="157ed-123">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="157ed-123">-Description</span></span>
<span data-ttu-id="157ed-124">Arka uç açıklaması.</span><span class="sxs-lookup"><span data-stu-id="157ed-124">Backend Description.</span></span>
<span data-ttu-id="157ed-125">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="157ed-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="157ed-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="157ed-126">-InputObject</span></span>
<span data-ttu-id="157ed-127">Psapimanagementarka uç örneği.</span><span class="sxs-lookup"><span data-stu-id="157ed-127">Instance of PsApiManagementBackend.</span></span> <span data-ttu-id="157ed-128">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="157ed-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="157ed-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="157ed-129">-PassThru</span></span>
<span data-ttu-id="157ed-130">Bu cmdlet 'in değiştirdiği  **Psapimanagementarka uç** değerini döndüren anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="157ed-130">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="157ed-131">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="157ed-131">-Protocol</span></span>
<span data-ttu-id="157ed-132">Arka uç Iletişim Protokolü (http veya SOAP).</span><span class="sxs-lookup"><span data-stu-id="157ed-132">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="157ed-133">Bu parametre isteğe bağlıdır</span><span class="sxs-lookup"><span data-stu-id="157ed-133">This parameter is optional</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: http, soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="157ed-134">-Proxy</span><span class="sxs-lookup"><span data-stu-id="157ed-134">-Proxy</span></span>
<span data-ttu-id="157ed-135">İstek arka uca gönderilirken kullanılacak proxy sunucusu ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="157ed-135">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="157ed-136">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="157ed-136">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="157ed-137">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="157ed-137">-ResourceId</span></span>
<span data-ttu-id="157ed-138">Dış sistemdeki kaynağın yönetim URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="157ed-138">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="157ed-139">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="157ed-139">This parameter is optional.</span></span>
<span data-ttu-id="157ed-140">Bu URL, mantık uygulamalarının, Işlev uygulamalarının veya API uygulamalarının ARM kaynak kimliği olabilir.</span><span class="sxs-lookup"><span data-stu-id="157ed-140">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="157ed-141">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="157ed-141">-ServiceFabricCluster</span></span>
<span data-ttu-id="157ed-142">Hizmet yapısı kümesi arka uç ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="157ed-142">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="157ed-143">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="157ed-143">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="157ed-144">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="157ed-144">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="157ed-145">Arka uca konuşurken sertifika zinciri doğrulamasının atlanıp atlanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="157ed-145">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="157ed-146">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="157ed-146">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="157ed-147">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="157ed-147">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="157ed-148">Arka uca konuşurken sertifika adı doğrulamasının atlanıp atlanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="157ed-148">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="157ed-149">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="157ed-149">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="157ed-150">-Başlık</span><span class="sxs-lookup"><span data-stu-id="157ed-150">-Title</span></span>
<span data-ttu-id="157ed-151">Arka uç başlığı.</span><span class="sxs-lookup"><span data-stu-id="157ed-151">Backend Title.</span></span>
<span data-ttu-id="157ed-152">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="157ed-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="157ed-153">-URL</span><span class="sxs-lookup"><span data-stu-id="157ed-153">-Url</span></span>
<span data-ttu-id="157ed-154">Arka uç için çalışma zamanı URL 'Si.</span><span class="sxs-lookup"><span data-stu-id="157ed-154">Runtime Url for the Backend.</span></span>
<span data-ttu-id="157ed-155">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="157ed-155">This parameter is optional.</span></span>

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

### <span data-ttu-id="157ed-156">-Onay</span><span class="sxs-lookup"><span data-stu-id="157ed-156">-Confirm</span></span>
<span data-ttu-id="157ed-157">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="157ed-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="157ed-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="157ed-158">-WhatIf</span></span>
<span data-ttu-id="157ed-159">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="157ed-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="157ed-160">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="157ed-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="157ed-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="157ed-161">CommonParameters</span></span>
<span data-ttu-id="157ed-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="157ed-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="157ed-163">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="157ed-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="157ed-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="157ed-164">INPUTS</span></span>

### <span data-ttu-id="157ed-165">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="157ed-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="157ed-166">System. String</span><span class="sxs-lookup"><span data-stu-id="157ed-166">System.String</span></span>

### <span data-ttu-id="157ed-167">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="157ed-167">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="157ed-168">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="157ed-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="157ed-169">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="157ed-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="157ed-170">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementservicefabric</span><span class="sxs-lookup"><span data-stu-id="157ed-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="157ed-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="157ed-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="157ed-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="157ed-172">OUTPUTS</span></span>

### <span data-ttu-id="157ed-173">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementarka uç</span><span class="sxs-lookup"><span data-stu-id="157ed-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="157ed-174">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="157ed-174">NOTES</span></span>

## <span data-ttu-id="157ed-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="157ed-175">RELATED LINKS</span></span>

[<span data-ttu-id="157ed-176">Get-Azapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="157ed-176">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="157ed-177">Yeni-Azsız arka uç</span><span class="sxs-lookup"><span data-stu-id="157ed-177">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="157ed-178">Yeni-Azapsananagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="157ed-178">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="157ed-179">Yeni-Azapsananagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="157ed-179">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="157ed-180">Remove-Azapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="157ed-180">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
