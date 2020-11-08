---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
ms.openlocfilehash: ced4c9708d2ac7f82144e1965beb36a250bbe369
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097725"
---
# <span data-ttu-id="a985b-101">New-AzApiManagementBackendServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a985b-101">New-AzApiManagementBackendServiceFabric</span></span>

## <span data-ttu-id="a985b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a985b-102">SYNOPSIS</span></span>
<span data-ttu-id="a985b-103">Nesnesi oluşturur `PsApiManagementServiceFabric`</span><span class="sxs-lookup"><span data-stu-id="a985b-103">Creates an object of `PsApiManagementServiceFabric`</span></span>

## <span data-ttu-id="a985b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a985b-104">SYNTAX</span></span>

```
New-AzApiManagementBackendServiceFabric -ManagementEndpoint <String[]> -ClientCertificateThumbprint <String>
 [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>] [-ServerCertificateThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a985b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a985b-105">DESCRIPTION</span></span>

<span data-ttu-id="a985b-106">**Yeni-Azapsananagementbackendservicefabric** cmdlet 'ı, `PsApiManagementServiceFabric` **New-azapsananagementarka uç** ve **set-azapsananagementarka uç** cmdlet 'inde kullanılacak bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a985b-106">The **New-AzApiManagementBackendServiceFabric** cmdlet creates an object of `PsApiManagementServiceFabric` to be used in cmdlet **New-AzApiManagementBackend** and **Set-AzApiManagementBackend**.</span></span>

## <span data-ttu-id="a985b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a985b-107">EXAMPLES</span></span>

### <span data-ttu-id="a985b-108">Örnek 1: arka uç hizmet yapısı oluşturma In-Memory nesnesi</span><span class="sxs-lookup"><span data-stu-id="a985b-108">Example 1: Create a Backend Service Fabric In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

<span data-ttu-id="a985b-109">Arka uç hizmet doku sözleşmesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="a985b-109">Creates a Backend Service Fabric Contract</span></span>

## <span data-ttu-id="a985b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a985b-110">PARAMETERS</span></span>

### <span data-ttu-id="a985b-111">-ClientCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="a985b-111">-ClientCertificateThumbprint</span></span>
<span data-ttu-id="a985b-112">Yönetim uç noktası için istemci sertifikası Parmak Izi.</span><span class="sxs-lookup"><span data-stu-id="a985b-112">Client Certificate Thumbprint for the management endpoint.</span></span>
<span data-ttu-id="a985b-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a985b-113">This parameter is required.</span></span>

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

### <span data-ttu-id="a985b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a985b-114">-DefaultProfile</span></span>
<span data-ttu-id="a985b-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a985b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a985b-116">-ManagementEndpoint</span><span class="sxs-lookup"><span data-stu-id="a985b-116">-ManagementEndpoint</span></span>
<span data-ttu-id="a985b-117">Hizmet yapısı küme yönetimi uç noktaları.</span><span class="sxs-lookup"><span data-stu-id="a985b-117">Service Fabric Cluster management Endpoints.</span></span>
<span data-ttu-id="a985b-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a985b-118">This parameter is required.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a985b-119">-MaxPartitionResolutionRetry</span><span class="sxs-lookup"><span data-stu-id="a985b-119">-MaxPartitionResolutionRetry</span></span>
<span data-ttu-id="a985b-120">Hizmet yapısı bölümü çözümlenirken en fazla deneme sayısı.</span><span class="sxs-lookup"><span data-stu-id="a985b-120">Maximum number of retries when resolving a Service Fabric partition.</span></span>
<span data-ttu-id="a985b-121">Bu parametre isteğe bağlıdır ve varsayılan değer 5 ' tir.</span><span class="sxs-lookup"><span data-stu-id="a985b-121">This parameter is optional and default value is 5.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a985b-122">-ServerCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="a985b-122">-ServerCertificateThumbprint</span></span>
<span data-ttu-id="a985b-123">TLS iletişimi için sertifikaların parmak izi küme yönetimi hizmeti kullanılır. Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a985b-123">Thumbprint of certificates cluster management service uses for tls communication.This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a985b-124">-ServerX509Name</span><span class="sxs-lookup"><span data-stu-id="a985b-124">-ServerX509Name</span></span>
<span data-ttu-id="a985b-125">Sunucu x509 sertifika adları koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="a985b-125">Server X509 Certificate Names Collection.</span></span>
<span data-ttu-id="a985b-126">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a985b-126">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a985b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a985b-127">CommonParameters</span></span>
<span data-ttu-id="a985b-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a985b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a985b-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a985b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a985b-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a985b-130">INPUTS</span></span>

### <span data-ttu-id="a985b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a985b-131">System.String</span></span>

## <span data-ttu-id="a985b-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a985b-132">OUTPUTS</span></span>

### <span data-ttu-id="a985b-133">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementservicefabric</span><span class="sxs-lookup"><span data-stu-id="a985b-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="a985b-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a985b-134">NOTES</span></span>

## <span data-ttu-id="a985b-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a985b-135">RELATED LINKS</span></span>

[<span data-ttu-id="a985b-136">Get-Azapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="a985b-136">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="a985b-137">Yeni-Azsız arka uç</span><span class="sxs-lookup"><span data-stu-id="a985b-137">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="a985b-138">Yeni-Azapsananagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="a985b-138">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="a985b-139">Set-Azapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="a985b-139">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="a985b-140">Remove-Azapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="a985b-140">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
