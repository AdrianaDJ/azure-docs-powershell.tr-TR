---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 2b38728f90de4639bf3e125f226ae2b40527ca45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591256"
---
# <span data-ttu-id="408e3-101">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="408e3-101">Get-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="408e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="408e3-102">SYNOPSIS</span></span>
<span data-ttu-id="408e3-103">Kimlik sağlayıcısı yapılandırma ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="408e3-103">Get the identity provider configuration details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="408e3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="408e3-104">SYNTAX</span></span>

### <span data-ttu-id="408e3-105">Aldentityproviders (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="408e3-105">AllIdentityProviders (Default)</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="408e3-106">IdentityProvider</span><span class="sxs-lookup"><span data-stu-id="408e3-106">IdentityProviderByType</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="408e3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="408e3-107">DESCRIPTION</span></span>
<span data-ttu-id="408e3-108">Kimlik sağlayıcısı yapılandırma ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="408e3-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="408e3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="408e3-109">EXAMPLES</span></span>

### <span data-ttu-id="408e3-110">--------------------------Örnek 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="408e3-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="408e3-111">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="408e3-111">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementIdentityProvider -Context $context
```

<span data-ttu-id="408e3-112">Hizmette tüm kimlik sağlayıcısı yapılandırmasını edinin.</span><span class="sxs-lookup"><span data-stu-id="408e3-112">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="408e3-113">--------------------------Örnek 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="408e3-113">--------------------------  Example 2  --------------------------</span></span>
<span data-ttu-id="408e3-114">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="408e3-114">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementIdentityProvider -Context $context -Type Aad
```

<span data-ttu-id="408e3-115">Azure Active Directory 'nin kimlik sağlayıcı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="408e3-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="408e3-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="408e3-116">PARAMETERS</span></span>

### <span data-ttu-id="408e3-117">-Context</span><span class="sxs-lookup"><span data-stu-id="408e3-117">-Context</span></span>
<span data-ttu-id="408e3-118">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="408e3-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="408e3-119">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="408e3-119">This parameter is required.</span></span>

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

### <span data-ttu-id="408e3-120">-Tür</span><span class="sxs-lookup"><span data-stu-id="408e3-120">-Type</span></span>
<span data-ttu-id="408e3-121">Kimlik sağlayıcısının tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="408e3-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="408e3-122">Belirtilmişse tanımlayıcı tarafından kimlik sağlayıcı yapılandırmasını bulmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="408e3-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="408e3-123">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="408e3-123">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="408e3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="408e3-124">-DefaultProfile</span></span>
<span data-ttu-id="408e3-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="408e3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="408e3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="408e3-126">CommonParameters</span></span>
<span data-ttu-id="408e3-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="408e3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="408e3-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="408e3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="408e3-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="408e3-129">INPUTS</span></span>

## <span data-ttu-id="408e3-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="408e3-130">OUTPUTS</span></span>

### <span data-ttu-id="408e3-131">IList<Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovider></span><span class="sxs-lookup"><span data-stu-id="408e3-131">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider></span></span>

### <span data-ttu-id="408e3-132">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="408e3-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="408e3-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="408e3-133">NOTES</span></span>

## <span data-ttu-id="408e3-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="408e3-134">RELATED LINKS</span></span>

