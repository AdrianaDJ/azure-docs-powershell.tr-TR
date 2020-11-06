---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6f568f27cf5b50cd517d8133578d6cf36060252f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587340"
---
# <span data-ttu-id="bcd0d-101">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bcd0d-101">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="bcd0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcd0d-102">SYNOPSIS</span></span>
<span data-ttu-id="bcd0d-103">OpenID Connect sağlayıcısını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="bcd0d-103">Modifies an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcd0d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bcd0d-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>]
 [-ClientSecret <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bcd0d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bcd0d-105">DESCRIPTION</span></span>
<span data-ttu-id="bcd0d-106">**Set-Azurermapımanagementopenıdconnectprovider** cmdlet 'ı, Azure API Yönetimi 'Nde OpenID Connect sağlayıcısını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="bcd0d-106">The **Set-AzureRmApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="bcd0d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bcd0d-107">EXAMPLES</span></span>

### <span data-ttu-id="bcd0d-108">Örnek 1: sağlayıcı için istemci gizliliğini değiştirme</span><span class="sxs-lookup"><span data-stu-id="bcd0d-108">Example 1: Change the client secret for a provider</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="bcd0d-109">Bu komut, KIMLIĞI OICProvicer01 olan sağlayıcıyı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="bcd0d-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="bcd0d-110">Komut, sağlayıcı için bir istemci parolası belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcd0d-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="bcd0d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bcd0d-111">PARAMETERS</span></span>

### <span data-ttu-id="bcd0d-112">-Clitıd</span><span class="sxs-lookup"><span data-stu-id="bcd0d-112">-ClientId</span></span>
<span data-ttu-id="bcd0d-113">Geliştirici konsolunun istemci KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcd0d-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="bcd0d-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="bcd0d-114">-ClientSecret</span></span>
<span data-ttu-id="bcd0d-115">Geliştirici konsolunun istemci gizliliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcd0d-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="bcd0d-116">-Context</span><span class="sxs-lookup"><span data-stu-id="bcd0d-116">-Context</span></span>
<span data-ttu-id="bcd0d-117">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcd0d-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="bcd0d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcd0d-118">-DefaultProfile</span></span>
<span data-ttu-id="bcd0d-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bcd0d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcd0d-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="bcd0d-120">-Description</span></span>
<span data-ttu-id="bcd0d-121">Bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcd0d-121">Specifies a description.</span></span>

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

### <span data-ttu-id="bcd0d-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="bcd0d-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="bcd0d-123">Sağlayıcının meta veri uç noktası URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcd0d-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="bcd0d-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="bcd0d-124">-Name</span></span>
<span data-ttu-id="bcd0d-125">Sağlayıcı için kolay bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcd0d-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="bcd0d-126">-Openıdconnectproviderıd</span><span class="sxs-lookup"><span data-stu-id="bcd0d-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="bcd0d-127">Bu cmdlet 'in değiştirdiği sağlayıcı için bir KIMLIK belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcd0d-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="bcd0d-128">KIMLIK belirtmezseniz, bu cmdlet bir tane oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bcd0d-128">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="bcd0d-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bcd0d-129">-PassThru</span></span>
<span data-ttu-id="bcd0d-130">Bu cmdlet 'in değiştirdiği **Psapsananagementopenıdconnectprovider** öğesini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcd0d-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="bcd0d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcd0d-131">CommonParameters</span></span>
<span data-ttu-id="bcd0d-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bcd0d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcd0d-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcd0d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcd0d-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bcd0d-134">INPUTS</span></span>

### <span data-ttu-id="bcd0d-135">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="bcd0d-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bcd0d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="bcd0d-136">System.String</span></span>

### <span data-ttu-id="bcd0d-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bcd0d-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bcd0d-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bcd0d-138">OUTPUTS</span></span>

### <span data-ttu-id="bcd0d-139">Microsoft. Azure. Commands. Apsananaen. ServiceManagement. modeller. Psapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="bcd0d-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="bcd0d-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bcd0d-140">NOTES</span></span>

## <span data-ttu-id="bcd0d-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bcd0d-141">RELATED LINKS</span></span>

[<span data-ttu-id="bcd0d-142">Get-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="bcd0d-142">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="bcd0d-143">Yeni-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="bcd0d-143">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="bcd0d-144">Remove-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="bcd0d-144">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)


