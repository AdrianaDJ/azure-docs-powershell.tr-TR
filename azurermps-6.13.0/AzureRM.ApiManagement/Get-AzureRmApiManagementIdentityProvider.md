---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 88147f9f26ecd31af1963c5ab378bb00262ef2ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763193"
---
# <span data-ttu-id="caf2d-101">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="caf2d-101">Get-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="caf2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="caf2d-102">SYNOPSIS</span></span>
<span data-ttu-id="caf2d-103">Kimlik sağlayıcısı yapılandırma ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="caf2d-103">Get the identity provider configuration details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="caf2d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="caf2d-104">SYNTAX</span></span>

### <span data-ttu-id="caf2d-105">Aldentityproviders (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="caf2d-105">AllIdentityProviders (Default)</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="caf2d-106">IdentityProvider</span><span class="sxs-lookup"><span data-stu-id="caf2d-106">IdentityProviderByType</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="caf2d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="caf2d-107">DESCRIPTION</span></span>
<span data-ttu-id="caf2d-108">Kimlik sağlayıcısı yapılandırma ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="caf2d-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="caf2d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="caf2d-109">EXAMPLES</span></span>

### <span data-ttu-id="caf2d-110">Örnek 1: tüm kimlik sağlayıcılarını alma</span><span class="sxs-lookup"><span data-stu-id="caf2d-110">Example 1: Get all Identity Providers</span></span>

```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="caf2d-111">Hizmette tüm kimlik sağlayıcısı yapılandırmasını edinin.</span><span class="sxs-lookup"><span data-stu-id="caf2d-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="caf2d-112">AAD türü kimlik sağlayıcısını alma</span><span class="sxs-lookup"><span data-stu-id="caf2d-112">Get the AAD Type Identity Provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext -Type Aad
```

<span data-ttu-id="caf2d-113">Azure Active Directory 'nin kimlik sağlayıcı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="caf2d-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="caf2d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="caf2d-114">PARAMETERS</span></span>

### <span data-ttu-id="caf2d-115">-Context</span><span class="sxs-lookup"><span data-stu-id="caf2d-115">-Context</span></span>
<span data-ttu-id="caf2d-116">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="caf2d-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="caf2d-117">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="caf2d-117">This parameter is required.</span></span>

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

### <span data-ttu-id="caf2d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caf2d-118">-DefaultProfile</span></span>
<span data-ttu-id="caf2d-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="caf2d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="caf2d-120">-Tür</span><span class="sxs-lookup"><span data-stu-id="caf2d-120">-Type</span></span>
<span data-ttu-id="caf2d-121">Kimlik sağlayıcısının tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="caf2d-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="caf2d-122">Belirtilmişse tanımlayıcı tarafından kimlik sağlayıcı yapılandırmasını bulmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="caf2d-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="caf2d-123">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="caf2d-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="caf2d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caf2d-124">CommonParameters</span></span>
<span data-ttu-id="caf2d-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="caf2d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caf2d-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caf2d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caf2d-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="caf2d-127">INPUTS</span></span>

### <span data-ttu-id="caf2d-128">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="caf2d-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="caf2d-129">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovidertype</span><span class="sxs-lookup"><span data-stu-id="caf2d-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="caf2d-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="caf2d-130">OUTPUTS</span></span>

### <span data-ttu-id="caf2d-131">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="caf2d-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="caf2d-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="caf2d-132">NOTES</span></span>

## <span data-ttu-id="caf2d-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="caf2d-133">RELATED LINKS</span></span>
