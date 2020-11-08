---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
ms.openlocfilehash: d75d385bc158e0855601d3432dff79b2e4339f2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108561"
---
# <span data-ttu-id="6fcae-101">Get-AzApiManagementIdentityProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="6fcae-101">Get-AzApiManagementIdentityProviderClientSecret</span></span>

## <span data-ttu-id="6fcae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fcae-102">SYNOPSIS</span></span>
<span data-ttu-id="6fcae-103">Kimlik sağlayıcısı istemci gizliliğini edinin.</span><span class="sxs-lookup"><span data-stu-id="6fcae-103">Get the identity provider client secret.</span></span>

## <span data-ttu-id="6fcae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6fcae-104">SYNTAX</span></span>

```
Get-AzApiManagementIdentityProviderClientSecret -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fcae-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6fcae-105">DESCRIPTION</span></span>
<span data-ttu-id="6fcae-106">Kimlik sağlayıcısı istemci gizliliğini edinin.</span><span class="sxs-lookup"><span data-stu-id="6fcae-106">Get the identity provider client secret.</span></span>

## <span data-ttu-id="6fcae-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6fcae-107">EXAMPLES</span></span>

### <span data-ttu-id="6fcae-108">Örnek 1: AAD türü kimlik sağlayıcısının istemci gizliliğini alma</span><span class="sxs-lookup"><span data-stu-id="6fcae-108">Example 1: Get the client secret of AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProviderClientSecret -Context $apimContext -Type Aad
```

<span data-ttu-id="6fcae-109">Azure Active Directory 'nin kimlik sağlayıcısı yapılandırmasının istemci gizliliğini alır.</span><span class="sxs-lookup"><span data-stu-id="6fcae-109">Gets the client secret of the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="6fcae-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6fcae-110">PARAMETERS</span></span>

### <span data-ttu-id="6fcae-111">-Context</span><span class="sxs-lookup"><span data-stu-id="6fcae-111">-Context</span></span>
<span data-ttu-id="6fcae-112">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="6fcae-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6fcae-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6fcae-113">This parameter is required.</span></span>

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

### <span data-ttu-id="6fcae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fcae-114">-DefaultProfile</span></span>
<span data-ttu-id="6fcae-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6fcae-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fcae-116">-Tür</span><span class="sxs-lookup"><span data-stu-id="6fcae-116">-Type</span></span>
<span data-ttu-id="6fcae-117">Kimlik sağlayıcısının tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="6fcae-117">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="6fcae-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6fcae-118">This parameter is required.</span></span>

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

### <span data-ttu-id="6fcae-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fcae-119">CommonParameters</span></span>
<span data-ttu-id="6fcae-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6fcae-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fcae-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6fcae-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fcae-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6fcae-122">INPUTS</span></span>

### <span data-ttu-id="6fcae-123">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="6fcae-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6fcae-124">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovidertype</span><span class="sxs-lookup"><span data-stu-id="6fcae-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="6fcae-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6fcae-125">OUTPUTS</span></span>

### <span data-ttu-id="6fcae-126">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementclientsecret</span><span class="sxs-lookup"><span data-stu-id="6fcae-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="6fcae-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6fcae-127">NOTES</span></span>

## <span data-ttu-id="6fcae-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6fcae-128">RELATED LINKS</span></span>
