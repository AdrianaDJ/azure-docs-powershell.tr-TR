---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: e25e3bfad6c40b136c3cbaa65999b8118e0abd11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592515"
---
# <span data-ttu-id="52a8b-101">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="52a8b-101">Get-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="52a8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52a8b-102">SYNOPSIS</span></span>
<span data-ttu-id="52a8b-103">Kimlik sağlayıcısı yapılandırma ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="52a8b-103">Get the identity provider configuration details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52a8b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52a8b-104">SYNTAX</span></span>

### <span data-ttu-id="52a8b-105">Aldentityproviders (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="52a8b-105">AllIdentityProviders (Default)</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52a8b-106">IdentityProvider</span><span class="sxs-lookup"><span data-stu-id="52a8b-106">IdentityProviderByType</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52a8b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="52a8b-107">DESCRIPTION</span></span>
<span data-ttu-id="52a8b-108">Kimlik sağlayıcısı yapılandırma ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="52a8b-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="52a8b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52a8b-109">EXAMPLES</span></span>

### <span data-ttu-id="52a8b-110">Örnek 1: tüm kimlik sağlayıcılarını alma</span><span class="sxs-lookup"><span data-stu-id="52a8b-110">Example 1: Get all Identity Providers</span></span>

```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="52a8b-111">Hizmette tüm kimlik sağlayıcısı yapılandırmasını edinin.</span><span class="sxs-lookup"><span data-stu-id="52a8b-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="52a8b-112">AAD türü kimlik sağlayıcısını alma</span><span class="sxs-lookup"><span data-stu-id="52a8b-112">Get the AAD Type Identity Provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext -Type Aad
```

<span data-ttu-id="52a8b-113">Azure Active Directory 'nin kimlik sağlayıcı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="52a8b-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="52a8b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52a8b-114">PARAMETERS</span></span>

### <span data-ttu-id="52a8b-115">-Context</span><span class="sxs-lookup"><span data-stu-id="52a8b-115">-Context</span></span>
<span data-ttu-id="52a8b-116">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="52a8b-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="52a8b-117">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="52a8b-117">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52a8b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52a8b-118">-DefaultProfile</span></span>
<span data-ttu-id="52a8b-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="52a8b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a8b-120">-Tür</span><span class="sxs-lookup"><span data-stu-id="52a8b-120">-Type</span></span>
<span data-ttu-id="52a8b-121">Kimlik sağlayıcısının tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="52a8b-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="52a8b-122">Belirtilmişse tanımlayıcı tarafından kimlik sağlayıcı yapılandırmasını bulmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="52a8b-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="52a8b-123">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="52a8b-123">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52a8b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52a8b-124">CommonParameters</span></span>
<span data-ttu-id="52a8b-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52a8b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52a8b-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52a8b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52a8b-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52a8b-127">INPUTS</span></span>

### <span data-ttu-id="52a8b-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="52a8b-128">None</span></span>
<span data-ttu-id="52a8b-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="52a8b-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="52a8b-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52a8b-130">OUTPUTS</span></span>

### <span data-ttu-id="52a8b-131">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="52a8b-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>
<span data-ttu-id="52a8b-132">API Yönetim hizmetinde yapılandırılan kimlik sağlayıcısının ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="52a8b-132">The details of the Identity Provider configured in API Management service.</span></span>

### <span data-ttu-id="52a8b-133">IList<Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovider></span><span class="sxs-lookup"><span data-stu-id="52a8b-133">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider></span></span>
<span data-ttu-id="52a8b-134">API Yönetim hizmetinde yapılandırılan kimlik sağlayıcılarının listesi.</span><span class="sxs-lookup"><span data-stu-id="52a8b-134">The list of Identity Providers configured in API Management service.</span></span>

## <span data-ttu-id="52a8b-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52a8b-135">NOTES</span></span>

## <span data-ttu-id="52a8b-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52a8b-136">RELATED LINKS</span></span>

