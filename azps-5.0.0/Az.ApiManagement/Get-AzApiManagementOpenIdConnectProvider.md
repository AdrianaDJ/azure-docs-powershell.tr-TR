---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6968b4ea1b222d0f046611f10e65f8073a4ba86a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94326050"
---
# <span data-ttu-id="91c93-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="91c93-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="91c93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91c93-102">SYNOPSIS</span></span>
<span data-ttu-id="91c93-103">OpenID Connect sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="91c93-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="91c93-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91c93-104">SYNTAX</span></span>

### <span data-ttu-id="91c93-105">Getallopenıdconnectproviders (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="91c93-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91c93-106">Getbyopenidconnectproviderıd</span><span class="sxs-lookup"><span data-stu-id="91c93-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91c93-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="91c93-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91c93-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="91c93-108">DESCRIPTION</span></span>
<span data-ttu-id="91c93-109">**Get-Azapımanagementopenıdconnectprovider** cmdlet 'ı Azure API yönetiminde OpenID Connect sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="91c93-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>
<span data-ttu-id="91c93-110">ClientSecret, sonuç ayrıntılarına eklenmeyecek.</span><span class="sxs-lookup"><span data-stu-id="91c93-110">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="91c93-111">İstemci gizliliğini almak için **Get-Azapsananagementopenıdconnectproviderclientsecret** seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="91c93-111">To get client secret, use **Get-AzApiManagementOpenIdConnectProviderClientSecret**.</span></span>

## <span data-ttu-id="91c93-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91c93-112">EXAMPLES</span></span>

### <span data-ttu-id="91c93-113">Örnek 1: tüm sağlayıcıları al</span><span class="sxs-lookup"><span data-stu-id="91c93-113">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="91c93-114">Bu komut, belirtilen bağlam için tüm OpenID bağlama sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="91c93-114">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="91c93-115">Örnek 2: KIMLIK kullanarak sağlayıcı alma</span><span class="sxs-lookup"><span data-stu-id="91c93-115">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="91c93-116">Bu komut, KIMLIĞI OICProvider01 olan sağlayıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="91c93-116">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="91c93-117">Örnek 3: ad kullanarak sağlayıcı alma</span><span class="sxs-lookup"><span data-stu-id="91c93-117">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="91c93-118">Bu komut contoso OpenID Connect Provider adlı sağlayıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="91c93-118">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="91c93-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91c93-119">PARAMETERS</span></span>

### <span data-ttu-id="91c93-120">-Context</span><span class="sxs-lookup"><span data-stu-id="91c93-120">-Context</span></span>
<span data-ttu-id="91c93-121">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="91c93-121">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="91c93-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91c93-122">-DefaultProfile</span></span>
<span data-ttu-id="91c93-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="91c93-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91c93-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="91c93-124">-Name</span></span>
<span data-ttu-id="91c93-125">Sağlayıcının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91c93-125">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="91c93-126">Bir ad belirtirseniz, bu cmdlet bu sağlayıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="91c93-126">If you specify a name, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="91c93-127">-Openıdconnectproviderıd</span><span class="sxs-lookup"><span data-stu-id="91c93-127">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="91c93-128">Bu cmdlet 'in kaldırdığı sağlayıcının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="91c93-128">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="91c93-129">Bir KIMLIK belirtirseniz, bu cmdlet bu sağlayıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="91c93-129">If you specify an ID, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="91c93-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c93-130">CommonParameters</span></span>
<span data-ttu-id="91c93-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91c93-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c93-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="91c93-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c93-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91c93-133">INPUTS</span></span>

### <span data-ttu-id="91c93-134">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="91c93-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="91c93-135">System. String</span><span class="sxs-lookup"><span data-stu-id="91c93-135">System.String</span></span>

## <span data-ttu-id="91c93-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91c93-136">OUTPUTS</span></span>

### <span data-ttu-id="91c93-137">Microsoft. Azure. Commands. Apsananaen. ServiceManagement. modeller. Psapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="91c93-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="91c93-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91c93-138">NOTES</span></span>

## <span data-ttu-id="91c93-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91c93-139">RELATED LINKS</span></span>

[<span data-ttu-id="91c93-140">Yeni-Azapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="91c93-140">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="91c93-141">Remove-Azapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="91c93-141">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="91c93-142">Set-Azapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="91c93-142">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


