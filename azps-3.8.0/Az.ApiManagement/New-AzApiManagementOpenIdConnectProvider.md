---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 37144ab119eba4f19c3b34b2b32dfd28ff305677
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097701"
---
# <span data-ttu-id="c99fc-101">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="c99fc-101">New-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="c99fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c99fc-102">SYNOPSIS</span></span>
<span data-ttu-id="c99fc-103">OpenID Connect sağlayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c99fc-103">Creates an OpenID Connect provider.</span></span>

## <span data-ttu-id="c99fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c99fc-104">SYNTAX</span></span>

```
New-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 -Name <String> -MetadataEndpointUri <String> -ClientId <String> [-ClientSecret <String>]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c99fc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c99fc-105">DESCRIPTION</span></span>
<span data-ttu-id="c99fc-106">**Yeni-Azapımanagementopenıdconnectprovider** cmdlet 'ı Azure API yönetiminde bir OpenID Connect sağlayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c99fc-106">The **New-AzApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="c99fc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c99fc-107">EXAMPLES</span></span>

### <span data-ttu-id="c99fc-108">Örnek 1: sağlayıcı oluşturma</span><span class="sxs-lookup"><span data-stu-id="c99fc-108">Example 1: Create a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="c99fc-109">Bu komut contoso OpenID Connect Provider adlı bir OpenID Connect **sağlayıcısı** oluşturur</span><span class="sxs-lookup"><span data-stu-id="c99fc-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="c99fc-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c99fc-110">PARAMETERS</span></span>

### <span data-ttu-id="c99fc-111">-Clitıd</span><span class="sxs-lookup"><span data-stu-id="c99fc-111">-ClientId</span></span>
<span data-ttu-id="c99fc-112">Geliştirici konsolunun istemci KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c99fc-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="c99fc-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="c99fc-113">-ClientSecret</span></span>
<span data-ttu-id="c99fc-114">Geliştirici konsolunun istemci gizliliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c99fc-114">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="c99fc-115">-Context</span><span class="sxs-lookup"><span data-stu-id="c99fc-115">-Context</span></span>
<span data-ttu-id="c99fc-116">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c99fc-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c99fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c99fc-117">-DefaultProfile</span></span>
<span data-ttu-id="c99fc-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c99fc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c99fc-119">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="c99fc-119">-Description</span></span>
<span data-ttu-id="c99fc-120">Bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="c99fc-120">Specifies a description.</span></span>

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

### <span data-ttu-id="c99fc-121">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="c99fc-121">-MetadataEndpointUri</span></span>
<span data-ttu-id="c99fc-122">Sağlayıcının meta veri uç noktası URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c99fc-122">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="c99fc-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="c99fc-123">-Name</span></span>
<span data-ttu-id="c99fc-124">Sağlayıcı için kolay bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="c99fc-124">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="c99fc-125">-Openıdconnectproviderıd</span><span class="sxs-lookup"><span data-stu-id="c99fc-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="c99fc-126">Sağlayıcı için bir KIMLIK belirtir.</span><span class="sxs-lookup"><span data-stu-id="c99fc-126">Specifies an ID for the provider.</span></span>
<span data-ttu-id="c99fc-127">KIMLIK belirtmezseniz, bu cmdlet bir tane oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c99fc-127">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="c99fc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c99fc-128">CommonParameters</span></span>
<span data-ttu-id="c99fc-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c99fc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c99fc-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c99fc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c99fc-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c99fc-131">INPUTS</span></span>

### <span data-ttu-id="c99fc-132">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="c99fc-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c99fc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c99fc-133">System.String</span></span>

## <span data-ttu-id="c99fc-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c99fc-134">OUTPUTS</span></span>

### <span data-ttu-id="c99fc-135">Microsoft. Azure. Commands. Apsananaen. ServiceManagement. modeller. Psapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="c99fc-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="c99fc-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c99fc-136">NOTES</span></span>

## <span data-ttu-id="c99fc-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c99fc-137">RELATED LINKS</span></span>

[<span data-ttu-id="c99fc-138">Get-Azapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="c99fc-138">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="c99fc-139">Remove-Azapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="c99fc-139">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="c99fc-140">Set-Azapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="c99fc-140">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


