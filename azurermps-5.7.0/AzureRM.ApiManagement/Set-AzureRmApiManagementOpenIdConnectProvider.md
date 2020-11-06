---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: c914c49aeb4f2a763a09c5b513bcbe7809110b05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594505"
---
# <span data-ttu-id="f712c-101">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f712c-101">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="f712c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f712c-102">SYNOPSIS</span></span>
<span data-ttu-id="f712c-103">OpenID Connect sağlayıcısını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f712c-103">Modifies an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f712c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f712c-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>]
 [-ClientSecret <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f712c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f712c-105">DESCRIPTION</span></span>
<span data-ttu-id="f712c-106">**Set-Azurermapımanagementopenıdconnectprovider** cmdlet 'ı, Azure API Yönetimi 'Nde OpenID Connect sağlayıcısını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f712c-106">The **Set-AzureRmApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="f712c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f712c-107">EXAMPLES</span></span>

### <span data-ttu-id="f712c-108">Örnek 1: sağlayıcı için istemci gizliliğini değiştirme</span><span class="sxs-lookup"><span data-stu-id="f712c-108">Example 1: Change the client secret for a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="f712c-109">Bu komut, KIMLIĞI OICProvicer01 olan sağlayıcıyı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f712c-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="f712c-110">Komut, sağlayıcı için bir istemci parolası belirtir.</span><span class="sxs-lookup"><span data-stu-id="f712c-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="f712c-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f712c-111">PARAMETERS</span></span>

### <span data-ttu-id="f712c-112">-Clitıd</span><span class="sxs-lookup"><span data-stu-id="f712c-112">-ClientId</span></span>
<span data-ttu-id="f712c-113">Geliştirici konsolunun istemci KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f712c-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="f712c-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="f712c-114">-ClientSecret</span></span>
<span data-ttu-id="f712c-115">Geliştirici konsolunun istemci gizliliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f712c-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="f712c-116">-Context</span><span class="sxs-lookup"><span data-stu-id="f712c-116">-Context</span></span>
<span data-ttu-id="f712c-117">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f712c-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f712c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f712c-118">-DefaultProfile</span></span>
<span data-ttu-id="f712c-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f712c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="f712c-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="f712c-120">-Description</span></span>
<span data-ttu-id="f712c-121">Bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="f712c-121">Specifies a description.</span></span>

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

### <span data-ttu-id="f712c-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="f712c-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="f712c-123">Sağlayıcının meta veri uç noktası URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f712c-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="f712c-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="f712c-124">-Name</span></span>
<span data-ttu-id="f712c-125">Sağlayıcı için kolay bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="f712c-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="f712c-126">-Openıdconnectproviderıd</span><span class="sxs-lookup"><span data-stu-id="f712c-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="f712c-127">Bu cmdlet 'in değiştirdiği sağlayıcı için bir KIMLIK belirtir.</span><span class="sxs-lookup"><span data-stu-id="f712c-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="f712c-128">KIMLIK belirtmezseniz, bu cmdlet bir tane oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f712c-128">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="f712c-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f712c-129">-PassThru</span></span>
<span data-ttu-id="f712c-130">Bu cmdlet 'in değiştirdiği **Psapsananagementopenıdconnectprovider** öğesini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f712c-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f712c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f712c-131">CommonParameters</span></span>
<span data-ttu-id="f712c-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f712c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f712c-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f712c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f712c-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f712c-134">INPUTS</span></span>

### <span data-ttu-id="f712c-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f712c-135">None</span></span>
<span data-ttu-id="f712c-136">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="f712c-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f712c-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f712c-137">OUTPUTS</span></span>

### <span data-ttu-id="f712c-138">Microsoft. Azure. Commands. Apsananaen. ServiceManagement. modeller. Psapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="f712c-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="f712c-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f712c-139">NOTES</span></span>

## <span data-ttu-id="f712c-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f712c-140">RELATED LINKS</span></span>

[<span data-ttu-id="f712c-141">Get-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="f712c-141">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="f712c-142">Yeni-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="f712c-142">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="f712c-143">Remove-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="f712c-143">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)


