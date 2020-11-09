---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: b267fc854127c1cb098481ac483a7572c8b2e12f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321934"
---
# <span data-ttu-id="22516-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="22516-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="22516-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22516-102">SYNOPSIS</span></span>
<span data-ttu-id="22516-103">Kimlik sağlayıcısı yapılandırma ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="22516-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="22516-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="22516-104">SYNTAX</span></span>

### <span data-ttu-id="22516-105">Aldentityproviders (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="22516-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22516-106">IdentityProvider</span><span class="sxs-lookup"><span data-stu-id="22516-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22516-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="22516-107">DESCRIPTION</span></span>
<span data-ttu-id="22516-108">Kimlik sağlayıcısı yapılandırma ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="22516-108">Get the identity provider configuration details.</span></span>
<span data-ttu-id="22516-109">ClientSecret, sonuç ayrıntılarına eklenmeyecek.</span><span class="sxs-lookup"><span data-stu-id="22516-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="22516-110">İstemci gizliliğini almak için **Get-Azapsananagementidentityproviderclientsecret** seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="22516-110">To get client secret, use **Get-AzApiManagementIdentityProviderClientSecret**.</span></span>

## <span data-ttu-id="22516-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="22516-111">EXAMPLES</span></span>

### <span data-ttu-id="22516-112">Örnek 1: tüm kimlik sağlayıcılarını alma</span><span class="sxs-lookup"><span data-stu-id="22516-112">Example 1: Get all Identity Providers</span></span>

```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="22516-113">Hizmette tüm kimlik sağlayıcısı yapılandırmasını edinin.</span><span class="sxs-lookup"><span data-stu-id="22516-113">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="22516-114">Örnek 2: AAD türü kimlik sağlayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="22516-114">Example 2: Get the AAD Type Identity Provider</span></span>
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

<span data-ttu-id="22516-115">Azure Active Directory 'nin kimlik sağlayıcı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="22516-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

### <span data-ttu-id="22516-116">Örnek 3: AAD B2C tür kimlik sağlayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="22516-116">Example 3: Get the AAD B2C Type Identity Provider</span></span>
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

<span data-ttu-id="22516-117">Azure Active Directory 'nin kimlik sağlayıcı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="22516-117">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="22516-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="22516-118">PARAMETERS</span></span>

### <span data-ttu-id="22516-119">-Context</span><span class="sxs-lookup"><span data-stu-id="22516-119">-Context</span></span>
<span data-ttu-id="22516-120">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="22516-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="22516-121">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="22516-121">This parameter is required.</span></span>

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

### <span data-ttu-id="22516-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22516-122">-DefaultProfile</span></span>
<span data-ttu-id="22516-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="22516-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22516-124">-Tür</span><span class="sxs-lookup"><span data-stu-id="22516-124">-Type</span></span>
<span data-ttu-id="22516-125">Kimlik sağlayıcısının tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="22516-125">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="22516-126">Belirtilmişse tanımlayıcı tarafından kimlik sağlayıcı yapılandırmasını bulmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="22516-126">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="22516-127">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="22516-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="22516-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22516-128">CommonParameters</span></span>
<span data-ttu-id="22516-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="22516-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22516-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="22516-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22516-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="22516-131">INPUTS</span></span>

### <span data-ttu-id="22516-132">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="22516-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="22516-133">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovidertype</span><span class="sxs-lookup"><span data-stu-id="22516-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="22516-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="22516-134">OUTPUTS</span></span>

### <span data-ttu-id="22516-135">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="22516-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="22516-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="22516-136">NOTES</span></span>

## <span data-ttu-id="22516-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="22516-137">RELATED LINKS</span></span>
