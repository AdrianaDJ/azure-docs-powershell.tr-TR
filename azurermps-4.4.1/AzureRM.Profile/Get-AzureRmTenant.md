---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
ms.openlocfilehash: 8ac36dd86abb996a934b59d064980233c931d214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590679"
---
# <span data-ttu-id="0d4df-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="0d4df-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="0d4df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d4df-102">SYNOPSIS</span></span>
<span data-ttu-id="0d4df-103">Geçerli Kullanıcı için yetkilendirilmiş kiracıları alır.</span><span class="sxs-lookup"><span data-stu-id="0d4df-103">Gets tenants that are authorized for the current user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d4df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d4df-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d4df-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d4df-105">DESCRIPTION</span></span>
<span data-ttu-id="0d4df-106">Get-AzureRmTenant cmdlet 'i, geçerli kullanıcı için yetkilendirilmiş kiracıları alır.</span><span class="sxs-lookup"><span data-stu-id="0d4df-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="0d4df-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d4df-107">EXAMPLES</span></span>

### <span data-ttu-id="0d4df-108">Örnek 1: Tüm kiracıları alma</span><span class="sxs-lookup"><span data-stu-id="0d4df-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

<span data-ttu-id="0d4df-109">Bu örnekte, bir Azure hesabının tüm yetkili kiracıları nasıl alabileceğiniz gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="0d4df-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="0d4df-110">Örnek 2: belirli bir kiracı alma</span><span class="sxs-lookup"><span data-stu-id="0d4df-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

<span data-ttu-id="0d4df-111">Bu örnekte, bir Azure hesabında belirli bir yetkili kiracının nasıl alınacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="0d4df-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="0d4df-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d4df-112">PARAMETERS</span></span>

### <span data-ttu-id="0d4df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d4df-113">-DefaultProfile</span></span>
<span data-ttu-id="0d4df-114">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0d4df-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d4df-115">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="0d4df-115">-TenantId</span></span>
<span data-ttu-id="0d4df-116">Bu cmdlet 'in aldığı kiracının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d4df-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d4df-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d4df-117">CommonParameters</span></span>
<span data-ttu-id="0d4df-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d4df-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d4df-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d4df-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d4df-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d4df-120">INPUTS</span></span>

## <span data-ttu-id="0d4df-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d4df-121">OUTPUTS</span></span>

### <span data-ttu-id="0d4df-122">PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="0d4df-122">PSAzureTenant</span></span>
<span data-ttu-id="0d4df-123">Bu cmdlet, geçerli hesap için yetkilendirilmiş kiracıları için kiracı KIMLIĞI ve ilişkili etki alanı bilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0d4df-123">This cmdlet returns the tenant ID and associated domain information for tenants authorized for the current account.</span></span>

## <span data-ttu-id="0d4df-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d4df-124">NOTES</span></span>

## <span data-ttu-id="0d4df-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d4df-125">RELATED LINKS</span></span>

