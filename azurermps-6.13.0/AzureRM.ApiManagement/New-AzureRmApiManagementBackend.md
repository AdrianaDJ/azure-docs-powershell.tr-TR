---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: 46e0a864bcedd8ac0c23761545f5480eaa4a093a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588645"
---
# <span data-ttu-id="7b578-101">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7b578-101">New-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="7b578-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b578-102">SYNOPSIS</span></span>
<span data-ttu-id="7b578-103">Yeni bir arka uç varlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7b578-103">Creates a new backend entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b578-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7b578-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b578-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7b578-105">DESCRIPTION</span></span>
<span data-ttu-id="7b578-106">API yönetiminde yeni bir arka uç varlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7b578-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="7b578-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7b578-107">EXAMPLES</span></span>

### <span data-ttu-id="7b578-108">Temel yetkilendirme düzeniyle arka uç 123 oluşturma</span><span class="sxs-lookup"><span data-stu-id="7b578-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="7b578-109">Yeni bir arka uç oluşturur</span><span class="sxs-lookup"><span data-stu-id="7b578-109">Creates a new Backend</span></span>

## <span data-ttu-id="7b578-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7b578-110">PARAMETERS</span></span>

### <span data-ttu-id="7b578-111">-Backenmuydunuz</span><span class="sxs-lookup"><span data-stu-id="7b578-111">-BackendId</span></span>
<span data-ttu-id="7b578-112">Yeni arka ucun tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="7b578-112">Identifier of new backend.</span></span>
<span data-ttu-id="7b578-113">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7b578-113">This parameter is optional.</span></span>
<span data-ttu-id="7b578-114">Belirtilmemişse,.</span><span class="sxs-lookup"><span data-stu-id="7b578-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="7b578-115">-Context</span><span class="sxs-lookup"><span data-stu-id="7b578-115">-Context</span></span>
<span data-ttu-id="7b578-116">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="7b578-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7b578-117">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="7b578-117">This parameter is required.</span></span>

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

### <span data-ttu-id="7b578-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="7b578-118">-Credential</span></span>
<span data-ttu-id="7b578-119">Arka uca konuşurken kullanılması gereken kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="7b578-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="7b578-120">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7b578-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="7b578-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b578-121">-DefaultProfile</span></span>
<span data-ttu-id="7b578-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7b578-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b578-123">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="7b578-123">-Description</span></span>
<span data-ttu-id="7b578-124">Arka uç açıklaması.</span><span class="sxs-lookup"><span data-stu-id="7b578-124">Backend Description.</span></span>
<span data-ttu-id="7b578-125">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7b578-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="7b578-126">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="7b578-126">-Protocol</span></span>
<span data-ttu-id="7b578-127">Arka uç Iletişim protokolü.</span><span class="sxs-lookup"><span data-stu-id="7b578-127">Backend Communication protocol.</span></span>
<span data-ttu-id="7b578-128">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="7b578-128">This parameter is required.</span></span>
<span data-ttu-id="7b578-129">Geçerli değerler ' http ' ve ' SOAP ' değerleridir.</span><span class="sxs-lookup"><span data-stu-id="7b578-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="7b578-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="7b578-130">-Proxy</span></span>
<span data-ttu-id="7b578-131">İstek arka uca gönderilirken kullanılacak proxy sunucusu ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="7b578-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="7b578-132">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7b578-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="7b578-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7b578-133">-ResourceId</span></span>
<span data-ttu-id="7b578-134">Dış sistemdeki kaynağın yönetim URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="7b578-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="7b578-135">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7b578-135">This parameter is optional.</span></span>
<span data-ttu-id="7b578-136">Bu URL, mantık uygulamalarının, Işlev uygulamalarının veya API uygulamalarının ARM kaynak kimliği olabilir.</span><span class="sxs-lookup"><span data-stu-id="7b578-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="7b578-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="7b578-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="7b578-138">Hizmet yapısı kümesi arka uç ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="7b578-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="7b578-139">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7b578-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="7b578-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="7b578-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="7b578-141">Arka uca konuşurken sertifika zinciri doğrulamasının atlanıp atlanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="7b578-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="7b578-142">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7b578-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="7b578-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="7b578-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="7b578-144">Arka uca konuşurken sertifika adı doğrulamasının atlanıp atlanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="7b578-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="7b578-145">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7b578-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="7b578-146">-Başlık</span><span class="sxs-lookup"><span data-stu-id="7b578-146">-Title</span></span>
<span data-ttu-id="7b578-147">Arka uç başlığı.</span><span class="sxs-lookup"><span data-stu-id="7b578-147">Backend Title.</span></span>
<span data-ttu-id="7b578-148">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7b578-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="7b578-149">-URL</span><span class="sxs-lookup"><span data-stu-id="7b578-149">-Url</span></span>
<span data-ttu-id="7b578-150">Arka uç için çalışma zamanı URL 'Si.</span><span class="sxs-lookup"><span data-stu-id="7b578-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="7b578-151">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="7b578-151">This parameter is required.</span></span>

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

### <span data-ttu-id="7b578-152">-Onay</span><span class="sxs-lookup"><span data-stu-id="7b578-152">-Confirm</span></span>
<span data-ttu-id="7b578-153">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7b578-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b578-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b578-154">-WhatIf</span></span>
<span data-ttu-id="7b578-155">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7b578-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b578-156">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7b578-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b578-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b578-157">CommonParameters</span></span>
<span data-ttu-id="7b578-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7b578-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b578-159">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b578-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b578-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7b578-160">INPUTS</span></span>

### <span data-ttu-id="7b578-161">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="7b578-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7b578-162">System. String</span><span class="sxs-lookup"><span data-stu-id="7b578-162">System.String</span></span>

### <span data-ttu-id="7b578-163">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7b578-163">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7b578-164">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="7b578-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="7b578-165">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="7b578-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="7b578-166">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementservicefabric</span><span class="sxs-lookup"><span data-stu-id="7b578-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="7b578-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7b578-167">OUTPUTS</span></span>

### <span data-ttu-id="7b578-168">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementarka uç</span><span class="sxs-lookup"><span data-stu-id="7b578-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="7b578-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7b578-169">NOTES</span></span>

## <span data-ttu-id="7b578-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7b578-170">RELATED LINKS</span></span>

[<span data-ttu-id="7b578-171">Get-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="7b578-171">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="7b578-172">Yeni-Azurermapımanagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="7b578-172">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="7b578-173">Yeni-Azurermapımanagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="7b578-173">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="7b578-174">Set-Azurermapımanaarka uç</span><span class="sxs-lookup"><span data-stu-id="7b578-174">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="7b578-175">Remove-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="7b578-175">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)

