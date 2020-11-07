---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: ce27a151ebb6d778ed647fb81909c44c11edbf8e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917703"
---
# <span data-ttu-id="e8700-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e8700-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="e8700-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8700-102">SYNOPSIS</span></span>
<span data-ttu-id="e8700-103">Arka uç güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e8700-103">Updates a Backend.</span></span>

## <span data-ttu-id="e8700-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8700-104">SYNTAX</span></span>

```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8700-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8700-105">DESCRIPTION</span></span>
<span data-ttu-id="e8700-106">API yönetiminde varolan bir arka uç 'Yi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e8700-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="e8700-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8700-107">EXAMPLES</span></span>

### <span data-ttu-id="e8700-108">Arka uç 123 'in açıklamasını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="e8700-108">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="e8700-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8700-109">PARAMETERS</span></span>

### <span data-ttu-id="e8700-110">-Backenmuydunuz</span><span class="sxs-lookup"><span data-stu-id="e8700-110">-BackendId</span></span>
<span data-ttu-id="e8700-111">Yeni arka ucun tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="e8700-111">Identifier of new backend.</span></span>
<span data-ttu-id="e8700-112">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e8700-112">This parameter is required.</span></span>

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

### <span data-ttu-id="e8700-113">-Context</span><span class="sxs-lookup"><span data-stu-id="e8700-113">-Context</span></span>
<span data-ttu-id="e8700-114">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="e8700-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e8700-115">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e8700-115">This parameter is required.</span></span>

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

### <span data-ttu-id="e8700-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="e8700-116">-Credential</span></span>
<span data-ttu-id="e8700-117">Arka uca konuşurken kullanılması gereken kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="e8700-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="e8700-118">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e8700-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="e8700-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8700-119">-DefaultProfile</span></span>
<span data-ttu-id="e8700-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e8700-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8700-121">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="e8700-121">-Description</span></span>
<span data-ttu-id="e8700-122">Arka uç açıklaması.</span><span class="sxs-lookup"><span data-stu-id="e8700-122">Backend Description.</span></span>
<span data-ttu-id="e8700-123">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e8700-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="e8700-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e8700-124">-PassThru</span></span>
<span data-ttu-id="e8700-125">Bu cmdlet 'in değiştirdiği  **Psapimanagementarka uç** değerini döndüren anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="e8700-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e8700-126">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="e8700-126">-Protocol</span></span>
<span data-ttu-id="e8700-127">Arka uç Iletişim Protokolü (http veya SOAP).</span><span class="sxs-lookup"><span data-stu-id="e8700-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="e8700-128">Bu parametre isteğe bağlıdır</span><span class="sxs-lookup"><span data-stu-id="e8700-128">This parameter is optional</span></span>

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

### <span data-ttu-id="e8700-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="e8700-129">-Proxy</span></span>
<span data-ttu-id="e8700-130">İstek arka uca gönderilirken kullanılacak proxy sunucusu ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="e8700-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="e8700-131">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e8700-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="e8700-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e8700-132">-ResourceId</span></span>
<span data-ttu-id="e8700-133">Dış sistemdeki kaynağın yönetim URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="e8700-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="e8700-134">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e8700-134">This parameter is optional.</span></span>
<span data-ttu-id="e8700-135">Bu URL, mantık uygulamalarının, Işlev uygulamalarının veya API uygulamalarının ARM kaynak kimliği olabilir.</span><span class="sxs-lookup"><span data-stu-id="e8700-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="e8700-136">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="e8700-136">-ServiceFabricCluster</span></span>
<span data-ttu-id="e8700-137">Hizmet yapısı kümesi arka uç ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="e8700-137">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="e8700-138">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e8700-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="e8700-139">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="e8700-139">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="e8700-140">Arka uca konuşurken sertifika zinciri doğrulamasının atlanıp atlanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="e8700-140">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="e8700-141">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e8700-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="e8700-142">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="e8700-142">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="e8700-143">Arka uca konuşurken sertifika adı doğrulamasının atlanıp atlanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="e8700-143">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="e8700-144">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e8700-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="e8700-145">-Başlık</span><span class="sxs-lookup"><span data-stu-id="e8700-145">-Title</span></span>
<span data-ttu-id="e8700-146">Arka uç başlığı.</span><span class="sxs-lookup"><span data-stu-id="e8700-146">Backend Title.</span></span>
<span data-ttu-id="e8700-147">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e8700-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="e8700-148">-URL</span><span class="sxs-lookup"><span data-stu-id="e8700-148">-Url</span></span>
<span data-ttu-id="e8700-149">Arka uç için çalışma zamanı URL 'Si.</span><span class="sxs-lookup"><span data-stu-id="e8700-149">Runtime Url for the Backend.</span></span>
<span data-ttu-id="e8700-150">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e8700-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="e8700-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="e8700-151">-Confirm</span></span>
<span data-ttu-id="e8700-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e8700-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8700-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8700-153">-WhatIf</span></span>
<span data-ttu-id="e8700-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8700-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8700-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e8700-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8700-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8700-156">CommonParameters</span></span>
<span data-ttu-id="e8700-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8700-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8700-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8700-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8700-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8700-159">INPUTS</span></span>

### <span data-ttu-id="e8700-160">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="e8700-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e8700-161">System. String</span><span class="sxs-lookup"><span data-stu-id="e8700-161">System.String</span></span>

### <span data-ttu-id="e8700-162">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="e8700-162">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e8700-163">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="e8700-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="e8700-164">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="e8700-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="e8700-165">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementservicefabric</span><span class="sxs-lookup"><span data-stu-id="e8700-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="e8700-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e8700-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e8700-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8700-167">OUTPUTS</span></span>

### <span data-ttu-id="e8700-168">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementarka uç</span><span class="sxs-lookup"><span data-stu-id="e8700-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="e8700-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8700-169">NOTES</span></span>

## <span data-ttu-id="e8700-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8700-170">RELATED LINKS</span></span>

[<span data-ttu-id="e8700-171">Get-Azapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="e8700-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="e8700-172">Yeni-Azsız arka uç</span><span class="sxs-lookup"><span data-stu-id="e8700-172">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="e8700-173">Yeni-Azapsananagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="e8700-173">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="e8700-174">Yeni-Azapsananagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="e8700-174">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="e8700-175">Remove-Azapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="e8700-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
