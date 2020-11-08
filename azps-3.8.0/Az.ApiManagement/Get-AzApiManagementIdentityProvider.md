---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 75525d3c77c3e2113c0e3cff5a7741ab916d7485
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097411"
---
# <span data-ttu-id="eb159-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="eb159-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="eb159-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb159-102">SYNOPSIS</span></span>
<span data-ttu-id="eb159-103">Kimlik sağlayıcısı yapılandırma ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="eb159-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="eb159-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eb159-104">SYNTAX</span></span>

### <span data-ttu-id="eb159-105">Aldentityproviders (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="eb159-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb159-106">IdentityProvider</span><span class="sxs-lookup"><span data-stu-id="eb159-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb159-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="eb159-107">DESCRIPTION</span></span>
<span data-ttu-id="eb159-108">Kimlik sağlayıcısı yapılandırma ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="eb159-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="eb159-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eb159-109">EXAMPLES</span></span>

### <span data-ttu-id="eb159-110">Örnek 1: tüm kimlik sağlayıcılarını alma</span><span class="sxs-lookup"><span data-stu-id="eb159-110">Example 1: Get all Identity Providers</span></span>

```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="eb159-111">Hizmette tüm kimlik sağlayıcısı yapılandırmasını edinin.</span><span class="sxs-lookup"><span data-stu-id="eb159-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="eb159-112">Örnek 2: AAD türü kimlik sağlayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="eb159-112">Example 2: Get the AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProvider -Context $apimContext -Type Aad


Type                     : Aad
ClientId                 : aaa
ClientSecret             : xxxxx
AllowedTenants           : {contosotest.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         :
SigninPolicyName         :
ProfileEditingPolicyName :
PasswordResetPolicyName  :
SigninTenant             :
Id                       : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/identityProviders/Aad
ResourceGroupName        : Api-Default-West-US
ServiceName              : contoso
```

<span data-ttu-id="eb159-113">Azure Active Directory 'nin kimlik sağlayıcı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="eb159-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

### <span data-ttu-id="eb159-114">Örnek 3: AAD B2C tür kimlik sağlayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="eb159-114">Example 3: Get the AAD B2C Type Identity Provider</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProvider -Context $context -Type AadB2C


Type                     : AadB2C
ClientId                 : f02dafe2-b8b8-48ec-a38e-27e5c16c51e5
ClientSecret             : xxxxxx
AllowedTenants           : {contosoaadb2c.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         : B2C_1_policy-signup
SigninPolicyName         : B2C_1_policy-signin
ProfileEditingPolicyName :
PasswordResetPolicyName  :
SigninTenant             : contosoaadb2c.onmicrosoft.com
Id                       : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/identityProviders/AadB2C
ResourceGroupName        : Api-Default-West-US
ServiceName              : contoso
```

<span data-ttu-id="eb159-115">Azure Active Directory 'nin kimlik sağlayıcı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="eb159-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="eb159-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eb159-116">PARAMETERS</span></span>

### <span data-ttu-id="eb159-117">-Context</span><span class="sxs-lookup"><span data-stu-id="eb159-117">-Context</span></span>
<span data-ttu-id="eb159-118">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="eb159-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="eb159-119">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="eb159-119">This parameter is required.</span></span>

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

### <span data-ttu-id="eb159-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb159-120">-DefaultProfile</span></span>
<span data-ttu-id="eb159-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eb159-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb159-122">-Tür</span><span class="sxs-lookup"><span data-stu-id="eb159-122">-Type</span></span>
<span data-ttu-id="eb159-123">Kimlik sağlayıcısının tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="eb159-123">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="eb159-124">Belirtilmişse tanımlayıcı tarafından kimlik sağlayıcı yapılandırmasını bulmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="eb159-124">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="eb159-125">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="eb159-125">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb159-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb159-126">CommonParameters</span></span>
<span data-ttu-id="eb159-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eb159-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb159-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="eb159-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb159-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eb159-129">INPUTS</span></span>

### <span data-ttu-id="eb159-130">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="eb159-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="eb159-131">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovidertype</span><span class="sxs-lookup"><span data-stu-id="eb159-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="eb159-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eb159-132">OUTPUTS</span></span>

### <span data-ttu-id="eb159-133">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="eb159-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="eb159-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eb159-134">NOTES</span></span>

## <span data-ttu-id="eb159-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eb159-135">RELATED LINKS</span></span>
