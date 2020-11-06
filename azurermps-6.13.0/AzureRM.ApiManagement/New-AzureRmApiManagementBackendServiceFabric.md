---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendServiceFabric.md
ms.openlocfilehash: 925e4949b444c9338fad3f88cf5066430e1b5a75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588642"
---
# <span data-ttu-id="ad5a5-101">New-AzureRmApiManagementBackendServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ad5a5-101">New-AzureRmApiManagementBackendServiceFabric</span></span>

## <span data-ttu-id="ad5a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad5a5-102">SYNOPSIS</span></span>
<span data-ttu-id="ad5a5-103">Nesnesi oluşturur `PsApiManagementServiceFabric`</span><span class="sxs-lookup"><span data-stu-id="ad5a5-103">Creates an object of `PsApiManagementServiceFabric`</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad5a5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad5a5-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendServiceFabric -ManagementEndpoint <String[]>
 -ClientCertificateThumbprint <String> [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>]
 [-ServerCertificateThumbprint <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad5a5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad5a5-105">DESCRIPTION</span></span>

<span data-ttu-id="ad5a5-106">**Yeni-Azurermapsananagementbackendservicefabric** cmdlet 'ı, `PsApiManagementServiceFabric` **Yeni-azurermapsananada** cmdlet 'te kullanılmak üzere bir nesne oluşturur ve **set-azurermapımanaarka uç**.</span><span class="sxs-lookup"><span data-stu-id="ad5a5-106">The **New-AzureRmApiManagementBackendServiceFabric** cmdlet creates an object of `PsApiManagementServiceFabric` to be used in cmdlet **New-AzureRmApiManagementBackend** and **Set-AzureRmApiManagementBackend**.</span></span>

## <span data-ttu-id="ad5a5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad5a5-107">EXAMPLES</span></span>

### <span data-ttu-id="ad5a5-108">Örnek 1: arka uç hizmet yapısı oluşturma In-Memory nesnesi</span><span class="sxs-lookup"><span data-stu-id="ad5a5-108">Example 1: Create a Backend Service Fabric In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzureRmApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

<span data-ttu-id="ad5a5-109">Arka uç hizmet doku sözleşmesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="ad5a5-109">Creates a Backend Service Fabric Contract</span></span>

## <span data-ttu-id="ad5a5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad5a5-110">PARAMETERS</span></span>

### <span data-ttu-id="ad5a5-111">-ClientCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="ad5a5-111">-ClientCertificateThumbprint</span></span>
<span data-ttu-id="ad5a5-112">Yönetim uç noktası için istemci sertifikası Parmak Izi.</span><span class="sxs-lookup"><span data-stu-id="ad5a5-112">Client Certificate Thumbprint for the management endpoint.</span></span>
<span data-ttu-id="ad5a5-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ad5a5-113">This parameter is required.</span></span>

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

### <span data-ttu-id="ad5a5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad5a5-114">-DefaultProfile</span></span>
<span data-ttu-id="ad5a5-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ad5a5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad5a5-116">-ManagementEndpoint</span><span class="sxs-lookup"><span data-stu-id="ad5a5-116">-ManagementEndpoint</span></span>
<span data-ttu-id="ad5a5-117">Hizmet yapısı küme yönetimi uç noktaları.</span><span class="sxs-lookup"><span data-stu-id="ad5a5-117">Service Fabric Cluster management Endpoints.</span></span>
<span data-ttu-id="ad5a5-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ad5a5-118">This parameter is required.</span></span>

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

### <span data-ttu-id="ad5a5-119">-MaxPartitionResolutionRetry</span><span class="sxs-lookup"><span data-stu-id="ad5a5-119">-MaxPartitionResolutionRetry</span></span>
<span data-ttu-id="ad5a5-120">Hizmet yapısı bölümü çözümlenirken en fazla deneme sayısı.</span><span class="sxs-lookup"><span data-stu-id="ad5a5-120">Maximum number of retries when resolving a Service Fabric partition.</span></span>
<span data-ttu-id="ad5a5-121">Bu parametre isteğe bağlıdır ve varsayılan değer 5 ' tir.</span><span class="sxs-lookup"><span data-stu-id="ad5a5-121">This parameter is optional and default value is 5.</span></span>

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

### <span data-ttu-id="ad5a5-122">-ServerCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="ad5a5-122">-ServerCertificateThumbprint</span></span>
<span data-ttu-id="ad5a5-123">TLS iletişimi için sertifikaların parmak izi küme yönetimi hizmeti kullanılır. Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ad5a5-123">Thumbprint of certificates cluster management service uses for tls communication.This parameter is optional.</span></span>

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

### <span data-ttu-id="ad5a5-124">-ServerX509Name</span><span class="sxs-lookup"><span data-stu-id="ad5a5-124">-ServerX509Name</span></span>
<span data-ttu-id="ad5a5-125">Sunucu x509 sertifika adları koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="ad5a5-125">Server X509 Certificate Names Collection.</span></span>
<span data-ttu-id="ad5a5-126">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ad5a5-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="ad5a5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad5a5-127">CommonParameters</span></span>
<span data-ttu-id="ad5a5-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad5a5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad5a5-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad5a5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad5a5-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad5a5-130">INPUTS</span></span>

### <span data-ttu-id="ad5a5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ad5a5-131">System.String</span></span>

## <span data-ttu-id="ad5a5-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad5a5-132">OUTPUTS</span></span>

### <span data-ttu-id="ad5a5-133">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementservicefabric</span><span class="sxs-lookup"><span data-stu-id="ad5a5-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="ad5a5-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad5a5-134">NOTES</span></span>

## <span data-ttu-id="ad5a5-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad5a5-135">RELATED LINKS</span></span>

[<span data-ttu-id="ad5a5-136">Get-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="ad5a5-136">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="ad5a5-137">Yeni-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="ad5a5-137">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="ad5a5-138">Yeni-Azurermapımanagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="ad5a5-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="ad5a5-139">Set-Azurermapımanaarka uç</span><span class="sxs-lookup"><span data-stu-id="ad5a5-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="ad5a5-140">Remove-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="ad5a5-140">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
