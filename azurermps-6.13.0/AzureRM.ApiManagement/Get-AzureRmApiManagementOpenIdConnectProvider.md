---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 0ffe2dfbd1ccbb05ef1ad828861e1d439373caa9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573102"
---
# <span data-ttu-id="199c5-101">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="199c5-101">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="199c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="199c5-102">SYNOPSIS</span></span>
<span data-ttu-id="199c5-103">OpenID Connect sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="199c5-103">Gets OpenID Connect providers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="199c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="199c5-104">SYNTAX</span></span>

### <span data-ttu-id="199c5-105">Getallopenıdconnectproviders (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="199c5-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="199c5-106">Getbyopenidconnectproviderıd</span><span class="sxs-lookup"><span data-stu-id="199c5-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="199c5-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="199c5-107">GetByName</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="199c5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="199c5-108">DESCRIPTION</span></span>
<span data-ttu-id="199c5-109">**Get-Azurermapımanagementopenıdconnectprovider** cmdlet 'ı Azure API yönetiminde OpenID Connect sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="199c5-109">The **Get-AzureRmApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="199c5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="199c5-110">EXAMPLES</span></span>

### <span data-ttu-id="199c5-111">Örnek 1: tüm sağlayıcıları al</span><span class="sxs-lookup"><span data-stu-id="199c5-111">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="199c5-112">Bu komut, belirtilen bağlam için tüm OpenID bağlama sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="199c5-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="199c5-113">Örnek 2: KIMLIK kullanarak sağlayıcı alma</span><span class="sxs-lookup"><span data-stu-id="199c5-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="199c5-114">Bu komut, KIMLIĞI OICProvicer01 olan sağlayıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="199c5-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="199c5-115">Örnek 3: ad kullanarak sağlayıcı alma</span><span class="sxs-lookup"><span data-stu-id="199c5-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="199c5-116">Bu komut contoso OpenID Connect Provider adlı sağlayıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="199c5-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="199c5-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="199c5-117">PARAMETERS</span></span>

### <span data-ttu-id="199c5-118">-Context</span><span class="sxs-lookup"><span data-stu-id="199c5-118">-Context</span></span>
<span data-ttu-id="199c5-119">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="199c5-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="199c5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="199c5-120">-DefaultProfile</span></span>
<span data-ttu-id="199c5-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="199c5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="199c5-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="199c5-122">-Name</span></span>
<span data-ttu-id="199c5-123">Sağlayıcının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="199c5-123">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="199c5-124">Bir ad belirtirseniz, bu cmdlet bu sağlayıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="199c5-124">If you specify a name, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="199c5-125">-Openıdconnectproviderıd</span><span class="sxs-lookup"><span data-stu-id="199c5-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="199c5-126">Bu cmdlet 'in kaldırdığı sağlayıcının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="199c5-126">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="199c5-127">Bir KIMLIK belirtirseniz, bu cmdlet bu sağlayıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="199c5-127">If you specify an ID, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="199c5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="199c5-128">CommonParameters</span></span>
<span data-ttu-id="199c5-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="199c5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="199c5-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="199c5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="199c5-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="199c5-131">INPUTS</span></span>

### <span data-ttu-id="199c5-132">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="199c5-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="199c5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="199c5-133">System.String</span></span>

## <span data-ttu-id="199c5-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="199c5-134">OUTPUTS</span></span>

### <span data-ttu-id="199c5-135">Microsoft. Azure. Commands. Apsananaen. ServiceManagement. modeller. Psapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="199c5-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="199c5-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="199c5-136">NOTES</span></span>

## <span data-ttu-id="199c5-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="199c5-137">RELATED LINKS</span></span>

[<span data-ttu-id="199c5-138">Yeni-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="199c5-138">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="199c5-139">Remove-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="199c5-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="199c5-140">Set-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="199c5-140">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


