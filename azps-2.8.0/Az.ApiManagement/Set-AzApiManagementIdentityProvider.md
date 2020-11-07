---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
ms.openlocfilehash: d2d689c9df73f7cd9bb6df6a5153e9afa71cb39d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753415"
---
# <span data-ttu-id="97c93-101">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="97c93-101">Set-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="97c93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97c93-102">SYNOPSIS</span></span>
<span data-ttu-id="97c93-103">Var olan bir kimlik sağlayıcısının yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="97c93-103">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="97c93-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97c93-104">SYNTAX</span></span>

### <span data-ttu-id="97c93-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="97c93-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97c93-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="97c93-106">ByInputObject</span></span>
```
Set-AzApiManagementIdentityProvider -InputObject <PsApiManagementIdentityProvider> [-ClientId <String>]
 [-ClientSecret <String>] [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>]
 [-SigninPolicyName <String>] [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97c93-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="97c93-107">DESCRIPTION</span></span>
<span data-ttu-id="97c93-108">Var olan bir kimlik sağlayıcısının yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="97c93-108">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="97c93-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97c93-109">EXAMPLES</span></span>

### <span data-ttu-id="97c93-110">Örnek 1: Facebook kimlik sağlayıcısını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="97c93-110">Example 1 : Update the facebook Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="97c93-111">Cmdlet, Facebook Identity sağlayıcısının Istemci gizliliğini güncelleştirir;</span><span class="sxs-lookup"><span data-stu-id="97c93-111">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="97c93-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97c93-112">PARAMETERS</span></span>

### <span data-ttu-id="97c93-113">-Allowedkiracılar</span><span class="sxs-lookup"><span data-stu-id="97c93-113">-AllowedTenants</span></span>
<span data-ttu-id="97c93-114">İzin verilen Azure Active Directory kiracıları listesi.</span><span class="sxs-lookup"><span data-stu-id="97c93-114">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="97c93-115">Yetkili</span><span class="sxs-lookup"><span data-stu-id="97c93-115">-Authority</span></span>
<span data-ttu-id="97c93-116">AAD veya AAD B2C için OpenID Connect Discovery uç noktası ana bilgisayar adı.</span><span class="sxs-lookup"><span data-stu-id="97c93-116">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="97c93-117">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="97c93-117">This parameter is optional.</span></span>

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

### <span data-ttu-id="97c93-118">-Clitıd</span><span class="sxs-lookup"><span data-stu-id="97c93-118">-ClientId</span></span>
<span data-ttu-id="97c93-119">Dış kimlik sağlayıcısındaki uygulamanın istemci kimliği.</span><span class="sxs-lookup"><span data-stu-id="97c93-119">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="97c93-120">Facebook oturumu için uygulama KIMLIĞI, Google oturumu için Istemci KIMLIĞI, Microsoft için uygulama KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="97c93-120">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="97c93-121">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="97c93-121">-ClientSecret</span></span>
<span data-ttu-id="97c93-122">Dış kimlik sağlayıcısında uygulamanın, oturum açma isteğine kimlik doğrulaması için kullanılan istemci parolası.</span><span class="sxs-lookup"><span data-stu-id="97c93-122">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="97c93-123">Örneğin, Facebook oturumu için uygulama gizliliğine, Google Login API anahtarı, Microsoft için ortak anahtar.</span><span class="sxs-lookup"><span data-stu-id="97c93-123">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="97c93-124">-Context</span><span class="sxs-lookup"><span data-stu-id="97c93-124">-Context</span></span>
<span data-ttu-id="97c93-125">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="97c93-125">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="97c93-126">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="97c93-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97c93-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97c93-127">-DefaultProfile</span></span>
<span data-ttu-id="97c93-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="97c93-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97c93-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97c93-129">-InputObject</span></span>
<span data-ttu-id="97c93-130">PsApiManagementIdentityProvider örneği.</span><span class="sxs-lookup"><span data-stu-id="97c93-130">Instance of PsApiManagementIdentityProvider.</span></span> <span data-ttu-id="97c93-131">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="97c93-131">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97c93-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="97c93-132">-PassThru</span></span>
<span data-ttu-id="97c93-133">Bu cmdlet 'in değiştirdiği  **Psapsananagementidentitysağlayıcısını** geri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="97c93-133">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="97c93-134">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="97c93-134">-PasswordResetPolicyName</span></span>
<span data-ttu-id="97c93-135">Parola sıfırlama Ilke adı.</span><span class="sxs-lookup"><span data-stu-id="97c93-135">Password Reset Policy Name.</span></span> <span data-ttu-id="97c93-136">Yalnızca AAD B2C Identity Provider için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="97c93-136">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="97c93-137">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="97c93-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="97c93-138">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="97c93-138">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="97c93-139">Profil düzenleme Ilkesi adı.</span><span class="sxs-lookup"><span data-stu-id="97c93-139">Profile Editing Policy Name.</span></span> <span data-ttu-id="97c93-140">Yalnızca AAD B2C Identity Provider için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="97c93-140">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="97c93-141">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="97c93-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="97c93-142">-Signınpolicyname</span><span class="sxs-lookup"><span data-stu-id="97c93-142">-SigninPolicyName</span></span>
<span data-ttu-id="97c93-143">Oturum açma Ilkesi adı.</span><span class="sxs-lookup"><span data-stu-id="97c93-143">Signin Policy Name.</span></span> <span data-ttu-id="97c93-144">Yalnızca AAD B2C Identity Provider için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="97c93-144">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="97c93-145">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="97c93-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="97c93-146">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="97c93-146">-SignupPolicyName</span></span>
<span data-ttu-id="97c93-147">Kaydolma Ilkesi adı.</span><span class="sxs-lookup"><span data-stu-id="97c93-147">Signup Policy Name.</span></span> <span data-ttu-id="97c93-148">Yalnızca AAD B2C Identity Provider için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="97c93-148">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="97c93-149">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="97c93-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="97c93-150">-Tür</span><span class="sxs-lookup"><span data-stu-id="97c93-150">-Type</span></span>
<span data-ttu-id="97c93-151">Var olan bir kimlik sağlayıcısının tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="97c93-151">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="97c93-152">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="97c93-152">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: ExpandedParameter
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97c93-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="97c93-153">-Confirm</span></span>
<span data-ttu-id="97c93-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="97c93-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97c93-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97c93-155">-WhatIf</span></span>
<span data-ttu-id="97c93-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="97c93-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97c93-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="97c93-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97c93-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97c93-158">CommonParameters</span></span>
<span data-ttu-id="97c93-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97c93-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97c93-160">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="97c93-160">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97c93-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97c93-161">INPUTS</span></span>

### <span data-ttu-id="97c93-162">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="97c93-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="97c93-163">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovidertype</span><span class="sxs-lookup"><span data-stu-id="97c93-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="97c93-164">System. String</span><span class="sxs-lookup"><span data-stu-id="97c93-164">System.String</span></span>

### <span data-ttu-id="97c93-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="97c93-165">System.String[]</span></span>

### <span data-ttu-id="97c93-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="97c93-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="97c93-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97c93-167">OUTPUTS</span></span>

### <span data-ttu-id="97c93-168">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="97c93-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="97c93-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97c93-169">NOTES</span></span>

## <span data-ttu-id="97c93-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97c93-170">RELATED LINKS</span></span>

[<span data-ttu-id="97c93-171">Yeni-Azapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="97c93-171">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="97c93-172">Get-Azapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="97c93-172">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="97c93-173">Remove-Azapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="97c93-173">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)
