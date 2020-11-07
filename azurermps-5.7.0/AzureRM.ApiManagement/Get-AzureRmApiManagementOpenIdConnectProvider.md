---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: c26fb8991acc47ab655cb47c44194ca209423a70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763593"
---
# <span data-ttu-id="67680-101">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="67680-101">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="67680-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67680-102">SYNOPSIS</span></span>
<span data-ttu-id="67680-103">OpenID Connect sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="67680-103">Gets OpenID Connect providers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67680-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="67680-104">SYNTAX</span></span>

### <span data-ttu-id="67680-105">Getallopenıdconnectproviders (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="67680-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67680-106">Getbyopenidconnectproviderıd</span><span class="sxs-lookup"><span data-stu-id="67680-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67680-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="67680-107">GetByName</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67680-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="67680-108">DESCRIPTION</span></span>
<span data-ttu-id="67680-109">**Get-Azurermapımanagementopenıdconnectprovider** cmdlet 'ı Azure API yönetiminde OpenID Connect sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="67680-109">The **Get-AzureRmApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="67680-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="67680-110">EXAMPLES</span></span>

### <span data-ttu-id="67680-111">Örnek 1: tüm sağlayıcıları al</span><span class="sxs-lookup"><span data-stu-id="67680-111">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="67680-112">Bu komut, belirtilen bağlam için tüm OpenID bağlama sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="67680-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="67680-113">Örnek 2: KIMLIK kullanarak sağlayıcı alma</span><span class="sxs-lookup"><span data-stu-id="67680-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="67680-114">Bu komut, KIMLIĞI OICProvicer01 olan sağlayıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="67680-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="67680-115">Örnek 3: ad kullanarak sağlayıcı alma</span><span class="sxs-lookup"><span data-stu-id="67680-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="67680-116">Bu komut contoso OpenID Connect Provider adlı sağlayıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="67680-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="67680-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="67680-117">PARAMETERS</span></span>

### <span data-ttu-id="67680-118">-Context</span><span class="sxs-lookup"><span data-stu-id="67680-118">-Context</span></span>
<span data-ttu-id="67680-119">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="67680-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="67680-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67680-120">-DefaultProfile</span></span>
<span data-ttu-id="67680-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="67680-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="67680-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="67680-122">-Name</span></span>
<span data-ttu-id="67680-123">Sağlayıcının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="67680-123">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="67680-124">Bir ad belirtirseniz, bu cmdlet bu sağlayıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="67680-124">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67680-125">-Openıdconnectproviderıd</span><span class="sxs-lookup"><span data-stu-id="67680-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="67680-126">Bu cmdlet 'in kaldırdığı sağlayıcının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="67680-126">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="67680-127">Bir KIMLIK belirtirseniz, bu cmdlet bu sağlayıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="67680-127">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: String
Parameter Sets: GetByOpenIdConnectProviderId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67680-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67680-128">CommonParameters</span></span>
<span data-ttu-id="67680-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="67680-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67680-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67680-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67680-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="67680-131">INPUTS</span></span>

### <span data-ttu-id="67680-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="67680-132">None</span></span>
<span data-ttu-id="67680-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="67680-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="67680-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="67680-134">OUTPUTS</span></span>

### <span data-ttu-id="67680-135">Microsoft. Azure. Commands. Apsananaen. ServiceManagement. modeller. Psapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="67680-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>
<span data-ttu-id="67680-136">API Yönetim hizmetinde yapılandırılan OpenID Connect sağlayıcısının ayrıntısı.</span><span class="sxs-lookup"><span data-stu-id="67680-136">The detail of the OpenId connect Provider configured in API Management service.</span></span>

### <span data-ttu-id="67680-137">IList<Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementopenıdconnectprovider></span><span class="sxs-lookup"><span data-stu-id="67680-137">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider></span></span>
<span data-ttu-id="67680-138">API Yönetim hizmetinde yapılandırılan OpenID Connect sağlayıcılarının listesi.</span><span class="sxs-lookup"><span data-stu-id="67680-138">The list of OpenId Connect Providers configured in API Management service.</span></span>

## <span data-ttu-id="67680-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="67680-139">NOTES</span></span>

## <span data-ttu-id="67680-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="67680-140">RELATED LINKS</span></span>

[<span data-ttu-id="67680-141">Yeni-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="67680-141">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="67680-142">Remove-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="67680-142">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="67680-143">Set-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="67680-143">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


