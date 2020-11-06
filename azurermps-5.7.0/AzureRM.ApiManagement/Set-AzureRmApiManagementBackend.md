---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: b5e51891f82b2a12f42fac3a1535f974912ca1dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590543"
---
# <span data-ttu-id="ee8a5-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ee8a5-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="ee8a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee8a5-102">SYNOPSIS</span></span>
<span data-ttu-id="ee8a5-103">Arka uç güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee8a5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ee8a5-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee8a5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ee8a5-105">DESCRIPTION</span></span>
<span data-ttu-id="ee8a5-106">API yönetiminde varolan bir arka uç 'Yi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="ee8a5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ee8a5-107">EXAMPLES</span></span>

### <span data-ttu-id="ee8a5-108">Arka uç 123 'in açıklamasını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="ee8a5-108">Updates the Description of the Backend 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="ee8a5-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ee8a5-109">PARAMETERS</span></span>

### <span data-ttu-id="ee8a5-110">-Backenmuydunuz</span><span class="sxs-lookup"><span data-stu-id="ee8a5-110">-BackendId</span></span>
<span data-ttu-id="ee8a5-111">Yeni arka ucun tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-111">Identifier of new backend.</span></span>
<span data-ttu-id="ee8a5-112">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-112">This parameter is required.</span></span>

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

### <span data-ttu-id="ee8a5-113">-Context</span><span class="sxs-lookup"><span data-stu-id="ee8a5-113">-Context</span></span>
<span data-ttu-id="ee8a5-114">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ee8a5-115">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-115">This parameter is required.</span></span>

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

### <span data-ttu-id="ee8a5-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="ee8a5-116">-Credential</span></span>
<span data-ttu-id="ee8a5-117">Arka uca konuşurken kullanılması gereken kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="ee8a5-118">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="ee8a5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee8a5-119">-DefaultProfile</span></span>
<span data-ttu-id="ee8a5-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="ee8a5-121">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="ee8a5-121">-Description</span></span>
<span data-ttu-id="ee8a5-122">Arka uç açıklaması.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-122">Backend Description.</span></span>
<span data-ttu-id="ee8a5-123">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="ee8a5-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ee8a5-124">-PassThru</span></span>
<span data-ttu-id="ee8a5-125">Bu cmdlet 'in değiştirdiği  **Psapimanagementarka uç** değerini döndüren anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee8a5-126">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="ee8a5-126">-Protocol</span></span>
<span data-ttu-id="ee8a5-127">Arka uç Iletişim Protokolü (http veya SOAP).</span><span class="sxs-lookup"><span data-stu-id="ee8a5-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="ee8a5-128">Bu parametre isteğe bağlıdır</span><span class="sxs-lookup"><span data-stu-id="ee8a5-128">This parameter is optional</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee8a5-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="ee8a5-129">-Proxy</span></span>
<span data-ttu-id="ee8a5-130">İstek arka uca gönderilirken kullanılacak proxy sunucusu ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="ee8a5-131">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="ee8a5-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ee8a5-132">-ResourceId</span></span>
<span data-ttu-id="ee8a5-133">Dış sistemdeki kaynağın yönetim URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="ee8a5-134">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-134">This parameter is optional.</span></span>
<span data-ttu-id="ee8a5-135">Bu URL, mantık uygulamalarının, Işlev uygulamalarının veya API uygulamalarının ARM kaynak kimliği olabilir.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="ee8a5-136">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="ee8a5-136">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="ee8a5-137">Arka uca konuşurken sertifika zinciri doğrulamasının atlanıp atlanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-137">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="ee8a5-138">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="ee8a5-139">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="ee8a5-139">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="ee8a5-140">Arka uca konuşurken sertifika adı doğrulamasının atlanıp atlanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-140">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="ee8a5-141">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="ee8a5-142">-Başlık</span><span class="sxs-lookup"><span data-stu-id="ee8a5-142">-Title</span></span>
<span data-ttu-id="ee8a5-143">Arka uç başlığı.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-143">Backend Title.</span></span>
<span data-ttu-id="ee8a5-144">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="ee8a5-145">-URL</span><span class="sxs-lookup"><span data-stu-id="ee8a5-145">-Url</span></span>
<span data-ttu-id="ee8a5-146">Arka uç için çalışma zamanı URL 'Si.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-146">Runtime Url for the Backend.</span></span>
<span data-ttu-id="ee8a5-147">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="ee8a5-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="ee8a5-148">-Confirm</span></span>
<span data-ttu-id="ee8a5-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee8a5-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee8a5-150">-WhatIf</span></span>
<span data-ttu-id="ee8a5-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee8a5-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee8a5-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee8a5-153">CommonParameters</span></span>
<span data-ttu-id="ee8a5-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee8a5-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee8a5-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee8a5-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ee8a5-156">INPUTS</span></span>

### <span data-ttu-id="ee8a5-157">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ee8a5-157">None</span></span>
<span data-ttu-id="ee8a5-158">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ee8a5-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ee8a5-159">OUTPUTS</span></span>

### <span data-ttu-id="ee8a5-160">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementarka uç</span><span class="sxs-lookup"><span data-stu-id="ee8a5-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="ee8a5-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ee8a5-161">NOTES</span></span>

## <span data-ttu-id="ee8a5-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ee8a5-162">RELATED LINKS</span></span>

[<span data-ttu-id="ee8a5-163">Get-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="ee8a5-163">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="ee8a5-164">Yeni-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="ee8a5-164">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="ee8a5-165">Yeni-Azurermapımanagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="ee8a5-165">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="ee8a5-166">Yeni-Azurermapımanagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="ee8a5-166">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="ee8a5-167">Remove-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="ee8a5-167">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
