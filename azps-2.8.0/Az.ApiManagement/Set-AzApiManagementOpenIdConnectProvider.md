---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 880c44e3edf8a5d2c95144d2af8910e73d366192
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753409"
---
# <span data-ttu-id="a7a2d-101">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a7a2d-101">Set-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="a7a2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7a2d-102">SYNOPSIS</span></span>
<span data-ttu-id="a7a2d-103">OpenID Connect sağlayıcısını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a7a2d-103">Modifies an OpenID Connect provider.</span></span>

## <span data-ttu-id="a7a2d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7a2d-104">SYNTAX</span></span>

```
Set-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>] [-ClientSecret <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a7a2d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7a2d-105">DESCRIPTION</span></span>
<span data-ttu-id="a7a2d-106">**Set-Azapımanagementopenıdconnectprovider** cmdlet 'ı Azure API Yönetimi 'Nde OpenID Connect sağlayıcısını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a7a2d-106">The **Set-AzApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="a7a2d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7a2d-107">EXAMPLES</span></span>

### <span data-ttu-id="a7a2d-108">Örnek 1: sağlayıcı için istemci gizliliğini değiştirme</span><span class="sxs-lookup"><span data-stu-id="a7a2d-108">Example 1: Change the client secret for a provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="a7a2d-109">Bu komut, KIMLIĞI OICProvider01 olan sağlayıcıyı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a7a2d-109">This command modifies the provider that has the ID OICProvider01.</span></span>
<span data-ttu-id="a7a2d-110">Komut, sağlayıcı için bir istemci parolası belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7a2d-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="a7a2d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7a2d-111">PARAMETERS</span></span>

### <span data-ttu-id="a7a2d-112">-Clitıd</span><span class="sxs-lookup"><span data-stu-id="a7a2d-112">-ClientId</span></span>
<span data-ttu-id="a7a2d-113">Geliştirici konsolunun istemci KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7a2d-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="a7a2d-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="a7a2d-114">-ClientSecret</span></span>
<span data-ttu-id="a7a2d-115">Geliştirici konsolunun istemci gizliliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7a2d-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="a7a2d-116">-Context</span><span class="sxs-lookup"><span data-stu-id="a7a2d-116">-Context</span></span>
<span data-ttu-id="a7a2d-117">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7a2d-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a7a2d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7a2d-118">-DefaultProfile</span></span>
<span data-ttu-id="a7a2d-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a7a2d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7a2d-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="a7a2d-120">-Description</span></span>
<span data-ttu-id="a7a2d-121">Bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7a2d-121">Specifies a description.</span></span>

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

### <span data-ttu-id="a7a2d-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="a7a2d-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="a7a2d-123">Sağlayıcının meta veri uç noktası URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7a2d-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="a7a2d-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="a7a2d-124">-Name</span></span>
<span data-ttu-id="a7a2d-125">Sağlayıcı için kolay bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7a2d-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="a7a2d-126">-Openıdconnectproviderıd</span><span class="sxs-lookup"><span data-stu-id="a7a2d-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="a7a2d-127">Bu cmdlet 'in değiştirdiği sağlayıcı için bir KIMLIK belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7a2d-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="a7a2d-128">KIMLIK belirtmezseniz, bu cmdlet bir tane oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a7a2d-128">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="a7a2d-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a7a2d-129">-PassThru</span></span>
<span data-ttu-id="a7a2d-130">Bu cmdlet 'in değiştirdiği **Psapsananagementopenıdconnectprovider** öğesini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7a2d-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a7a2d-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="a7a2d-131">-Confirm</span></span>
<span data-ttu-id="a7a2d-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a7a2d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7a2d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7a2d-133">-WhatIf</span></span>
<span data-ttu-id="a7a2d-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a7a2d-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7a2d-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a7a2d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7a2d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7a2d-136">CommonParameters</span></span>
<span data-ttu-id="a7a2d-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7a2d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7a2d-138">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a7a2d-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7a2d-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7a2d-139">INPUTS</span></span>

### <span data-ttu-id="a7a2d-140">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="a7a2d-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a7a2d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a7a2d-141">System.String</span></span>

### <span data-ttu-id="a7a2d-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a7a2d-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a7a2d-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7a2d-143">OUTPUTS</span></span>

### <span data-ttu-id="a7a2d-144">Microsoft. Azure. Commands. Apsananaen. ServiceManagement. modeller. Psapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="a7a2d-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="a7a2d-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7a2d-145">NOTES</span></span>

## <span data-ttu-id="a7a2d-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7a2d-146">RELATED LINKS</span></span>

[<span data-ttu-id="a7a2d-147">Get-Azapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="a7a2d-147">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="a7a2d-148">Yeni-Azapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="a7a2d-148">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="a7a2d-149">Remove-Azapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="a7a2d-149">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)


