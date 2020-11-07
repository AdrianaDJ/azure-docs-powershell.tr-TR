---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: f3692383f5fc93c0d76951f6dcaeb409ae3ee0f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753586"
---
# <span data-ttu-id="31b0a-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="31b0a-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="31b0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31b0a-102">SYNOPSIS</span></span>
<span data-ttu-id="31b0a-103">Kimlik sağlayıcısı yapılandırma ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="31b0a-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="31b0a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="31b0a-104">SYNTAX</span></span>

### <span data-ttu-id="31b0a-105">Aldentityproviders (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="31b0a-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31b0a-106">IdentityProvider</span><span class="sxs-lookup"><span data-stu-id="31b0a-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31b0a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="31b0a-107">DESCRIPTION</span></span>
<span data-ttu-id="31b0a-108">Kimlik sağlayıcısı yapılandırma ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="31b0a-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="31b0a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="31b0a-109">EXAMPLES</span></span>

### <span data-ttu-id="31b0a-110">Örnek 1: tüm kimlik sağlayıcılarını alma</span><span class="sxs-lookup"><span data-stu-id="31b0a-110">Example 1: Get all Identity Providers</span></span>

```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="31b0a-111">Hizmette tüm kimlik sağlayıcısı yapılandırmasını edinin.</span><span class="sxs-lookup"><span data-stu-id="31b0a-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="31b0a-112">AAD türü kimlik sağlayıcısını alma</span><span class="sxs-lookup"><span data-stu-id="31b0a-112">Get the AAD Type Identity Provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext -Type Aad
```

<span data-ttu-id="31b0a-113">Azure Active Directory 'nin kimlik sağlayıcı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="31b0a-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="31b0a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="31b0a-114">PARAMETERS</span></span>

### <span data-ttu-id="31b0a-115">-Context</span><span class="sxs-lookup"><span data-stu-id="31b0a-115">-Context</span></span>
<span data-ttu-id="31b0a-116">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="31b0a-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="31b0a-117">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="31b0a-117">This parameter is required.</span></span>

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

### <span data-ttu-id="31b0a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b0a-118">-DefaultProfile</span></span>
<span data-ttu-id="31b0a-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="31b0a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31b0a-120">-Tür</span><span class="sxs-lookup"><span data-stu-id="31b0a-120">-Type</span></span>
<span data-ttu-id="31b0a-121">Kimlik sağlayıcısının tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="31b0a-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="31b0a-122">Belirtilmişse tanımlayıcı tarafından kimlik sağlayıcı yapılandırmasını bulmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="31b0a-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="31b0a-123">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="31b0a-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="31b0a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b0a-124">CommonParameters</span></span>
<span data-ttu-id="31b0a-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="31b0a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b0a-126">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="31b0a-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b0a-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="31b0a-127">INPUTS</span></span>

### <span data-ttu-id="31b0a-128">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="31b0a-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="31b0a-129">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovidertype</span><span class="sxs-lookup"><span data-stu-id="31b0a-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="31b0a-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="31b0a-130">OUTPUTS</span></span>

### <span data-ttu-id="31b0a-131">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="31b0a-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="31b0a-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="31b0a-132">NOTES</span></span>

## <span data-ttu-id="31b0a-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="31b0a-133">RELATED LINKS</span></span>
