---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: c0c659f195aa1104b14f41e4cbc82a1ad86a1b1f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109254"
---
# <span data-ttu-id="b07db-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="b07db-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="b07db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b07db-102">SYNOPSIS</span></span>
<span data-ttu-id="b07db-103">Kiracının erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="b07db-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="b07db-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b07db-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b07db-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b07db-105">DESCRIPTION</span></span>
<span data-ttu-id="b07db-106">**Get-AzApiManagementTenantAccess** cmdlet 'i kiracının kiracı erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="b07db-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>
<span data-ttu-id="b07db-107">Anahtarlar sonuç ayrıntılarına dahil olmaz.</span><span class="sxs-lookup"><span data-stu-id="b07db-107">Keys will not be included into result details.</span></span> <span data-ttu-id="b07db-108">İstemci gizliliğini almak için **Get-Azapsananagementtenantaccesssecret** seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b07db-108">To get client secret, use **Get-AzApiManagementTenantAccessSecret**.</span></span>

## <span data-ttu-id="b07db-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b07db-109">EXAMPLES</span></span>

### <span data-ttu-id="b07db-110">Örnek 1: kiracı erişimi yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="b07db-110">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="b07db-111">Bu komut, belirtilen bağlam için kiracı erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="b07db-111">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="b07db-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b07db-112">PARAMETERS</span></span>

### <span data-ttu-id="b07db-113">-Context</span><span class="sxs-lookup"><span data-stu-id="b07db-113">-Context</span></span>
<span data-ttu-id="b07db-114">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b07db-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b07db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b07db-115">-DefaultProfile</span></span>
<span data-ttu-id="b07db-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b07db-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b07db-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b07db-117">CommonParameters</span></span>
<span data-ttu-id="b07db-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b07db-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b07db-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b07db-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b07db-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b07db-120">INPUTS</span></span>

### <span data-ttu-id="b07db-121">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="b07db-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="b07db-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b07db-122">OUTPUTS</span></span>

### <span data-ttu-id="b07db-123">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementaccessınformation</span><span class="sxs-lookup"><span data-stu-id="b07db-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="b07db-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b07db-124">NOTES</span></span>

## <span data-ttu-id="b07db-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b07db-125">RELATED LINKS</span></span>

[<span data-ttu-id="b07db-126">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="b07db-126">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


