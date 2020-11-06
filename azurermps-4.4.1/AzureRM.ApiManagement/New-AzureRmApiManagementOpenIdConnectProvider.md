---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: f008d21e1d1d3f2aba7c87255fa7c95074bca532
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591221"
---
# <span data-ttu-id="0c7fe-101">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0c7fe-101">New-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="0c7fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c7fe-102">SYNOPSIS</span></span>
<span data-ttu-id="0c7fe-103">OpenID Connect sağlayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0c7fe-103">Creates an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c7fe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c7fe-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] -Name <String> -MetadataEndpointUri <String> -ClientId <String>
 [-ClientSecret <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c7fe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c7fe-105">DESCRIPTION</span></span>
<span data-ttu-id="0c7fe-106">**Yeni-Azurermapımanagementopenıdconnectprovider** cmdlet 'ı, Azure API yönetiminde bir OpenID Connect sağlayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0c7fe-106">The **New-AzureRmApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="0c7fe-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c7fe-107">EXAMPLES</span></span>

### <span data-ttu-id="0c7fe-108">Örnek 1: sağlayıcı oluşturma</span><span class="sxs-lookup"><span data-stu-id="0c7fe-108">Example 1: Create a provider</span></span>
```
PS C:\>New-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="0c7fe-109">Bu komut contoso OpenID Connect Provider adlı bir OpenID Connect **sağlayıcısı** oluşturur</span><span class="sxs-lookup"><span data-stu-id="0c7fe-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="0c7fe-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c7fe-110">PARAMETERS</span></span>

### <span data-ttu-id="0c7fe-111">-Clitıd</span><span class="sxs-lookup"><span data-stu-id="0c7fe-111">-ClientId</span></span>
<span data-ttu-id="0c7fe-112">Geliştirici konsolunun istemci KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c7fe-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="0c7fe-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="0c7fe-113">-ClientSecret</span></span>
<span data-ttu-id="0c7fe-114">Geliştirici konsolunun istemci gizliliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c7fe-114">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="0c7fe-115">-Context</span><span class="sxs-lookup"><span data-stu-id="0c7fe-115">-Context</span></span>
<span data-ttu-id="0c7fe-116">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c7fe-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0c7fe-117">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="0c7fe-117">-Description</span></span>
<span data-ttu-id="0c7fe-118">Bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c7fe-118">Specifies a description.</span></span>

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

### <span data-ttu-id="0c7fe-119">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="0c7fe-119">-MetadataEndpointUri</span></span>
<span data-ttu-id="0c7fe-120">Sağlayıcının meta veri uç noktası URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c7fe-120">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="0c7fe-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="0c7fe-121">-Name</span></span>
<span data-ttu-id="0c7fe-122">Sağlayıcı için kolay bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c7fe-122">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="0c7fe-123">-Openıdconnectproviderıd</span><span class="sxs-lookup"><span data-stu-id="0c7fe-123">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="0c7fe-124">Sağlayıcı için bir KIMLIK belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c7fe-124">Specifies an ID for the provider.</span></span>
<span data-ttu-id="0c7fe-125">KIMLIK belirtmezseniz, bu cmdlet bir tane oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0c7fe-125">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="0c7fe-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c7fe-126">-DefaultProfile</span></span>
<span data-ttu-id="0c7fe-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0c7fe-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c7fe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c7fe-128">CommonParameters</span></span>
<span data-ttu-id="0c7fe-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c7fe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c7fe-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c7fe-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c7fe-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c7fe-131">INPUTS</span></span>

## <span data-ttu-id="0c7fe-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c7fe-132">OUTPUTS</span></span>

### <span data-ttu-id="0c7fe-133">Microsoft. Azure. Commands. Apsananaen. ServiceManagement. modeller. Psapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="0c7fe-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="0c7fe-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c7fe-134">NOTES</span></span>

## <span data-ttu-id="0c7fe-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c7fe-135">RELATED LINKS</span></span>

[<span data-ttu-id="0c7fe-136">Get-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="0c7fe-136">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="0c7fe-137">Remove-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="0c7fe-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="0c7fe-138">Set-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="0c7fe-138">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


