---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
ms.openlocfilehash: ec64a339c29facdbb940b8141c72222ff932c1bd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109257"
---
# <span data-ttu-id="e9e1e-101">Get-AzApiManagementTenantAccessSecret</span><span class="sxs-lookup"><span data-stu-id="e9e1e-101">Get-AzApiManagementTenantAccessSecret</span></span>

## <span data-ttu-id="e9e1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9e1e-102">SYNOPSIS</span></span>
<span data-ttu-id="e9e1e-103">Kiracının erişim yapılandırma anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e9e1e-103">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="e9e1e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9e1e-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9e1e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9e1e-105">DESCRIPTION</span></span>
<span data-ttu-id="e9e1e-106">Kiracının erişim yapılandırma anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e9e1e-106">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="e9e1e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9e1e-107">EXAMPLES</span></span>

### <span data-ttu-id="e9e1e-108">Örnek 1: kiracı erişimi yapılandırma anahtarlarını alma</span><span class="sxs-lookup"><span data-stu-id="e9e1e-108">Example 1: Get tenant access configuration keys</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccessSecret -Context $apimContext
```

<span data-ttu-id="e9e1e-109">Bu komut, belirtilen bağlam için kiracı erişimi yapılandırma anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e9e1e-109">This command gets the tenant access configuration keys for the specified context.</span></span>

## <span data-ttu-id="e9e1e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9e1e-110">PARAMETERS</span></span>

### <span data-ttu-id="e9e1e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="e9e1e-111">-Context</span></span>
<span data-ttu-id="e9e1e-112">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="e9e1e-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e9e1e-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e9e1e-113">This parameter is required.</span></span>

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

### <span data-ttu-id="e9e1e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9e1e-114">-DefaultProfile</span></span>
<span data-ttu-id="e9e1e-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e9e1e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9e1e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9e1e-116">CommonParameters</span></span>
<span data-ttu-id="e9e1e-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9e1e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9e1e-118">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e9e1e-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9e1e-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9e1e-119">INPUTS</span></span>

### <span data-ttu-id="e9e1e-120">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="e9e1e-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="e9e1e-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9e1e-121">OUTPUTS</span></span>

### <span data-ttu-id="e9e1e-122">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementaccessınformation</span><span class="sxs-lookup"><span data-stu-id="e9e1e-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="e9e1e-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9e1e-123">NOTES</span></span>

## <span data-ttu-id="e9e1e-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9e1e-124">RELATED LINKS</span></span>
