---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: 52e159ae0f9d1b94b316394ddefe04f0bd8aa1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573038"
---
# <span data-ttu-id="45599-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="45599-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="45599-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45599-102">SYNOPSIS</span></span>
<span data-ttu-id="45599-103">Arka uç güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="45599-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45599-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="45599-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45599-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="45599-105">DESCRIPTION</span></span>
<span data-ttu-id="45599-106">API yönetiminde varolan bir arka uç 'Yi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="45599-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="45599-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="45599-107">EXAMPLES</span></span>

### <span data-ttu-id="45599-108">Arka uç 123 'in açıklamasını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="45599-108">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="45599-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="45599-109">PARAMETERS</span></span>

### <span data-ttu-id="45599-110">-Backenmuydunuz</span><span class="sxs-lookup"><span data-stu-id="45599-110">-BackendId</span></span>
<span data-ttu-id="45599-111">Yeni arka ucun tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="45599-111">Identifier of new backend.</span></span>
<span data-ttu-id="45599-112">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="45599-112">This parameter is required.</span></span>

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

### <span data-ttu-id="45599-113">-Context</span><span class="sxs-lookup"><span data-stu-id="45599-113">-Context</span></span>
<span data-ttu-id="45599-114">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="45599-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="45599-115">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="45599-115">This parameter is required.</span></span>

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

### <span data-ttu-id="45599-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="45599-116">-Credential</span></span>
<span data-ttu-id="45599-117">Arka uca konuşurken kullanılması gereken kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="45599-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="45599-118">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="45599-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="45599-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45599-119">-DefaultProfile</span></span>
<span data-ttu-id="45599-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="45599-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45599-121">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="45599-121">-Description</span></span>
<span data-ttu-id="45599-122">Arka uç açıklaması.</span><span class="sxs-lookup"><span data-stu-id="45599-122">Backend Description.</span></span>
<span data-ttu-id="45599-123">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="45599-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="45599-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="45599-124">-PassThru</span></span>
<span data-ttu-id="45599-125">Bu cmdlet 'in değiştirdiği  **Psapimanagementarka uç** değerini döndüren anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="45599-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="45599-126">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="45599-126">-Protocol</span></span>
<span data-ttu-id="45599-127">Arka uç Iletişim Protokolü (http veya SOAP).</span><span class="sxs-lookup"><span data-stu-id="45599-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="45599-128">Bu parametre isteğe bağlıdır</span><span class="sxs-lookup"><span data-stu-id="45599-128">This parameter is optional</span></span>

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

### <span data-ttu-id="45599-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="45599-129">-Proxy</span></span>
<span data-ttu-id="45599-130">İstek arka uca gönderilirken kullanılacak proxy sunucusu ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="45599-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="45599-131">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="45599-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="45599-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="45599-132">-ResourceId</span></span>
<span data-ttu-id="45599-133">Dış sistemdeki kaynağın yönetim URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="45599-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="45599-134">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="45599-134">This parameter is optional.</span></span>
<span data-ttu-id="45599-135">Bu URL, mantık uygulamalarının, Işlev uygulamalarının veya API uygulamalarının ARM kaynak kimliği olabilir.</span><span class="sxs-lookup"><span data-stu-id="45599-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="45599-136">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="45599-136">-ServiceFabricCluster</span></span>
<span data-ttu-id="45599-137">Hizmet yapısı kümesi arka uç ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="45599-137">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="45599-138">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="45599-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="45599-139">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="45599-139">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="45599-140">Arka uca konuşurken sertifika zinciri doğrulamasının atlanıp atlanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="45599-140">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="45599-141">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="45599-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="45599-142">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="45599-142">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="45599-143">Arka uca konuşurken sertifika adı doğrulamasının atlanıp atlanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="45599-143">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="45599-144">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="45599-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="45599-145">-Başlık</span><span class="sxs-lookup"><span data-stu-id="45599-145">-Title</span></span>
<span data-ttu-id="45599-146">Arka uç başlığı.</span><span class="sxs-lookup"><span data-stu-id="45599-146">Backend Title.</span></span>
<span data-ttu-id="45599-147">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="45599-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="45599-148">-URL</span><span class="sxs-lookup"><span data-stu-id="45599-148">-Url</span></span>
<span data-ttu-id="45599-149">Arka uç için çalışma zamanı URL 'Si.</span><span class="sxs-lookup"><span data-stu-id="45599-149">Runtime Url for the Backend.</span></span>
<span data-ttu-id="45599-150">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="45599-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="45599-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="45599-151">-Confirm</span></span>
<span data-ttu-id="45599-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="45599-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45599-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45599-153">-WhatIf</span></span>
<span data-ttu-id="45599-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="45599-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45599-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="45599-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45599-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45599-156">CommonParameters</span></span>
<span data-ttu-id="45599-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="45599-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45599-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45599-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45599-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="45599-159">INPUTS</span></span>

### <span data-ttu-id="45599-160">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="45599-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="45599-161">System. String</span><span class="sxs-lookup"><span data-stu-id="45599-161">System.String</span></span>

### <span data-ttu-id="45599-162">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="45599-162">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="45599-163">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="45599-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="45599-164">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="45599-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="45599-165">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementservicefabric</span><span class="sxs-lookup"><span data-stu-id="45599-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="45599-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="45599-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="45599-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="45599-167">OUTPUTS</span></span>

### <span data-ttu-id="45599-168">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementarka uç</span><span class="sxs-lookup"><span data-stu-id="45599-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="45599-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="45599-169">NOTES</span></span>

## <span data-ttu-id="45599-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="45599-170">RELATED LINKS</span></span>

[<span data-ttu-id="45599-171">Get-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="45599-171">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="45599-172">Yeni-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="45599-172">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="45599-173">Yeni-Azurermapımanagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="45599-173">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="45599-174">Yeni-Azurermapımanagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="45599-174">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="45599-175">Remove-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="45599-175">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
