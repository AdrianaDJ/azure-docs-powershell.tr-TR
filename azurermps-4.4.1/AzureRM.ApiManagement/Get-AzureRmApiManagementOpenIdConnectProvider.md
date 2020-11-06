---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: d97090f6374890d9ae7ba24e53d6e1d60430f7b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587043"
---
# <span data-ttu-id="5c232-101">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5c232-101">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="5c232-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c232-102">SYNOPSIS</span></span>
<span data-ttu-id="5c232-103">OpenID Connect sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="5c232-103">Gets OpenID Connect providers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c232-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5c232-104">SYNTAX</span></span>

### <span data-ttu-id="5c232-105">Tüm OpenID Connect sağlayıcılarını alma (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5c232-105">Get all OpenID Connect Providers (Default)</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c232-106">OpenID Connect sağlayıcı KIMLIĞIYLE al</span><span class="sxs-lookup"><span data-stu-id="5c232-106">Get by OpenID Connect Provider ID</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c232-107">OpenID ile bul sağlayıcı kolay adı</span><span class="sxs-lookup"><span data-stu-id="5c232-107">Find by OpenID Connect Provider friendly Name</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c232-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5c232-108">DESCRIPTION</span></span>
<span data-ttu-id="5c232-109">**Get-Azurermapımanagementopenıdconnectprovider** cmdlet 'ı Azure API yönetiminde OpenID Connect sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="5c232-109">The **Get-AzureRmApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="5c232-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5c232-110">EXAMPLES</span></span>

### <span data-ttu-id="5c232-111">Örnek 1: tüm sağlayıcıları al</span><span class="sxs-lookup"><span data-stu-id="5c232-111">Example 1: Get all providers</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext
```

<span data-ttu-id="5c232-112">Bu komut, belirtilen bağlam için tüm OpenID bağlama sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="5c232-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="5c232-113">Örnek 2: KIMLIK kullanarak sağlayıcı alma</span><span class="sxs-lookup"><span data-stu-id="5c232-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="5c232-114">Bu komut, KIMLIĞI OICProvicer01 olan sağlayıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="5c232-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="5c232-115">Örnek 3: ad kullanarak sağlayıcı alma</span><span class="sxs-lookup"><span data-stu-id="5c232-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="5c232-116">Bu komut contoso OpenID Connect Provider adlı sağlayıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="5c232-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="5c232-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5c232-117">PARAMETERS</span></span>

### <span data-ttu-id="5c232-118">-Context</span><span class="sxs-lookup"><span data-stu-id="5c232-118">-Context</span></span>
<span data-ttu-id="5c232-119">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c232-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5c232-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="5c232-120">-Name</span></span>
<span data-ttu-id="5c232-121">Sağlayıcının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c232-121">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="5c232-122">Bir ad belirtirseniz, bu cmdlet bu sağlayıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="5c232-122">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by OpenID Connect Provider friendly Name
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c232-123">-Openıdconnectproviderıd</span><span class="sxs-lookup"><span data-stu-id="5c232-123">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="5c232-124">Bu cmdlet 'in kaldırdığı sağlayıcının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c232-124">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="5c232-125">Bir KIMLIK belirtirseniz, bu cmdlet bu sağlayıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="5c232-125">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by OpenID Connect Provider ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c232-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c232-126">-DefaultProfile</span></span>
<span data-ttu-id="5c232-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5c232-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c232-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c232-128">CommonParameters</span></span>
<span data-ttu-id="5c232-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5c232-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c232-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c232-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c232-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5c232-131">INPUTS</span></span>

## <span data-ttu-id="5c232-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5c232-132">OUTPUTS</span></span>

### <span data-ttu-id="5c232-133">IList<Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementopenıdconnectprovider></span><span class="sxs-lookup"><span data-stu-id="5c232-133">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider></span></span>

## <span data-ttu-id="5c232-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5c232-134">NOTES</span></span>

## <span data-ttu-id="5c232-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5c232-135">RELATED LINKS</span></span>

[<span data-ttu-id="5c232-136">Yeni-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="5c232-136">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="5c232-137">Remove-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="5c232-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="5c232-138">Set-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="5c232-138">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


