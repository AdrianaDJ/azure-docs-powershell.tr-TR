---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: 5caef678df0aef88f4655c031d53e995920d0379
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753542"
---
# <span data-ttu-id="fc1bd-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fc1bd-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="fc1bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc1bd-102">SYNOPSIS</span></span>
<span data-ttu-id="fc1bd-103">Yeni bir arka uç varlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="fc1bd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc1bd-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc1bd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc1bd-105">DESCRIPTION</span></span>
<span data-ttu-id="fc1bd-106">API yönetiminde yeni bir arka uç varlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="fc1bd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc1bd-107">EXAMPLES</span></span>

### <span data-ttu-id="fc1bd-108">Temel yetkilendirme düzeniyle arka uç 123 oluşturma</span><span class="sxs-lookup"><span data-stu-id="fc1bd-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="fc1bd-109">Yeni bir arka uç oluşturur</span><span class="sxs-lookup"><span data-stu-id="fc1bd-109">Creates a new Backend</span></span>

## <span data-ttu-id="fc1bd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc1bd-110">PARAMETERS</span></span>

### <span data-ttu-id="fc1bd-111">-Backenmuydunuz</span><span class="sxs-lookup"><span data-stu-id="fc1bd-111">-BackendId</span></span>
<span data-ttu-id="fc1bd-112">Yeni arka ucun tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-112">Identifier of new backend.</span></span>
<span data-ttu-id="fc1bd-113">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-113">This parameter is optional.</span></span>
<span data-ttu-id="fc1bd-114">Belirtilmemişse,.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="fc1bd-115">-Context</span><span class="sxs-lookup"><span data-stu-id="fc1bd-115">-Context</span></span>
<span data-ttu-id="fc1bd-116">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fc1bd-117">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-117">This parameter is required.</span></span>

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

### <span data-ttu-id="fc1bd-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="fc1bd-118">-Credential</span></span>
<span data-ttu-id="fc1bd-119">Arka uca konuşurken kullanılması gereken kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="fc1bd-120">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="fc1bd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc1bd-121">-DefaultProfile</span></span>
<span data-ttu-id="fc1bd-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc1bd-123">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="fc1bd-123">-Description</span></span>
<span data-ttu-id="fc1bd-124">Arka uç açıklaması.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-124">Backend Description.</span></span>
<span data-ttu-id="fc1bd-125">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="fc1bd-126">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="fc1bd-126">-Protocol</span></span>
<span data-ttu-id="fc1bd-127">Arka uç Iletişim protokolü.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-127">Backend Communication protocol.</span></span>
<span data-ttu-id="fc1bd-128">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-128">This parameter is required.</span></span>
<span data-ttu-id="fc1bd-129">Geçerli değerler ' http ' ve ' SOAP ' değerleridir.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-129">Valid values are 'http' and 'soap'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: http, soap

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc1bd-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="fc1bd-130">-Proxy</span></span>
<span data-ttu-id="fc1bd-131">İstek arka uca gönderilirken kullanılacak proxy sunucusu ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="fc1bd-132">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="fc1bd-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fc1bd-133">-ResourceId</span></span>
<span data-ttu-id="fc1bd-134">Dış sistemdeki kaynağın yönetim URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="fc1bd-135">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-135">This parameter is optional.</span></span>
<span data-ttu-id="fc1bd-136">Bu URL, mantık uygulamalarının, Işlev uygulamalarının veya API uygulamalarının ARM kaynak kimliği olabilir.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="fc1bd-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="fc1bd-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="fc1bd-138">Hizmet yapısı kümesi arka uç ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="fc1bd-139">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="fc1bd-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="fc1bd-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="fc1bd-141">Arka uca konuşurken sertifika zinciri doğrulamasının atlanıp atlanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="fc1bd-142">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="fc1bd-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="fc1bd-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="fc1bd-144">Arka uca konuşurken sertifika adı doğrulamasının atlanıp atlanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="fc1bd-145">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="fc1bd-146">-Başlık</span><span class="sxs-lookup"><span data-stu-id="fc1bd-146">-Title</span></span>
<span data-ttu-id="fc1bd-147">Arka uç başlığı.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-147">Backend Title.</span></span>
<span data-ttu-id="fc1bd-148">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="fc1bd-149">-URL</span><span class="sxs-lookup"><span data-stu-id="fc1bd-149">-Url</span></span>
<span data-ttu-id="fc1bd-150">Arka uç için çalışma zamanı URL 'Si.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="fc1bd-151">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-151">This parameter is required.</span></span>

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

### <span data-ttu-id="fc1bd-152">-Onay</span><span class="sxs-lookup"><span data-stu-id="fc1bd-152">-Confirm</span></span>
<span data-ttu-id="fc1bd-153">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc1bd-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc1bd-154">-WhatIf</span></span>
<span data-ttu-id="fc1bd-155">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc1bd-156">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc1bd-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc1bd-157">CommonParameters</span></span>
<span data-ttu-id="fc1bd-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc1bd-159">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-159">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc1bd-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc1bd-160">INPUTS</span></span>

### <span data-ttu-id="fc1bd-161">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="fc1bd-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fc1bd-162">System. String</span><span class="sxs-lookup"><span data-stu-id="fc1bd-162">System.String</span></span>

### <span data-ttu-id="fc1bd-163">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="fc1bd-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fc1bd-164">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="fc1bd-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="fc1bd-165">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="fc1bd-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="fc1bd-166">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementservicefabric</span><span class="sxs-lookup"><span data-stu-id="fc1bd-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="fc1bd-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc1bd-167">OUTPUTS</span></span>

### <span data-ttu-id="fc1bd-168">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementarka uç</span><span class="sxs-lookup"><span data-stu-id="fc1bd-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="fc1bd-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc1bd-169">NOTES</span></span>

## <span data-ttu-id="fc1bd-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc1bd-170">RELATED LINKS</span></span>

[<span data-ttu-id="fc1bd-171">Get-Azapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="fc1bd-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="fc1bd-172">Yeni-Azapsananagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="fc1bd-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="fc1bd-173">Yeni-Azapsananagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="fc1bd-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="fc1bd-174">Set-Azapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="fc1bd-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="fc1bd-175">Remove-Azapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="fc1bd-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

