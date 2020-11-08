---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
ms.openlocfilehash: dcc66b6d28157ff9d5551e2fdf0cab18f7727828
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108018"
---
# <span data-ttu-id="8c094-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="8c094-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span></span>

## <span data-ttu-id="8c094-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c094-102">SYNOPSIS</span></span>
<span data-ttu-id="8c094-103">OpenID Connect sağlayıcısı istemci gizliliğini alır.</span><span class="sxs-lookup"><span data-stu-id="8c094-103">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="8c094-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8c094-104">SYNTAX</span></span>

```
Get-AzApiManagementOpenIdConnectProviderClientSecret -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c094-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8c094-105">DESCRIPTION</span></span>
<span data-ttu-id="8c094-106">OpenID Connect sağlayıcısı istemci gizliliğini alır.</span><span class="sxs-lookup"><span data-stu-id="8c094-106">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="8c094-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8c094-107">EXAMPLES</span></span>

### <span data-ttu-id="8c094-108">Örnek 1: KIMLIK kullanarak sağlayıcı istemci gizliliğini alma</span><span class="sxs-lookup"><span data-stu-id="8c094-108">Example 1: Get a provider client secret by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProviderClientSecret -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="8c094-109">Bu komut, KIMLIĞI OICProvider01 olan sağlayıcının istemci gizliliğini alır.</span><span class="sxs-lookup"><span data-stu-id="8c094-109">This command gets a client secret of the provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="8c094-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8c094-110">PARAMETERS</span></span>

### <span data-ttu-id="8c094-111">-Context</span><span class="sxs-lookup"><span data-stu-id="8c094-111">-Context</span></span>
<span data-ttu-id="8c094-112">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="8c094-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8c094-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="8c094-113">This parameter is required.</span></span>

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

### <span data-ttu-id="8c094-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c094-114">-DefaultProfile</span></span>
<span data-ttu-id="8c094-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8c094-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c094-116">-Openıdconnectproviderıd</span><span class="sxs-lookup"><span data-stu-id="8c094-116">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="8c094-117">OpenID Connect sağlayıcısının tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="8c094-117">Identifier of a OpenID Connect Provider.</span></span>
<span data-ttu-id="8c094-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="8c094-118">This parameter is required.</span></span>

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

### <span data-ttu-id="8c094-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c094-119">CommonParameters</span></span>
<span data-ttu-id="8c094-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8c094-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c094-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8c094-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c094-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8c094-122">INPUTS</span></span>

### <span data-ttu-id="8c094-123">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="8c094-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8c094-124">System. String</span><span class="sxs-lookup"><span data-stu-id="8c094-124">System.String</span></span>

## <span data-ttu-id="8c094-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8c094-125">OUTPUTS</span></span>

### <span data-ttu-id="8c094-126">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementclientsecret</span><span class="sxs-lookup"><span data-stu-id="8c094-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="8c094-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8c094-127">NOTES</span></span>

## <span data-ttu-id="8c094-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8c094-128">RELATED LINKS</span></span>
