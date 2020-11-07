---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: fc033eb1989838d8ed8e20d568f92ef20f8275e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753519"
---
# <span data-ttu-id="b10bc-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="b10bc-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="b10bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b10bc-102">SYNOPSIS</span></span>
<span data-ttu-id="b10bc-103">Yeni bir kimlik sağlayıcı yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b10bc-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="b10bc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b10bc-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b10bc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b10bc-105">DESCRIPTION</span></span>
<span data-ttu-id="b10bc-106">Yeni bir kimlik sağlayıcı yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b10bc-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="b10bc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b10bc-107">EXAMPLES</span></span>

### <span data-ttu-id="b10bc-108">Örnek 1: Facebook 'i geliştirici portalı oturumları için kimlik sağlayıcı olarak yapılandırma</span><span class="sxs-lookup"><span data-stu-id="b10bc-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="b10bc-109">Bu komut, Facebook kimliğini, Apımanai hizmetinin Geliştirici Portalında kabul edilen bir kimlik sağlayıcısı olarak yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="b10bc-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="b10bc-110">Bu işlem, Facebook uygulamasının,.</span><span class="sxs-lookup"><span data-stu-id="b10bc-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

### <span data-ttu-id="b10bc-111">Örnek 2: geliştirici portalı oturumları için kimlik sağlayıcısı olarak adB2C 'i yapılandırma</span><span class="sxs-lookup"><span data-stu-id="b10bc-111">Example 2: Configures adB2C as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $context -Type AadB2C -ClientId 6b1fc750-9e68-450c-97d2-ba6acd0fbc20 -ClientSecret "foobar" -AllowedTenants 'samirtestbc.onmicrosoft.com' -SignupPolicyName B2C_1_signup-policy

Type                     : AadB2C
ClientId                 : 6b1fc750-9e68-450c-97d2-ba6acd0fbc20
ClientSecret             : foobar
AllowedTenants           : {samirtestbc.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         : B2C_1_signup-policy
SigninPolicyName         :
ProfileEditingPolicyName :
PasswordResetPolicyName  :
Id                       : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/identityProviders/AadB2C
ResourceGroupName        : Api-Default-WestUS
ServiceName              : contoso
```

<span data-ttu-id="b10bc-112">Bu komut, Facebook kimliğini, Apımanai hizmetinin Geliştirici Portalında kabul edilen bir kimlik sağlayıcısı olarak yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="b10bc-112">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="b10bc-113">Bu işlem, Facebook uygulamasının,.</span><span class="sxs-lookup"><span data-stu-id="b10bc-113">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="b10bc-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b10bc-114">PARAMETERS</span></span>

### <span data-ttu-id="b10bc-115">-Allowedkiracılar</span><span class="sxs-lookup"><span data-stu-id="b10bc-115">-AllowedTenants</span></span>
<span data-ttu-id="b10bc-116">İzin verilen Azure Active Directory kiracıları listesi</span><span class="sxs-lookup"><span data-stu-id="b10bc-116">List of allowed Azure Active Directory Tenants</span></span>

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

### <span data-ttu-id="b10bc-117">Yetkili</span><span class="sxs-lookup"><span data-stu-id="b10bc-117">-Authority</span></span>
<span data-ttu-id="b10bc-118">AAD veya AAD B2C için OpenID Connect Discovery uç noktası ana bilgisayar adı.</span><span class="sxs-lookup"><span data-stu-id="b10bc-118">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="b10bc-119">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="b10bc-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="b10bc-120">-Clitıd</span><span class="sxs-lookup"><span data-stu-id="b10bc-120">-ClientId</span></span>
<span data-ttu-id="b10bc-121">Dış kimlik sağlayıcısındaki uygulamanın istemci kimliği.</span><span class="sxs-lookup"><span data-stu-id="b10bc-121">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="b10bc-122">Facebook oturumu için uygulama KIMLIĞI, Google oturumu için Istemci KIMLIĞI, Microsoft için uygulama KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b10bc-122">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="b10bc-123">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="b10bc-123">-ClientSecret</span></span>
<span data-ttu-id="b10bc-124">Dış kimlik sağlayıcısında uygulamanın, oturum açma isteğine kimlik doğrulaması için kullanılan istemci parolası.</span><span class="sxs-lookup"><span data-stu-id="b10bc-124">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="b10bc-125">Örneğin, Facebook oturumu için uygulama gizliliğine, Google Login API anahtarı, Microsoft için ortak anahtar.</span><span class="sxs-lookup"><span data-stu-id="b10bc-125">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="b10bc-126">-Context</span><span class="sxs-lookup"><span data-stu-id="b10bc-126">-Context</span></span>
<span data-ttu-id="b10bc-127">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="b10bc-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b10bc-128">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="b10bc-128">This parameter is required.</span></span>

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

### <span data-ttu-id="b10bc-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b10bc-129">-DefaultProfile</span></span>
<span data-ttu-id="b10bc-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b10bc-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b10bc-131">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="b10bc-131">-PasswordResetPolicyName</span></span>
<span data-ttu-id="b10bc-132">Parola sıfırlama Ilke adı.</span><span class="sxs-lookup"><span data-stu-id="b10bc-132">Password Reset Policy Name.</span></span> <span data-ttu-id="b10bc-133">Yalnızca AAD B2C Identity Provider için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="b10bc-133">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="b10bc-134">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="b10bc-134">This parameter is optional.</span></span>

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

### <span data-ttu-id="b10bc-135">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="b10bc-135">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="b10bc-136">Profil düzenleme Ilkesi adı.</span><span class="sxs-lookup"><span data-stu-id="b10bc-136">Profile Editing Policy Name.</span></span> <span data-ttu-id="b10bc-137">Yalnızca AAD B2C Identity Provider için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="b10bc-137">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="b10bc-138">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="b10bc-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="b10bc-139">-Signınpolicyname</span><span class="sxs-lookup"><span data-stu-id="b10bc-139">-SigninPolicyName</span></span>
<span data-ttu-id="b10bc-140">Oturum açma Ilkesi adı.</span><span class="sxs-lookup"><span data-stu-id="b10bc-140">Signin Policy Name.</span></span> <span data-ttu-id="b10bc-141">Yalnızca AAD B2C Identity Provider için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="b10bc-141">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="b10bc-142">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="b10bc-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="b10bc-143">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="b10bc-143">-SignupPolicyName</span></span>
<span data-ttu-id="b10bc-144">Kaydolma Ilkesi adı.</span><span class="sxs-lookup"><span data-stu-id="b10bc-144">Signup Policy Name.</span></span> <span data-ttu-id="b10bc-145">Yalnızca AAD B2C Identity Provider için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="b10bc-145">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="b10bc-146">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="b10bc-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="b10bc-147">-Tür</span><span class="sxs-lookup"><span data-stu-id="b10bc-147">-Type</span></span>
<span data-ttu-id="b10bc-148">Kimlik sağlayıcısının tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="b10bc-148">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="b10bc-149">Belirtilmişse tanımlayıcı tarafından kimlik sağlayıcı yapılandırmasını bulmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="b10bc-149">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="b10bc-150">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="b10bc-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="b10bc-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="b10bc-151">-Confirm</span></span>
<span data-ttu-id="b10bc-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b10bc-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b10bc-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b10bc-153">-WhatIf</span></span>
<span data-ttu-id="b10bc-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b10bc-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b10bc-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b10bc-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b10bc-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b10bc-156">CommonParameters</span></span>
<span data-ttu-id="b10bc-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b10bc-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b10bc-158">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b10bc-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b10bc-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b10bc-159">INPUTS</span></span>

### <span data-ttu-id="b10bc-160">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="b10bc-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b10bc-161">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovidertype</span><span class="sxs-lookup"><span data-stu-id="b10bc-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="b10bc-162">System. String</span><span class="sxs-lookup"><span data-stu-id="b10bc-162">System.String</span></span>

### <span data-ttu-id="b10bc-163">System. String []</span><span class="sxs-lookup"><span data-stu-id="b10bc-163">System.String[]</span></span>

## <span data-ttu-id="b10bc-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b10bc-164">OUTPUTS</span></span>

### <span data-ttu-id="b10bc-165">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="b10bc-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="b10bc-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b10bc-166">NOTES</span></span>

## <span data-ttu-id="b10bc-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b10bc-167">RELATED LINKS</span></span>

[<span data-ttu-id="b10bc-168">Get-Azapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="b10bc-168">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="b10bc-169">Remove-Azapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="b10bc-169">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="b10bc-170">Set-Azapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="b10bc-170">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)
