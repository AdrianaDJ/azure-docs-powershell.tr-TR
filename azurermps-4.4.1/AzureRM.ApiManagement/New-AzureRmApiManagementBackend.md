---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: 144830c2155379683c8568eda6e0d1bc021b38fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591239"
---
# <span data-ttu-id="a9c49-101">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a9c49-101">New-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="a9c49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9c49-102">SYNOPSIS</span></span>
<span data-ttu-id="a9c49-103">Yeni bir arka uç varlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9c49-103">Creates a new backend entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9c49-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9c49-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9c49-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9c49-105">DESCRIPTION</span></span>
<span data-ttu-id="a9c49-106">API yönetiminde yeni bir arka uç varlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9c49-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="a9c49-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9c49-107">EXAMPLES</span></span>

### <span data-ttu-id="a9c49-108">Temel yetkilendirme düzeniyle arka uç 123 oluşturma</span><span class="sxs-lookup"><span data-stu-id="a9c49-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```
$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="a9c49-109">Yeni bir arka uç oluşturur</span><span class="sxs-lookup"><span data-stu-id="a9c49-109">Creates a new Backend</span></span>

## <span data-ttu-id="a9c49-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9c49-110">PARAMETERS</span></span>

### <span data-ttu-id="a9c49-111">-Backenmuydunuz</span><span class="sxs-lookup"><span data-stu-id="a9c49-111">-BackendId</span></span>
<span data-ttu-id="a9c49-112">Yeni arka ucun tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="a9c49-112">Identifier of new backend.</span></span>
<span data-ttu-id="a9c49-113">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a9c49-113">This parameter is optional.</span></span>
<span data-ttu-id="a9c49-114">Belirtilmemişse,.</span><span class="sxs-lookup"><span data-stu-id="a9c49-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="a9c49-115">-Context</span><span class="sxs-lookup"><span data-stu-id="a9c49-115">-Context</span></span>
<span data-ttu-id="a9c49-116">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="a9c49-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a9c49-117">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a9c49-117">This parameter is required.</span></span>

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

### <span data-ttu-id="a9c49-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="a9c49-118">-Credential</span></span>
<span data-ttu-id="a9c49-119">Arka uca konuşurken kullanılması gereken kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="a9c49-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="a9c49-120">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a9c49-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="a9c49-121">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="a9c49-121">-Description</span></span>
<span data-ttu-id="a9c49-122">Arka uç açıklaması.</span><span class="sxs-lookup"><span data-stu-id="a9c49-122">Backend Description.</span></span>
<span data-ttu-id="a9c49-123">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a9c49-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="a9c49-124">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="a9c49-124">-Protocol</span></span>
<span data-ttu-id="a9c49-125">Arka uç Iletişim protokolü.</span><span class="sxs-lookup"><span data-stu-id="a9c49-125">Backend Communication protocol.</span></span>
<span data-ttu-id="a9c49-126">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a9c49-126">This parameter is required.</span></span>
<span data-ttu-id="a9c49-127">Geçerli değerler ' http ' ve ' SOAP ' değerleridir.</span><span class="sxs-lookup"><span data-stu-id="a9c49-127">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="a9c49-128">-Proxy</span><span class="sxs-lookup"><span data-stu-id="a9c49-128">-Proxy</span></span>
<span data-ttu-id="a9c49-129">İstek arka uca gönderilirken kullanılacak proxy sunucusu ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="a9c49-129">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="a9c49-130">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a9c49-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="a9c49-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a9c49-131">-ResourceId</span></span>
<span data-ttu-id="a9c49-132">Dış sistemdeki kaynağın yönetim URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="a9c49-132">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="a9c49-133">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a9c49-133">This parameter is optional.</span></span>
<span data-ttu-id="a9c49-134">Bu URL, mantık uygulamalarının, Işlev uygulamalarının veya API uygulamalarının ARM kaynak kimliği olabilir.</span><span class="sxs-lookup"><span data-stu-id="a9c49-134">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="a9c49-135">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="a9c49-135">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="a9c49-136">Arka uca konuşurken sertifika zinciri doğrulamasının atlanıp atlanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="a9c49-136">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="a9c49-137">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a9c49-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="a9c49-138">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="a9c49-138">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="a9c49-139">Arka uca konuşurken sertifika adı doğrulamasının atlanıp atlanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="a9c49-139">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="a9c49-140">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a9c49-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="a9c49-141">-Başlık</span><span class="sxs-lookup"><span data-stu-id="a9c49-141">-Title</span></span>
<span data-ttu-id="a9c49-142">Arka uç başlığı.</span><span class="sxs-lookup"><span data-stu-id="a9c49-142">Backend Title.</span></span>
<span data-ttu-id="a9c49-143">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a9c49-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="a9c49-144">-URL</span><span class="sxs-lookup"><span data-stu-id="a9c49-144">-Url</span></span>
<span data-ttu-id="a9c49-145">Arka uç için çalışma zamanı URL 'Si.</span><span class="sxs-lookup"><span data-stu-id="a9c49-145">Runtime Url for the Backend.</span></span>
<span data-ttu-id="a9c49-146">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a9c49-146">This parameter is required.</span></span>

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

### <span data-ttu-id="a9c49-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="a9c49-147">-Confirm</span></span>
<span data-ttu-id="a9c49-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a9c49-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9c49-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9c49-149">-WhatIf</span></span>
<span data-ttu-id="a9c49-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9c49-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9c49-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a9c49-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9c49-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9c49-152">-DefaultProfile</span></span>
<span data-ttu-id="a9c49-153">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a9c49-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9c49-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9c49-154">CommonParameters</span></span>
<span data-ttu-id="a9c49-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9c49-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9c49-156">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9c49-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9c49-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9c49-157">INPUTS</span></span>

## <span data-ttu-id="a9c49-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9c49-158">OUTPUTS</span></span>

### <span data-ttu-id="a9c49-159">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementarka uç</span><span class="sxs-lookup"><span data-stu-id="a9c49-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="a9c49-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9c49-160">NOTES</span></span>

## <span data-ttu-id="a9c49-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9c49-161">RELATED LINKS</span></span>

[<span data-ttu-id="a9c49-162">Get-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="a9c49-162">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="a9c49-163">Yeni-Azurermapımanagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="a9c49-163">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="a9c49-164">Yeni-Azurermapımanagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="a9c49-164">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="a9c49-165">Set-Azurermapımanaarka uç</span><span class="sxs-lookup"><span data-stu-id="a9c49-165">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="a9c49-166">Remove-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="a9c49-166">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)

