---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: c0730053dce60dbf556ef00f522aa463ffb26601
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761671"
---
# <span data-ttu-id="e12fc-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="e12fc-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="e12fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e12fc-102">SYNOPSIS</span></span>
<span data-ttu-id="e12fc-103">Yeni bir kimlik sağlayıcı yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e12fc-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="e12fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e12fc-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e12fc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e12fc-105">DESCRIPTION</span></span>
<span data-ttu-id="e12fc-106">Yeni bir kimlik sağlayıcı yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e12fc-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="e12fc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e12fc-107">EXAMPLES</span></span>

### <span data-ttu-id="e12fc-108">Örnek 1: Facebook 'i geliştirici portalı oturumları için kimlik sağlayıcı olarak yapılandırma</span><span class="sxs-lookup"><span data-stu-id="e12fc-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="e12fc-109">Bu komut, Facebook kimliğini, Apımanai hizmetinin Geliştirici Portalında kabul edilen bir kimlik sağlayıcısı olarak yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="e12fc-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="e12fc-110">Bu işlem, Facebook uygulamasının,.</span><span class="sxs-lookup"><span data-stu-id="e12fc-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="e12fc-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e12fc-111">PARAMETERS</span></span>

### <span data-ttu-id="e12fc-112">-Allowedkiracılar</span><span class="sxs-lookup"><span data-stu-id="e12fc-112">-AllowedTenants</span></span>
<span data-ttu-id="e12fc-113">İzin verilen Azure Active Directory kiracıları listesi</span><span class="sxs-lookup"><span data-stu-id="e12fc-113">List of allowed Azure Active Directory Tenants</span></span>

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

### <span data-ttu-id="e12fc-114">-Clitıd</span><span class="sxs-lookup"><span data-stu-id="e12fc-114">-ClientId</span></span>
<span data-ttu-id="e12fc-115">Dış kimlik sağlayıcısındaki uygulamanın istemci kimliği.</span><span class="sxs-lookup"><span data-stu-id="e12fc-115">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="e12fc-116">Facebook oturumu için uygulama KIMLIĞI, Google oturumu için Istemci KIMLIĞI, Microsoft için uygulama KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e12fc-116">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="e12fc-117">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="e12fc-117">-ClientSecret</span></span>
<span data-ttu-id="e12fc-118">Dış kimlik sağlayıcısında uygulamanın, oturum açma isteğine kimlik doğrulaması için kullanılan istemci parolası.</span><span class="sxs-lookup"><span data-stu-id="e12fc-118">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="e12fc-119">Örneğin, Facebook oturumu için uygulama gizliliğine, Google Login API anahtarı, Microsoft için ortak anahtar.</span><span class="sxs-lookup"><span data-stu-id="e12fc-119">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="e12fc-120">-Context</span><span class="sxs-lookup"><span data-stu-id="e12fc-120">-Context</span></span>
<span data-ttu-id="e12fc-121">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="e12fc-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e12fc-122">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e12fc-122">This parameter is required.</span></span>

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

### <span data-ttu-id="e12fc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e12fc-123">-DefaultProfile</span></span>
<span data-ttu-id="e12fc-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e12fc-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e12fc-125">-Tür</span><span class="sxs-lookup"><span data-stu-id="e12fc-125">-Type</span></span>
<span data-ttu-id="e12fc-126">Kimlik sağlayıcısının tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="e12fc-126">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="e12fc-127">Belirtilmişse tanımlayıcı tarafından kimlik sağlayıcı yapılandırmasını bulmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="e12fc-127">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="e12fc-128">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e12fc-128">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e12fc-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="e12fc-129">-Confirm</span></span>
<span data-ttu-id="e12fc-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e12fc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e12fc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e12fc-131">-WhatIf</span></span>
<span data-ttu-id="e12fc-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e12fc-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e12fc-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e12fc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e12fc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e12fc-134">CommonParameters</span></span>
<span data-ttu-id="e12fc-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e12fc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e12fc-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e12fc-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e12fc-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e12fc-137">INPUTS</span></span>

### <span data-ttu-id="e12fc-138">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="e12fc-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e12fc-139">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovidertype</span><span class="sxs-lookup"><span data-stu-id="e12fc-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="e12fc-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e12fc-140">System.String</span></span>

### <span data-ttu-id="e12fc-141">System. String []</span><span class="sxs-lookup"><span data-stu-id="e12fc-141">System.String[]</span></span>

## <span data-ttu-id="e12fc-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e12fc-142">OUTPUTS</span></span>

### <span data-ttu-id="e12fc-143">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="e12fc-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="e12fc-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e12fc-144">NOTES</span></span>

## <span data-ttu-id="e12fc-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e12fc-145">RELATED LINKS</span></span>

[<span data-ttu-id="e12fc-146">Get-Azapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="e12fc-146">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="e12fc-147">Remove-Azapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="e12fc-147">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="e12fc-148">Set-Azapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="e12fc-148">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)
