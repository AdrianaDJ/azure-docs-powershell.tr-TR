---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: fe320af601fad9d905471525b1a418c12c355f63
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917684"
---
# <span data-ttu-id="1286b-101">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="1286b-101">Set-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="1286b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1286b-102">SYNOPSIS</span></span>
<span data-ttu-id="1286b-103">OpenID Connect sağlayıcısını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1286b-103">Modifies an OpenID Connect provider.</span></span>

## <span data-ttu-id="1286b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1286b-104">SYNTAX</span></span>

```
Set-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>] [-ClientSecret <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1286b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1286b-105">DESCRIPTION</span></span>
<span data-ttu-id="1286b-106">**Set-Azapımanagementopenıdconnectprovider** cmdlet 'ı Azure API Yönetimi 'Nde OpenID Connect sağlayıcısını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1286b-106">The **Set-AzApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="1286b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1286b-107">EXAMPLES</span></span>

### <span data-ttu-id="1286b-108">Örnek 1: sağlayıcı için istemci gizliliğini değiştirme</span><span class="sxs-lookup"><span data-stu-id="1286b-108">Example 1: Change the client secret for a provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="1286b-109">Bu komut, KIMLIĞI OICProvicer01 olan sağlayıcıyı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1286b-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="1286b-110">Komut, sağlayıcı için bir istemci parolası belirtir.</span><span class="sxs-lookup"><span data-stu-id="1286b-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="1286b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1286b-111">PARAMETERS</span></span>

### <span data-ttu-id="1286b-112">-Clitıd</span><span class="sxs-lookup"><span data-stu-id="1286b-112">-ClientId</span></span>
<span data-ttu-id="1286b-113">Geliştirici konsolunun istemci KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1286b-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="1286b-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="1286b-114">-ClientSecret</span></span>
<span data-ttu-id="1286b-115">Geliştirici konsolunun istemci gizliliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1286b-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="1286b-116">-Context</span><span class="sxs-lookup"><span data-stu-id="1286b-116">-Context</span></span>
<span data-ttu-id="1286b-117">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1286b-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1286b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1286b-118">-DefaultProfile</span></span>
<span data-ttu-id="1286b-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1286b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1286b-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="1286b-120">-Description</span></span>
<span data-ttu-id="1286b-121">Bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="1286b-121">Specifies a description.</span></span>

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

### <span data-ttu-id="1286b-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="1286b-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="1286b-123">Sağlayıcının meta veri uç noktası URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1286b-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="1286b-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="1286b-124">-Name</span></span>
<span data-ttu-id="1286b-125">Sağlayıcı için kolay bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="1286b-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="1286b-126">-Openıdconnectproviderıd</span><span class="sxs-lookup"><span data-stu-id="1286b-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="1286b-127">Bu cmdlet 'in değiştirdiği sağlayıcı için bir KIMLIK belirtir.</span><span class="sxs-lookup"><span data-stu-id="1286b-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="1286b-128">KIMLIK belirtmezseniz, bu cmdlet bir tane oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1286b-128">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="1286b-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1286b-129">-PassThru</span></span>
<span data-ttu-id="1286b-130">Bu cmdlet 'in değiştirdiği **Psapsananagementopenıdconnectprovider** öğesini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1286b-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1286b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1286b-131">CommonParameters</span></span>
<span data-ttu-id="1286b-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1286b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1286b-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1286b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1286b-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1286b-134">INPUTS</span></span>

### <span data-ttu-id="1286b-135">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="1286b-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1286b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1286b-136">System.String</span></span>

### <span data-ttu-id="1286b-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1286b-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1286b-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1286b-138">OUTPUTS</span></span>

### <span data-ttu-id="1286b-139">Microsoft. Azure. Commands. Apsananaen. ServiceManagement. modeller. Psapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="1286b-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="1286b-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1286b-140">NOTES</span></span>

## <span data-ttu-id="1286b-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1286b-141">RELATED LINKS</span></span>

[<span data-ttu-id="1286b-142">Get-Azapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="1286b-142">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="1286b-143">Yeni-Azapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="1286b-143">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="1286b-144">Remove-Azapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="1286b-144">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

