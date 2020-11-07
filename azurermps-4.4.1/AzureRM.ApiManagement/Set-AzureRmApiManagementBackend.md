---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: 85545777f5a76f3f75e81648a009ffcdcad8ab30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764279"
---
# <span data-ttu-id="269d2-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="269d2-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="269d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="269d2-102">SYNOPSIS</span></span>
<span data-ttu-id="269d2-103">Arka uç güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="269d2-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="269d2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="269d2-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="269d2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="269d2-105">DESCRIPTION</span></span>
<span data-ttu-id="269d2-106">API yönetiminde varolan bir arka uç 'Yi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="269d2-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="269d2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="269d2-107">EXAMPLES</span></span>

### <span data-ttu-id="269d2-108">Arka uç 123 'in açıklamasını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="269d2-108">Updates the Description of the Backend 123</span></span>
```
Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="269d2-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="269d2-109">PARAMETERS</span></span>

### <span data-ttu-id="269d2-110">-Backenmuydunuz</span><span class="sxs-lookup"><span data-stu-id="269d2-110">-BackendId</span></span>
<span data-ttu-id="269d2-111">Yeni arka ucun tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="269d2-111">Identifier of new backend.</span></span>
<span data-ttu-id="269d2-112">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="269d2-112">This parameter is required.</span></span>

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

### <span data-ttu-id="269d2-113">-Context</span><span class="sxs-lookup"><span data-stu-id="269d2-113">-Context</span></span>
<span data-ttu-id="269d2-114">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="269d2-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="269d2-115">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="269d2-115">This parameter is required.</span></span>

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

### <span data-ttu-id="269d2-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="269d2-116">-Credential</span></span>
<span data-ttu-id="269d2-117">Arka uca konuşurken kullanılması gereken kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="269d2-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="269d2-118">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="269d2-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="269d2-119">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="269d2-119">-Description</span></span>
<span data-ttu-id="269d2-120">Arka uç açıklaması.</span><span class="sxs-lookup"><span data-stu-id="269d2-120">Backend Description.</span></span>
<span data-ttu-id="269d2-121">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="269d2-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="269d2-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="269d2-122">-PassThru</span></span>
<span data-ttu-id="269d2-123">Bu cmdlet 'in değiştirdiği  **Psapimanagementarka uç** değerini döndüren anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="269d2-123">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="269d2-124">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="269d2-124">-Protocol</span></span>
<span data-ttu-id="269d2-125">Arka uç Iletişim Protokolü (http veya SOAP).</span><span class="sxs-lookup"><span data-stu-id="269d2-125">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="269d2-126">Bu parametre isteğe bağlıdır</span><span class="sxs-lookup"><span data-stu-id="269d2-126">This parameter is optional</span></span>

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

### <span data-ttu-id="269d2-127">-Proxy</span><span class="sxs-lookup"><span data-stu-id="269d2-127">-Proxy</span></span>
<span data-ttu-id="269d2-128">İstek arka uca gönderilirken kullanılacak proxy sunucusu ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="269d2-128">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="269d2-129">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="269d2-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="269d2-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="269d2-130">-ResourceId</span></span>
<span data-ttu-id="269d2-131">Dış sistemdeki kaynağın yönetim URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="269d2-131">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="269d2-132">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="269d2-132">This parameter is optional.</span></span>
<span data-ttu-id="269d2-133">Bu URL, mantık uygulamalarının, Işlev uygulamalarının veya API uygulamalarının ARM kaynak kimliği olabilir.</span><span class="sxs-lookup"><span data-stu-id="269d2-133">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="269d2-134">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="269d2-134">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="269d2-135">Arka uca konuşurken sertifika zinciri doğrulamasının atlanıp atlanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="269d2-135">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="269d2-136">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="269d2-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="269d2-137">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="269d2-137">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="269d2-138">Arka uca konuşurken sertifika adı doğrulamasının atlanıp atlanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="269d2-138">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="269d2-139">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="269d2-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="269d2-140">-Başlık</span><span class="sxs-lookup"><span data-stu-id="269d2-140">-Title</span></span>
<span data-ttu-id="269d2-141">Arka uç başlığı.</span><span class="sxs-lookup"><span data-stu-id="269d2-141">Backend Title.</span></span>
<span data-ttu-id="269d2-142">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="269d2-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="269d2-143">-URL</span><span class="sxs-lookup"><span data-stu-id="269d2-143">-Url</span></span>
<span data-ttu-id="269d2-144">Arka uç için çalışma zamanı URL 'Si.</span><span class="sxs-lookup"><span data-stu-id="269d2-144">Runtime Url for the Backend.</span></span>
<span data-ttu-id="269d2-145">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="269d2-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="269d2-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="269d2-146">-Confirm</span></span>
<span data-ttu-id="269d2-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="269d2-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="269d2-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="269d2-148">-WhatIf</span></span>
<span data-ttu-id="269d2-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="269d2-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="269d2-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="269d2-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="269d2-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="269d2-151">-DefaultProfile</span></span>
<span data-ttu-id="269d2-152">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="269d2-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="269d2-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="269d2-153">CommonParameters</span></span>
<span data-ttu-id="269d2-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="269d2-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="269d2-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="269d2-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="269d2-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="269d2-156">INPUTS</span></span>

## <span data-ttu-id="269d2-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="269d2-157">OUTPUTS</span></span>

### <span data-ttu-id="269d2-158">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementarka uç</span><span class="sxs-lookup"><span data-stu-id="269d2-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="269d2-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="269d2-159">NOTES</span></span>

## <span data-ttu-id="269d2-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="269d2-160">RELATED LINKS</span></span>

[<span data-ttu-id="269d2-161">Get-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="269d2-161">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="269d2-162">Yeni-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="269d2-162">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="269d2-163">Yeni-Azurermapımanagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="269d2-163">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="269d2-164">Yeni-Azurermapımanagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="269d2-164">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="269d2-165">Remove-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="269d2-165">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
