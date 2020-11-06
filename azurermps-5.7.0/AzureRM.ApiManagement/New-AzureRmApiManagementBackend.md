---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: c337e82c88c7fdbbc1f8a3663249126c9d92b19f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594519"
---
# <span data-ttu-id="97142-101">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="97142-101">New-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="97142-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97142-102">SYNOPSIS</span></span>
<span data-ttu-id="97142-103">Yeni bir arka uç varlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="97142-103">Creates a new backend entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97142-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97142-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97142-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="97142-105">DESCRIPTION</span></span>
<span data-ttu-id="97142-106">API yönetiminde yeni bir arka uç varlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="97142-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="97142-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97142-107">EXAMPLES</span></span>

### <span data-ttu-id="97142-108">Temel yetkilendirme düzeniyle arka uç 123 oluşturma</span><span class="sxs-lookup"><span data-stu-id="97142-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="97142-109">Yeni bir arka uç oluşturur</span><span class="sxs-lookup"><span data-stu-id="97142-109">Creates a new Backend</span></span>

## <span data-ttu-id="97142-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97142-110">PARAMETERS</span></span>

### <span data-ttu-id="97142-111">-Backenmuydunuz</span><span class="sxs-lookup"><span data-stu-id="97142-111">-BackendId</span></span>
<span data-ttu-id="97142-112">Yeni arka ucun tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="97142-112">Identifier of new backend.</span></span>
<span data-ttu-id="97142-113">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="97142-113">This parameter is optional.</span></span>
<span data-ttu-id="97142-114">Belirtilmemişse,.</span><span class="sxs-lookup"><span data-stu-id="97142-114">If not specified will be generated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97142-115">-Context</span><span class="sxs-lookup"><span data-stu-id="97142-115">-Context</span></span>
<span data-ttu-id="97142-116">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="97142-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="97142-117">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="97142-117">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97142-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="97142-118">-Credential</span></span>
<span data-ttu-id="97142-119">Arka uca konuşurken kullanılması gereken kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="97142-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="97142-120">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="97142-120">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementBackendCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97142-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97142-121">-DefaultProfile</span></span>
<span data-ttu-id="97142-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="97142-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97142-123">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="97142-123">-Description</span></span>
<span data-ttu-id="97142-124">Arka uç açıklaması.</span><span class="sxs-lookup"><span data-stu-id="97142-124">Backend Description.</span></span>
<span data-ttu-id="97142-125">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="97142-125">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97142-126">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="97142-126">-Protocol</span></span>
<span data-ttu-id="97142-127">Arka uç Iletişim protokolü.</span><span class="sxs-lookup"><span data-stu-id="97142-127">Backend Communication protocol.</span></span>
<span data-ttu-id="97142-128">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="97142-128">This parameter is required.</span></span>
<span data-ttu-id="97142-129">Geçerli değerler ' http ' ve ' SOAP ' değerleridir.</span><span class="sxs-lookup"><span data-stu-id="97142-129">Valid values are 'http' and 'soap'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97142-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="97142-130">-Proxy</span></span>
<span data-ttu-id="97142-131">İstek arka uca gönderilirken kullanılacak proxy sunucusu ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="97142-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="97142-132">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="97142-132">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementBackendProxy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97142-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="97142-133">-ResourceId</span></span>
<span data-ttu-id="97142-134">Dış sistemdeki kaynağın yönetim URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="97142-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="97142-135">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="97142-135">This parameter is optional.</span></span>
<span data-ttu-id="97142-136">Bu URL, mantık uygulamalarının, Işlev uygulamalarının veya API uygulamalarının ARM kaynak kimliği olabilir.</span><span class="sxs-lookup"><span data-stu-id="97142-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97142-137">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="97142-137">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="97142-138">Arka uca konuşurken sertifika zinciri doğrulamasının atlanıp atlanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="97142-138">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="97142-139">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="97142-139">This parameter is optional.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97142-140">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="97142-140">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="97142-141">Arka uca konuşurken sertifika adı doğrulamasının atlanıp atlanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="97142-141">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="97142-142">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="97142-142">This parameter is optional.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97142-143">-Başlık</span><span class="sxs-lookup"><span data-stu-id="97142-143">-Title</span></span>
<span data-ttu-id="97142-144">Arka uç başlığı.</span><span class="sxs-lookup"><span data-stu-id="97142-144">Backend Title.</span></span>
<span data-ttu-id="97142-145">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="97142-145">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97142-146">-URL</span><span class="sxs-lookup"><span data-stu-id="97142-146">-Url</span></span>
<span data-ttu-id="97142-147">Arka uç için çalışma zamanı URL 'Si.</span><span class="sxs-lookup"><span data-stu-id="97142-147">Runtime Url for the Backend.</span></span>
<span data-ttu-id="97142-148">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="97142-148">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97142-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="97142-149">-Confirm</span></span>
<span data-ttu-id="97142-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="97142-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97142-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97142-151">-WhatIf</span></span>
<span data-ttu-id="97142-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="97142-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97142-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="97142-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97142-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97142-154">CommonParameters</span></span>
<span data-ttu-id="97142-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97142-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97142-156">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97142-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97142-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97142-157">INPUTS</span></span>

### <span data-ttu-id="97142-158">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="97142-158">None</span></span>
<span data-ttu-id="97142-159">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="97142-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="97142-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97142-160">OUTPUTS</span></span>

### <span data-ttu-id="97142-161">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementarka uç</span><span class="sxs-lookup"><span data-stu-id="97142-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="97142-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97142-162">NOTES</span></span>

## <span data-ttu-id="97142-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97142-163">RELATED LINKS</span></span>

[<span data-ttu-id="97142-164">Get-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="97142-164">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="97142-165">Yeni-Azurermapımanagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="97142-165">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="97142-166">Yeni-Azurermapımanagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="97142-166">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="97142-167">Set-Azurermapımanaarka uç</span><span class="sxs-lookup"><span data-stu-id="97142-167">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="97142-168">Remove-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="97142-168">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)

