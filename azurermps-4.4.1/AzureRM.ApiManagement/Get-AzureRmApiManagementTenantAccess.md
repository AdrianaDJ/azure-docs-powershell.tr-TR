---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: 30243ef1796e621d0898aae38e29ddb1dc7fd20b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593858"
---
# <span data-ttu-id="9ef1d-101">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="9ef1d-101">Get-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="9ef1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ef1d-102">SYNOPSIS</span></span>
<span data-ttu-id="9ef1d-103">Kiracının erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="9ef1d-103">Gets the access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ef1d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ef1d-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ef1d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ef1d-105">DESCRIPTION</span></span>
<span data-ttu-id="9ef1d-106">**Get-AzureRmApiManagementTenantAccess** cmdlet 'i kiracının kiracı erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="9ef1d-106">The **Get-AzureRmApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="9ef1d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ef1d-107">EXAMPLES</span></span>

### <span data-ttu-id="9ef1d-108">Örnek 1: kiracı erişimi yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="9ef1d-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>Get-AzureRmApiManagementTenantAccess -Context $ApimContext
```

<span data-ttu-id="9ef1d-109">Bu komut, belirtilen bağlam için kiracı erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="9ef1d-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="9ef1d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ef1d-110">PARAMETERS</span></span>

### <span data-ttu-id="9ef1d-111">-Context</span><span class="sxs-lookup"><span data-stu-id="9ef1d-111">-Context</span></span>
<span data-ttu-id="9ef1d-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ef1d-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9ef1d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ef1d-113">-DefaultProfile</span></span>
<span data-ttu-id="9ef1d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9ef1d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ef1d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ef1d-115">CommonParameters</span></span>
<span data-ttu-id="9ef1d-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ef1d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ef1d-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ef1d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ef1d-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ef1d-118">INPUTS</span></span>

## <span data-ttu-id="9ef1d-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ef1d-119">OUTPUTS</span></span>

### <span data-ttu-id="9ef1d-120">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementaccessınformation</span><span class="sxs-lookup"><span data-stu-id="9ef1d-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="9ef1d-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ef1d-121">NOTES</span></span>

## <span data-ttu-id="9ef1d-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ef1d-122">RELATED LINKS</span></span>

[<span data-ttu-id="9ef1d-123">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="9ef1d-123">Set-AzureRmApiManagementTenantAccess</span></span>](./Set-AzureRmApiManagementTenantAccess.md)


