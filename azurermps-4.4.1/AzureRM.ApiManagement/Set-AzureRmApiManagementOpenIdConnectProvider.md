---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: f890236907ea0a717245d9345be276a6ccf04b8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591831"
---
# <span data-ttu-id="92998-101">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="92998-101">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="92998-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92998-102">SYNOPSIS</span></span>
<span data-ttu-id="92998-103">OpenID Connect sağlayıcısını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="92998-103">Modifies an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92998-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="92998-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>]
 [-ClientSecret <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92998-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="92998-105">DESCRIPTION</span></span>
<span data-ttu-id="92998-106">**Set-Azurermapımanagementopenıdconnectprovider** cmdlet 'ı, Azure API Yönetimi 'Nde OpenID Connect sağlayıcısını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="92998-106">The **Set-AzureRmApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="92998-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="92998-107">EXAMPLES</span></span>

### <span data-ttu-id="92998-108">Örnek 1: sağlayıcı için istemci gizliliğini değiştirme</span><span class="sxs-lookup"><span data-stu-id="92998-108">Example 1: Change the client secret for a provider</span></span>
```
PS C:\>Set-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="92998-109">Bu komut, KIMLIĞI OICProvicer01 olan sağlayıcıyı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="92998-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="92998-110">Komut, sağlayıcı için bir istemci parolası belirtir.</span><span class="sxs-lookup"><span data-stu-id="92998-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="92998-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="92998-111">PARAMETERS</span></span>

### <span data-ttu-id="92998-112">-Clitıd</span><span class="sxs-lookup"><span data-stu-id="92998-112">-ClientId</span></span>
<span data-ttu-id="92998-113">Geliştirici konsolunun istemci KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="92998-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="92998-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="92998-114">-ClientSecret</span></span>
<span data-ttu-id="92998-115">Geliştirici konsolunun istemci gizliliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="92998-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="92998-116">-Context</span><span class="sxs-lookup"><span data-stu-id="92998-116">-Context</span></span>
<span data-ttu-id="92998-117">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="92998-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="92998-118">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="92998-118">-Description</span></span>
<span data-ttu-id="92998-119">Bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="92998-119">Specifies a description.</span></span>

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

### <span data-ttu-id="92998-120">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="92998-120">-MetadataEndpointUri</span></span>
<span data-ttu-id="92998-121">Sağlayıcının meta veri uç noktası URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="92998-121">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="92998-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="92998-122">-Name</span></span>
<span data-ttu-id="92998-123">Sağlayıcı için kolay bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="92998-123">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="92998-124">-Openıdconnectproviderıd</span><span class="sxs-lookup"><span data-stu-id="92998-124">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="92998-125">Bu cmdlet 'in değiştirdiği sağlayıcı için bir KIMLIK belirtir.</span><span class="sxs-lookup"><span data-stu-id="92998-125">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="92998-126">KIMLIK belirtmezseniz, bu cmdlet bir tane oluşturur.</span><span class="sxs-lookup"><span data-stu-id="92998-126">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="92998-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="92998-127">-PassThru</span></span>
<span data-ttu-id="92998-128">Bu cmdlet 'in değiştirdiği **Psapsananagementopenıdconnectprovider** öğesini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="92998-128">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="92998-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92998-129">-DefaultProfile</span></span>
<span data-ttu-id="92998-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="92998-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92998-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92998-131">CommonParameters</span></span>
<span data-ttu-id="92998-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="92998-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92998-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92998-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92998-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="92998-134">INPUTS</span></span>

## <span data-ttu-id="92998-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="92998-135">OUTPUTS</span></span>

### <span data-ttu-id="92998-136">Microsoft. Azure. Commands. Apsananaen. ServiceManagement. modeller. Psapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="92998-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="92998-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="92998-137">NOTES</span></span>

## <span data-ttu-id="92998-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="92998-138">RELATED LINKS</span></span>

[<span data-ttu-id="92998-139">Get-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="92998-139">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="92998-140">Yeni-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="92998-140">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="92998-141">Remove-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="92998-141">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)


