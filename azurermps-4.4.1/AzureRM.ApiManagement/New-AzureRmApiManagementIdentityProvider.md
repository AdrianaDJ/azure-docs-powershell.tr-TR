---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: d6536c63ab3241e999c87dfb025205571c29596c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591223"
---
# <span data-ttu-id="783e8-101">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="783e8-101">New-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="783e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="783e8-102">SYNOPSIS</span></span>
<span data-ttu-id="783e8-103">Yeni bir kimlik sağlayıcı yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="783e8-103">Creates a new Identity Provider configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="783e8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="783e8-104">SYNTAX</span></span>

```
New-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="783e8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="783e8-105">DESCRIPTION</span></span>
<span data-ttu-id="783e8-106">Yeni bir kimlik sağlayıcı yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="783e8-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="783e8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="783e8-107">EXAMPLES</span></span>

### <span data-ttu-id="783e8-108">Örnek 1: Facebook 'i geliştirici portalı oturumları için kimlik sağlayıcı olarak yapılandırma</span><span class="sxs-lookup"><span data-stu-id="783e8-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```
New-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="783e8-109">Bu komut, Facebook kimliğini, Apımanai hizmetinin Geliştirici Portalında kabul edilen bir kimlik sağlayıcısı olarak yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="783e8-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="783e8-110">Bu işlem, Facebook uygulamasının,.</span><span class="sxs-lookup"><span data-stu-id="783e8-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="783e8-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="783e8-111">PARAMETERS</span></span>

### <span data-ttu-id="783e8-112">-Allowedkiracılar</span><span class="sxs-lookup"><span data-stu-id="783e8-112">-AllowedTenants</span></span>
<span data-ttu-id="783e8-113">İzin verilen Azure Active Directory kiracıları listesi</span><span class="sxs-lookup"><span data-stu-id="783e8-113">List of allowed Azure Active Directory Tenants</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="783e8-114">-Clitıd</span><span class="sxs-lookup"><span data-stu-id="783e8-114">-ClientId</span></span>
<span data-ttu-id="783e8-115">Dış kimlik sağlayıcısındaki uygulamanın istemci kimliği.</span><span class="sxs-lookup"><span data-stu-id="783e8-115">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="783e8-116">Facebook oturumu için uygulama KIMLIĞI, Google oturumu için Istemci KIMLIĞI, Microsoft için uygulama KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="783e8-116">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="783e8-117">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="783e8-117">-ClientSecret</span></span>
<span data-ttu-id="783e8-118">Dış kimlik sağlayıcısında uygulamanın, oturum açma isteğine kimlik doğrulaması için kullanılan istemci parolası.</span><span class="sxs-lookup"><span data-stu-id="783e8-118">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="783e8-119">Örneğin, Facebook oturumu için uygulama gizliliğine, Google Login API anahtarı, Microsoft için ortak anahtar.</span><span class="sxs-lookup"><span data-stu-id="783e8-119">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="783e8-120">-Context</span><span class="sxs-lookup"><span data-stu-id="783e8-120">-Context</span></span>
<span data-ttu-id="783e8-121">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="783e8-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="783e8-122">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="783e8-122">This parameter is required.</span></span>

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

### <span data-ttu-id="783e8-123">-Tür</span><span class="sxs-lookup"><span data-stu-id="783e8-123">-Type</span></span>
<span data-ttu-id="783e8-124">Kimlik sağlayıcısının tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="783e8-124">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="783e8-125">Belirtilmişse tanımlayıcı tarafından kimlik sağlayıcı yapılandırmasını bulmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="783e8-125">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="783e8-126">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="783e8-126">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="783e8-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="783e8-127">-Confirm</span></span>
<span data-ttu-id="783e8-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="783e8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="783e8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="783e8-129">-WhatIf</span></span>
<span data-ttu-id="783e8-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="783e8-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="783e8-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="783e8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="783e8-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="783e8-132">-DefaultProfile</span></span>
<span data-ttu-id="783e8-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="783e8-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="783e8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="783e8-134">CommonParameters</span></span>
<span data-ttu-id="783e8-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="783e8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="783e8-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="783e8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="783e8-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="783e8-137">INPUTS</span></span>

## <span data-ttu-id="783e8-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="783e8-138">OUTPUTS</span></span>

### <span data-ttu-id="783e8-139">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="783e8-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="783e8-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="783e8-140">NOTES</span></span>

## <span data-ttu-id="783e8-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="783e8-141">RELATED LINKS</span></span>

[<span data-ttu-id="783e8-142">Get-Azurermapımanagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="783e8-142">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="783e8-143">Remove-Azurermapımanagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="783e8-143">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="783e8-144">Set-Azurermapımanagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="783e8-144">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)
