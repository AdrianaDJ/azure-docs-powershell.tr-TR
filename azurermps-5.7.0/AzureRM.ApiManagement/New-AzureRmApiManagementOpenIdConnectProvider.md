---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 088b88bcaa7f0d493552060c150e9d76a4b16c7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586846"
---
# <span data-ttu-id="67826-101">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="67826-101">New-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="67826-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67826-102">SYNOPSIS</span></span>
<span data-ttu-id="67826-103">OpenID Connect sağlayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="67826-103">Creates an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67826-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="67826-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] -Name <String> -MetadataEndpointUri <String> -ClientId <String>
 [-ClientSecret <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67826-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="67826-105">DESCRIPTION</span></span>
<span data-ttu-id="67826-106">**Yeni-Azurermapımanagementopenıdconnectprovider** cmdlet 'ı, Azure API yönetiminde bir OpenID Connect sağlayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="67826-106">The **New-AzureRmApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="67826-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="67826-107">EXAMPLES</span></span>

### <span data-ttu-id="67826-108">Örnek 1: sağlayıcı oluşturma</span><span class="sxs-lookup"><span data-stu-id="67826-108">Example 1: Create a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="67826-109">Bu komut contoso OpenID Connect Provider adlı bir OpenID Connect **sağlayıcısı** oluşturur</span><span class="sxs-lookup"><span data-stu-id="67826-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="67826-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="67826-110">PARAMETERS</span></span>

### <span data-ttu-id="67826-111">-Clitıd</span><span class="sxs-lookup"><span data-stu-id="67826-111">-ClientId</span></span>
<span data-ttu-id="67826-112">Geliştirici konsolunun istemci KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="67826-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="67826-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="67826-113">-ClientSecret</span></span>
<span data-ttu-id="67826-114">Geliştirici konsolunun istemci gizliliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="67826-114">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="67826-115">-Context</span><span class="sxs-lookup"><span data-stu-id="67826-115">-Context</span></span>
<span data-ttu-id="67826-116">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="67826-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="67826-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67826-117">-DefaultProfile</span></span>
<span data-ttu-id="67826-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="67826-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="67826-119">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="67826-119">-Description</span></span>
<span data-ttu-id="67826-120">Bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="67826-120">Specifies a description.</span></span>

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

### <span data-ttu-id="67826-121">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="67826-121">-MetadataEndpointUri</span></span>
<span data-ttu-id="67826-122">Sağlayıcının meta veri uç noktası URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="67826-122">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="67826-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="67826-123">-Name</span></span>
<span data-ttu-id="67826-124">Sağlayıcı için kolay bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="67826-124">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="67826-125">-Openıdconnectproviderıd</span><span class="sxs-lookup"><span data-stu-id="67826-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="67826-126">Sağlayıcı için bir KIMLIK belirtir.</span><span class="sxs-lookup"><span data-stu-id="67826-126">Specifies an ID for the provider.</span></span>
<span data-ttu-id="67826-127">KIMLIK belirtmezseniz, bu cmdlet bir tane oluşturur.</span><span class="sxs-lookup"><span data-stu-id="67826-127">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="67826-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67826-128">CommonParameters</span></span>
<span data-ttu-id="67826-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="67826-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67826-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67826-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67826-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="67826-131">INPUTS</span></span>

### <span data-ttu-id="67826-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="67826-132">None</span></span>
<span data-ttu-id="67826-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="67826-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="67826-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="67826-134">OUTPUTS</span></span>

### <span data-ttu-id="67826-135">Microsoft. Azure. Commands. Apsananaen. ServiceManagement. modeller. Psapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="67826-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="67826-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="67826-136">NOTES</span></span>

## <span data-ttu-id="67826-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="67826-137">RELATED LINKS</span></span>

[<span data-ttu-id="67826-138">Get-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="67826-138">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="67826-139">Remove-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="67826-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="67826-140">Set-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="67826-140">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


