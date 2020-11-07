---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: b6c8c0260e1f45b55dedca4d0a9f1f5ab3fed59a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751160"
---
# <span data-ttu-id="531f9-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="531f9-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="531f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="531f9-102">SYNOPSIS</span></span>
<span data-ttu-id="531f9-103">OpenID Connect sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="531f9-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="531f9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="531f9-104">SYNTAX</span></span>

### <span data-ttu-id="531f9-105">Getallopenıdconnectproviders (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="531f9-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="531f9-106">Getbyopenidconnectproviderıd</span><span class="sxs-lookup"><span data-stu-id="531f9-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="531f9-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="531f9-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="531f9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="531f9-108">DESCRIPTION</span></span>
<span data-ttu-id="531f9-109">**Get-Azapımanagementopenıdconnectprovider** cmdlet 'ı Azure API yönetiminde OpenID Connect sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="531f9-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="531f9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="531f9-110">EXAMPLES</span></span>

### <span data-ttu-id="531f9-111">Örnek 1: tüm sağlayıcıları al</span><span class="sxs-lookup"><span data-stu-id="531f9-111">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="531f9-112">Bu komut, belirtilen bağlam için tüm OpenID bağlama sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="531f9-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="531f9-113">Örnek 2: KIMLIK kullanarak sağlayıcı alma</span><span class="sxs-lookup"><span data-stu-id="531f9-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="531f9-114">Bu komut, KIMLIĞI OICProvicer01 olan sağlayıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="531f9-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="531f9-115">Örnek 3: ad kullanarak sağlayıcı alma</span><span class="sxs-lookup"><span data-stu-id="531f9-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="531f9-116">Bu komut contoso OpenID Connect Provider adlı sağlayıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="531f9-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="531f9-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="531f9-117">PARAMETERS</span></span>

### <span data-ttu-id="531f9-118">-Context</span><span class="sxs-lookup"><span data-stu-id="531f9-118">-Context</span></span>
<span data-ttu-id="531f9-119">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="531f9-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="531f9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="531f9-120">-DefaultProfile</span></span>
<span data-ttu-id="531f9-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="531f9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="531f9-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="531f9-122">-Name</span></span>
<span data-ttu-id="531f9-123">Sağlayıcının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="531f9-123">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="531f9-124">Bir ad belirtirseniz, bu cmdlet bu sağlayıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="531f9-124">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="531f9-125">-Openıdconnectproviderıd</span><span class="sxs-lookup"><span data-stu-id="531f9-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="531f9-126">Bu cmdlet 'in kaldırdığı sağlayıcının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="531f9-126">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="531f9-127">Bir KIMLIK belirtirseniz, bu cmdlet bu sağlayıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="531f9-127">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByOpenIdConnectProviderId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="531f9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="531f9-128">CommonParameters</span></span>
<span data-ttu-id="531f9-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="531f9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="531f9-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="531f9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="531f9-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="531f9-131">INPUTS</span></span>

### <span data-ttu-id="531f9-132">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="531f9-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="531f9-133">System. String</span><span class="sxs-lookup"><span data-stu-id="531f9-133">System.String</span></span>

## <span data-ttu-id="531f9-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="531f9-134">OUTPUTS</span></span>

### <span data-ttu-id="531f9-135">Microsoft. Azure. Commands. Apsananaen. ServiceManagement. modeller. Psapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="531f9-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="531f9-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="531f9-136">NOTES</span></span>

## <span data-ttu-id="531f9-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="531f9-137">RELATED LINKS</span></span>

[<span data-ttu-id="531f9-138">Yeni-Azapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="531f9-138">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="531f9-139">Remove-Azapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="531f9-139">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="531f9-140">Set-Azapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="531f9-140">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


